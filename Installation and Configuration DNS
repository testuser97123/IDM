## Install and Configure DNS

### Setting up Hostname 

    [redhat@identity-management ~]$ hostnamectl set-hostname identity-management.ocp4.example.com ; bash 

### Install DNS Server

    [redhat@identity-management ~]$ sudo dnf install bind-utils bind -y 
    Updating Subscription Management repositories.
    Unable to read consumer identity

    This system is not registered with an entitlement server. You can use subscription-manager to register.

    gitlab_gitlab-ee                                                              637  B/s | 1.0 kB     00:01    
    gitlab_gitlab-ee-source                                                       573  B/s | 951  B     00:01    
    Package bind-utils-32:9.16.23-14.el9_3.x86_64 is already installed.
    Package bind-32:9.16.23-14.el9_3.x86_64 is already installed.
    Dependencies resolved.
    Nothing to do.
    Complete!

## Configure DNS Setting for IP & Zones. 

    [redhat@identity-management ~]$ sudo vim /etc/named.conf 
    options {
            listen-on port 53 { 192.168.122.2; };
            listen-on-v6 port 53 { ::1; };
            directory       "/var/named";
            dump-file       "/var/named/data/cache_dump.db";
            statistics-file "/var/named/data/named_stats.txt";
            memstatistics-file "/var/named/data/named_mem_stats.txt";
            secroots-file   "/var/named/data/named.secroots";
            recursing-file  "/var/named/data/named.recursing";
            allow-query     { 192.168.122.0/24; };
    ..
    zone "ocp4.example.com" IN {
            type master;
            file "for";
    };
    zone "122.168.192.in-addr.arpa" IN {
            type master;
            file "rev";
    };

### Configure forward Zone. 

    [redhat@identity-management ~]$ sudo vim /var/named/for
    $TTL 84660
    @       IN SOA  root.ocp4.example.com. identity-managment.ocp4.example.com.  (
                                            0       ; serial
                                            1D      ; refresh
                                            1H      ; retry
                                            1W      ; expire
                                            3H )    ; minimum
    @       IN      NS      identity-managment.ocp4.example.com.
    @       IN      A       192.168.122.2
    identity-managment.ocp4.example.com.    IN      A       192.168.122.2
    gitlab.ocp4.example.com.                IN      A       192.168.122.2

### Configure Reverse Zone. 

    [redhat@identity-management ~]$ sudo vim /var/named/rev 
    $TTL 84660
    @       IN SOA  root.ocp4.example.com. identity-managment.ocp4.example.com.  (
                                            0       ; serial
                                            1D      ; refresh
                                            1H      ; retry
                                            1W      ; expire
                                            3H )    ; minimum
    @       IN      NS      identity-managment.ocp4.example.com.
    @       IN      PTR     ocp4.example.com.
    identity-managment.ocp4.example.com.    IN      A       192.168.122.2
    gitlab.ocp4.example.com.                IN      A       192.168.122.2
    2       IN      PTR     identity-managment.ocp4.example.com.
    2       IN      PTR     gitlab.ocp4.example.com.

### Check nslookup 

    [root@identity-management ~]# nslookup identity-management.ocp4.example.com
    Server:		192.168.122.2
    Address:	192.168.122.2#53

    Name:	identity-management.ocp4.example.com
    Address: 192.168.122.2



    [root@identity-management named]# nslookup ocp4.example.com
    Server:		192.168.122.2
    Address:	192.168.122.2#53

    Name:	ocp4.example.com
    Address: 192.168.122.2

### Dig Nameserver resolver

    [root@identity-management named]# dig -x 192.168.122.2

    ; <<>> DiG 9.16.23-RH <<>> -x 192.168.122.2
    ;; global options: +cmd
    ;; Got answer:
    ;; ->>HEADER<<- opcode: QUERY, status: NOERROR, id: 39070
    ;; flags: qr aa rd ra; QUERY: 1, ANSWER: 2, AUTHORITY: 0, ADDITIONAL: 1

    ;; OPT PSEUDOSECTION:
    ; EDNS: version: 0, flags:; udp: 1232
    ; COOKIE: 83b26db746ed02560100000065f9b79960ede4d12ba8c6c0 (good)
    ;; QUESTION SECTION:
    ;2.122.168.192.in-addr.arpa.	IN	PTR

    ;; ANSWER SECTION:
    2.122.168.192.in-addr.arpa. 84660 IN	PTR	identity-managment.ocp4.example.com.
    2.122.168.192.in-addr.arpa. 84660 IN	PTR	gitlab.ocp4.example.com.

    ;; Query time: 1 msec
    ;; SERVER: 192.168.122.2#53(192.168.122.2)
    ;; WHEN: Tue Mar 19 21:34:41 IST 2024
    ;; MSG SIZE  rcvd: 153


    [root@identity-management named]# dig gitlab.ocp4.example.com

    ; <<>> DiG 9.16.23-RH <<>> gitlab.ocp4.example.com
    ;; global options: +cmd
    ;; Got answer:
    ;; ->>HEADER<<- opcode: QUERY, status: NOERROR, id: 5652
    ;; flags: qr aa rd ra; QUERY: 1, ANSWER: 1, AUTHORITY: 0, ADDITIONAL: 1

    ;; OPT PSEUDOSECTION:
    ; EDNS: version: 0, flags:; udp: 1232
    ; COOKIE: c5142984b99138bc0100000065f9b7a6a377abd7ae268b5e (good)
    ;; QUESTION SECTION:
    ;gitlab.ocp4.example.com.	IN	A

    ;; ANSWER SECTION:
    gitlab.ocp4.example.com. 84660	IN	A	192.168.122.2

    ;; Query time: 0 msec
    ;; SERVER: 192.168.122.2#53(192.168.122.2)
    ;; WHEN: Tue Mar 19 21:34:54 IST 2024
    ;; MSG SIZE  rcvd: 96


## Configure NTP clock synchronize.

# Install NTP 

    [root@identity-management ~]# yum install chrony -y 
    [root@identity-management ~]# vim /etc/chrony.conf 
    # Use public servers from the pool.ntp.org project.
    # Please consider joining the pool (https://www.pool.ntp.org/join.html).
    pool 2.rhel.pool.ntp.org iburst
    pool 192.168.122.2 iburst

    # Use NTP servers from DHCP.
    sourcedir /run/chrony-dhcp

    # Record the rate at which the system clock gains/losses time.
    driftfile /var/lib/chrony/drift

    # Allow the system clock to be stepped in the first three updates
    # if its offset is larger than 1 second.
    makestep 1.0 3

    # Enable kernel synchronization of the real-time clock (RTC).
    rtcsync

    # Enable hardware timestamping on all interfaces that support it.
    #hwtimestamp *

    # Increase the minimum number of selectable sources required to adjust
    # the system clock.
    #minsources 2

    # Allow NTP client access from local network.
    #allow 192.168.0.0/16
    allow 192.168.0.0/24
    # Serve time even if not synchronized to a time source.
    local stratum 10

    [root@identity-management ~]# systemctl restart chronyd 
    [root@identity-management ~]# systemctl enable --now chronyd 

    [root@identity-management ~]# chronyc sources
    MS Name/IP address         Stratum Poll Reach LastRx Last sample               
    ===============================================================================
    ^- 129.151.47.232                3   6    33     0  +3947us[+3947us] +/-   63ms
    ^* 172-232-97-196.ip.linode>     2   6    17     3   -158us[-1237us] +/-   44ms
    ^- ntp.nic.in                    2   6    17     3  -4224us[-4224us] +/-   78ms
    ^- ntp6.mum-in.hosts.301-mo>     2   6    27     2  -9856us[-9856us] +/-   77ms
    ^? gitlab.ocp4.example.com       0   7     0     -     +0ns[   +0ns] +/-    0ns

    [root@identity-management ~]# timedatectl 
                Local time: Tue 2024-03-19 21:41:02 IST
            Universal time: Tue 2024-03-19 16:11:02 UTC
                    RTC time: Tue 2024-03-19 16:11:02
                    Time zone: Asia/Kolkata (IST, +0530)
    System clock synchronized: yes
                NTP service: active
            RTC in local TZ: no
