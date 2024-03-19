

### Configure dnf module and install relevant IdM packages: 

    [root@identity-management ~]# dnf install ipa-server
    Updating Subscription Management repositories.
    Last metadata expiration check: 0:02:50 ago on Tue 19 Mar 2024 10:21:13 PM IST.
    Dependencies resolved.
    ====================================================================================================================================
    Package                                    Architecture  Version                     Repository                               Size
    ====================================================================================================================================
    Installing:
    ipa-server                                 x86_64        4.10.2-8.el9_3              rhel-9-for-x86_64-appstream-rpms        418 k
    Installing dependencies:
    389-ds-base                                x86_64        2.3.6-5.el9_3               rhel-9-for-x86_64-appstream-rpms        3.0 M
    389-ds-base-libs                           x86_64        2.3.6-5.el9_3               rhel-9-for-x86_64-appstream-rpms        1.5 M
    apache-commons-cli                         noarch        1.4-17.el9                  rhel-9-for-x86_64-appstream-rpms         73 k
    apache-commons-codec                       noarch        1.15-7.el9                  rhel-9-for-x86_64-appstream-rpms        304 k
    apache-commons-io                          noarch        1:2.8.0-8.el9               rhel-9-for-x86_64-appstream-rpms        286 k
    apache-commons-lang3                       noarch        3.12.0-6.el9                rhel-9-for-x86_64-appstream-rpms        561 k
    apache-commons-logging                     noarch        1.2-29.el9                  rhel-9-for-x86_64-appstream-rpms         80 k
    apache-commons-net                         noarch        3.6-14.el9                  rhel-9-for-x86_64-appstream-rpms        293 k
    apr                                        x86_64        1.7.0-12.el9_3              rhel-9-for-x86_64-appstream-rpms        126 k
    apr-util                                   x86_64        1.6.1-23.el9                rhel-9-for-x86_64-appstream-rpms         97 k
    apr-util-bdb                               x86_64        1.6.1-23.el9                rhel-9-for-x86_64-appstream-rpms         14 k
    augeas-libs                                x86_64        1.13.0-5.el9                rhel-9-for-x86_64-appstream-rpms        459 k
    autofs                                     x86_64        1:5.1.7-55.el9              rhel-9-for-x86_64-baseos-rpms           392 k
    certmonger                                 x86_64        0.79.17-1.el9               rhel-9-for-x86_64-appstream-rpms        618 k
    copy-jdk-configs                           noarch        4.0-3.el9                   rhel-9-for-x86_64-appstream-rpms         29 k
    cyrus-sasl-md5                             x86_64        2.1.27-21.el9               rhel-9-for-x86_64-appstream-rpms         45 k
    ecj                                        noarch        1:4.20-11.el9               rhel-9-for-x86_64-appstream-rpms        1.9 M
    fontawesome-fonts                          noarch        1:4.7.0-13.el9              rhel-9-for-x86_64-appstream-rpms        207 k
    gssproxy                                   x86_64        0.8.4-6.el9                 rhel-9-for-x86_64-baseos-rpms           114 k
    httpcomponents-client                      noarch        4.5.13-3.el9                rhel-9-for-x86_64-appstream-rpms        659 k
    httpcomponents-core                        noarch        4.4.13-7.el9                rhel-9-for-x86_64-appstream-rpms        635 k
    httpd                                      x86_64        2.4.57-5.el9                rhel-9-for-x86_64-appstream-rpms         52 k
    httpd-core                                 x86_64        2.4.57-5.el9                rhel-9-for-x86_64-appstream-rpms        1.5 M
    httpd-filesystem                           noarch        2.4.57-5.el9                rhel-9-for-x86_64-appstream-rpms         16 k
    httpd-tools                                x86_64        2.4.57-5.el9                rhel-9-for-x86_64-appstream-rpms         87 k
    idm-jss                                    x86_64        5.4.1-2.el9                 rhel-9-for-x86_64-appstream-rpms        1.3 M
    idm-ldapjdk                                noarch        5.4.0-1.el9                 rhel-9-for-x86_64-appstream-rpms        344 k
    idm-pki-acme                               noarch        11.4.2-1.el9                rhel-9-for-x86_64-appstream-rpms        989 k
    idm-pki-base                               noarch        11.4.2-1.el9                rhel-9-for-x86_64-appstream-rpms        275 k
    idm-pki-ca                                 noarch        11.4.2-1.el9                rhel-9-for-x86_64-appstream-rpms        1.7 M
    idm-pki-java                               noarch        11.4.2-1.el9                rhel-9-for-x86_64-appstream-rpms        619 k
    idm-pki-kra                                noarch        11.4.2-1.el9                rhel-9-for-x86_64-appstream-rpms        308 k
    idm-pki-server                             noarch        11.4.2-1.el9                rhel-9-for-x86_64-appstream-rpms        2.5 M
    idm-pki-tools                              x86_64        11.4.2-1.el9                rhel-9-for-x86_64-appstream-rpms        919 k
    idm-tomcatjss                              noarch        8.4.0-1.el9                 rhel-9-for-x86_64-appstream-rpms         40 k
    ipa-client                                 x86_64        4.10.2-8.el9_3              rhel-9-for-x86_64-appstream-rpms        133 k
    ipa-client-common                          noarch        4.10.2-8.el9_3              rhel-9-for-x86_64-appstream-rpms         46 k
    ipa-common                                 noarch        4.10.2-8.el9_3              rhel-9-for-x86_64-appstream-rpms        659 k
    ipa-healthcheck-core                       noarch        0.12-4.el9                  rhel-9-for-x86_64-appstream-rpms         64 k
    ipa-selinux                                noarch        4.10.2-8.el9_3              rhel-9-for-x86_64-appstream-rpms         34 k
    ipa-server-common                          noarch        4.10.2-8.el9_3              rhel-9-for-x86_64-appstream-rpms        503 k
    jakarta-activation                         noarch        1.2.2-5.el9                 rhel-9-for-x86_64-appstream-rpms         82 k
    jakarta-annotations                        noarch        1.3.5-13.el9                rhel-9-for-x86_64-appstream-rpms         48 k
    java-11-openjdk-headless                   x86_64        1:11.0.22.0.7-2.el9         rhel-9-for-x86_64-appstream-rpms         40 M
    java-17-openjdk-headless                   x86_64        1:17.0.10.0.7-2.el9         rhel-9-for-x86_64-appstream-rpms         45 M
    javapackages-filesystem                    noarch        6.0.0-4.el9                 rhel-9-for-x86_64-appstream-rpms         17 k
    javapackages-tools                         noarch        6.0.0-4.el9                 rhel-9-for-x86_64-appstream-rpms         29 k
    jaxb-api                                   noarch        2.3.3-5.el9                 rhel-9-for-x86_64-appstream-rpms        112 k
    jboss-jaxrs-2.0-api                        noarch        1.0.0-16.el9                rhel-9-for-x86_64-appstream-rpms        113 k
    jboss-logging                              noarch        3.4.1-9.el9                 rhel-9-for-x86_64-appstream-rpms         60 k
    jboss-logging-tools                        noarch        2.2.1-7.el9                 rhel-9-for-x86_64-appstream-rpms        224 k
    jdeparser                                  noarch        2.0.3-12.el9                rhel-9-for-x86_64-appstream-rpms        219 k
    keyutils                                   x86_64        1.6.3-1.el9                 rhel-9-for-x86_64-baseos-rpms            78 k
    krb5-pkinit                                x86_64        1.21.1-1.el9                rhel-9-for-x86_64-baseos-rpms            62 k
    krb5-server                                x86_64        1.21.1-1.el9                rhel-9-for-x86_64-baseos-rpms           309 k
    krb5-workstation                           x86_64        1.21.1-1.el9                rhel-9-for-x86_64-baseos-rpms           540 k
    libdb-utils                                x86_64        5.3.28-53.el9               rhel-9-for-x86_64-appstream-rpms        145 k
    libev                                      x86_64        4.33-5.el9                  rhel-9-for-x86_64-baseos-rpms            56 k
    libkadm5                                   x86_64        1.21.1-1.el9                rhel-9-for-x86_64-baseos-rpms            81 k
    libnfsidmap                                x86_64        1:2.5.4-20.el9              rhel-9-for-x86_64-baseos-rpms            66 k
    libnsl2                                    x86_64        2.0.0-1.el9                 rhel-9-for-x86_64-appstream-rpms         33 k
    libsss_autofs                              x86_64        2.9.1-4.el9_3.5             rhel-9-for-x86_64-baseos-rpms            43 k
    libverto-libev                             x86_64        0.3.2-3.el9                 rhel-9-for-x86_64-baseos-rpms            15 k
    lksctp-tools                               x86_64        1.0.19-2.el9                rhel-9-for-x86_64-baseos-rpms            98 k
    lua                                        x86_64        5.4.4-4.el9                 rhel-9-for-x86_64-appstream-rpms        192 k
    lua-posix                                  x86_64        35.0-8.el9                  rhel-9-for-x86_64-appstream-rpms        155 k
    mod_auth_gssapi                            x86_64        1.6.3-7.el9                 rhel-9-for-x86_64-appstream-rpms         76 k
    mod_lookup_identity                        x86_64        1.0.0-15.el9                rhel-9-for-x86_64-appstream-rpms         30 k
    mod_session                                x86_64        2.4.57-5.el9                rhel-9-for-x86_64-appstream-rpms         51 k
    mod_ssl                                    x86_64        1:2.4.57-5.el9              rhel-9-for-x86_64-appstream-rpms        113 k
    nfs-utils                                  x86_64        1:2.5.4-20.el9              rhel-9-for-x86_64-baseos-rpms           458 k
    nss-tools                                  x86_64        3.90.0-6.el9_3              rhel-9-for-x86_64-appstream-rpms        447 k
    oddjob                                     x86_64        0.34.7-7.el9                rhel-9-for-x86_64-appstream-rpms         73 k
    oddjob-mkhomedir                           x86_64        0.34.7-7.el9                rhel-9-for-x86_64-appstream-rpms         31 k
    open-sans-fonts                            noarch        1.10-16.el9                 rhel-9-for-x86_64-appstream-rpms        475 k
    openldap-clients                           x86_64        2.6.3-1.el9                 rhel-9-for-x86_64-baseos-rpms           182 k
    openssl-perl                               x86_64        1:3.0.7-25.el9_3            rhel-9-for-x86_64-appstream-rpms         43 k
    pki-jackson-annotations                    noarch        2.14.1-1.el9                rhel-9-for-x86_64-appstream-rpms         83 k
    pki-jackson-core                           noarch        2.14.1-2.el9                rhel-9-for-x86_64-appstream-rpms        446 k
    pki-jackson-databind                       noarch        2.14.1-2.el9                rhel-9-for-x86_64-appstream-rpms        1.5 M
    pki-jackson-jaxrs-json-provider            noarch        2.14.1-2.el9                rhel-9-for-x86_64-appstream-rpms         24 k
    pki-jackson-jaxrs-providers                noarch        2.14.1-2.el9                rhel-9-for-x86_64-appstream-rpms         47 k
    pki-jackson-module-jaxb-annotations        noarch        2.14.1-2.el9                rhel-9-for-x86_64-appstream-rpms         51 k
    pki-resteasy                               noarch        3.0.26-15.el9               rhel-9-for-x86_64-appstream-rpms         16 k
    pki-resteasy-client                        noarch        3.0.26-15.el9               rhel-9-for-x86_64-appstream-rpms        165 k
    pki-resteasy-core                          noarch        3.0.26-15.el9               rhel-9-for-x86_64-appstream-rpms        801 k
    pki-resteasy-jackson2-provider             noarch        3.0.26-15.el9               rhel-9-for-x86_64-appstream-rpms         31 k
    publicsuffix-list                          noarch        20210518-3.el9              rhel-9-for-x86_64-appstream-rpms         85 k
    python3-argcomplete                        noarch        1.12.0-5.el9                rhel-9-for-x86_64-appstream-rpms         71 k
    python3-augeas                             noarch        0.5.0-25.el9                rhel-9-for-x86_64-appstream-rpms         31 k
    python3-babel                              noarch        2.9.1-2.el9                 rhel-9-for-x86_64-appstream-rpms        6.0 M
    python3-cffi                               x86_64        1.14.5-5.el9                rhel-9-for-x86_64-appstream-rpms        257 k
    python3-cryptography                       x86_64        36.0.1-4.el9                rhel-9-for-x86_64-baseos-rpms           1.2 M
    python3-dns                                noarch        2.3.0-2.el9                 rhel-9-for-x86_64-baseos-rpms           469 k
    python3-gssapi                             x86_64        1.6.9-5.el9                 rhel-9-for-x86_64-appstream-rpms        489 k
    python3-idm-pki                            noarch        11.4.2-1.el9                rhel-9-for-x86_64-appstream-rpms        172 k
    python3-ipaclient                          noarch        4.10.2-8.el9_3              rhel-9-for-x86_64-appstream-rpms        651 k
    python3-ipalib                             noarch        4.10.2-8.el9_3              rhel-9-for-x86_64-appstream-rpms        674 k
    python3-ipaserver                          noarch        4.10.2-8.el9_3              rhel-9-for-x86_64-appstream-rpms        1.5 M
    python3-jinja2                             noarch        2.11.3-4.el9                rhel-9-for-x86_64-appstream-rpms        253 k
    python3-jwcrypto                           noarch        0.8-4.el9                   rhel-9-for-x86_64-appstream-rpms         76 k
    python3-kdcproxy                           noarch        1.0.0-7.el9                 rhel-9-for-x86_64-appstream-rpms         43 k
    python3-ldap                               x86_64        3.4.3-2.el9                 rhel-9-for-x86_64-appstream-rpms        259 k
    python3-lib389                             noarch        2.3.6-5.el9_3               rhel-9-for-x86_64-appstream-rpms        1.0 M
    python3-libipa_hbac                        x86_64        2.9.1-4.el9_3.5             rhel-9-for-x86_64-baseos-rpms            34 k
    python3-markupsafe                         x86_64        1.1.1-12.el9                rhel-9-for-x86_64-appstream-rpms         39 k
    python3-mod_wsgi                           x86_64        4.7.1-11.el9                rhel-9-for-x86_64-appstream-rpms        1.0 M
    python3-netaddr                            noarch        0.8.0-5.el9                 rhel-9-for-x86_64-appstream-rpms        1.6 M
    python3-netifaces                          x86_64        0.10.6-15.el9               rhel-9-for-x86_64-appstream-rpms         26 k
    python3-pyasn1                             noarch        0.4.8-6.el9                 rhel-9-for-x86_64-appstream-rpms        163 k
    python3-pyasn1-modules                     noarch        0.4.8-6.el9                 rhel-9-for-x86_64-appstream-rpms        283 k
    python3-pycparser                          noarch        2.20-6.el9                  rhel-9-for-x86_64-appstream-rpms        139 k
    python3-pytz                               noarch        2021.1-5.el9                rhel-9-for-x86_64-appstream-rpms         55 k
    python3-pyusb                              noarch        1.0.2-13.el9                rhel-9-for-x86_64-appstream-rpms         96 k
    python3-qrcode-core                        noarch        6.1-12.el9                  rhel-9-for-x86_64-appstream-rpms         61 k
    python3-sss                                x86_64        2.9.1-4.el9_3.5             rhel-9-for-x86_64-baseos-rpms            35 k
    python3-sss-murmur                         x86_64        2.9.1-4.el9_3.5             rhel-9-for-x86_64-baseos-rpms            23 k
    python3-sssdconfig                         noarch        2.9.1-4.el9_3.5             rhel-9-for-x86_64-baseos-rpms            68 k
    python3-yubico                             noarch        1.3.3-7.el9                 rhel-9-for-x86_64-appstream-rpms         73 k
    redhat-logos-httpd                         noarch        90.4-2.el9                  rhel-9-for-x86_64-appstream-rpms         18 k
    redhat-logos-ipa                           noarch        90.4-2.el9                  rhel-9-for-x86_64-appstream-rpms         20 k
    rpcbind                                    x86_64        1.2.6-5.el9                 rhel-9-for-x86_64-baseos-rpms            62 k
    slapi-nis                                  x86_64        0.60.0-5.el9_3              rhel-9-for-x86_64-appstream-rpms        153 k
    slf4j                                      noarch        1.7.30-13.el9               rhel-9-for-x86_64-appstream-rpms         73 k
    slf4j-jdk14                                noarch        1.7.30-13.el9               rhel-9-for-x86_64-appstream-rpms         19 k
    softhsm                                    x86_64        2.6.1-7.el9.2               rhel-9-for-x86_64-appstream-rpms        453 k
    sssd-dbus                                  x86_64        2.9.1-4.el9_3.5             rhel-9-for-x86_64-baseos-rpms           140 k
    sssd-idp                                   x86_64        2.9.1-4.el9_3.5             rhel-9-for-x86_64-appstream-rpms         46 k
    sssd-nfs-idmap                             x86_64        2.9.1-4.el9_3.5             rhel-9-for-x86_64-baseos-rpms            44 k
    sssd-tools                                 x86_64        2.9.1-4.el9_3.5             rhel-9-for-x86_64-baseos-rpms           182 k
    tomcat                                     noarch        1:9.0.62-37.el9_3.2         rhel-9-for-x86_64-appstream-rpms        101 k
    tomcat-el-3.0-api                          noarch        1:9.0.62-37.el9_3.2         rhel-9-for-x86_64-appstream-rpms        108 k
    tomcat-jsp-2.3-api                         noarch        1:9.0.62-37.el9_3.2         rhel-9-for-x86_64-appstream-rpms         67 k
    tomcat-lib                                 noarch        1:9.0.62-37.el9_3.2         rhel-9-for-x86_64-appstream-rpms        5.8 M
    tomcat-servlet-4.0-api                     noarch        1:9.0.62-37.el9_3.2         rhel-9-for-x86_64-appstream-rpms        286 k
    tzdata-java                                noarch        2024a-1.el9                 rhel-9-for-x86_64-appstream-rpms        234 k
    Installing weak dependencies:
    apr-util-openssl                           x86_64        1.6.1-23.el9                rhel-9-for-x86_64-appstream-rpms         17 k
    mod_http2                                  x86_64        1.15.19-5.el9               rhel-9-for-x86_64-appstream-rpms        152 k
    mod_lua                                    x86_64        2.4.57-5.el9                rhel-9-for-x86_64-appstream-rpms         62 k

    Transaction Summary
    ====================================================================================================================================
    Install  140 Packages

    Total download size: 141 M
    Installed size: 544 M
    Is this ok [y/N]: y


    [root@identity-management ~]# dnf install ipa-server ipa-server-dns
    Updating Subscription Management repositories.
    Last metadata expiration check: 0:00:08 ago on Tue 19 Mar 2024 11:14:04 PM IST.
    Package ipa-server-4.10.2-8.el9_3.x86_64 is already installed.
    Dependencies resolved.
    ====================================================================================================================================
    Package                          Architecture       Version                     Repository                                    Size
    ====================================================================================================================================
    Installing:
    ipa-server-dns                   noarch             4.10.2-8.el9_3              rhel-9-for-x86_64-appstream-rpms              53 k
    Installing dependencies:
    bind-dyndb-ldap                  x86_64             11.9-8.el9_1                rhel-9-for-x86_64-appstream-rpms             109 k
    ldns                             x86_64             1.7.1-11.el9                rhel-9-for-x86_64-appstream-rpms             163 k
    opencryptoki                     x86_64             3.21.0-9.el9_3              rhel-9-for-x86_64-baseos-rpms                207 k
    opencryptoki-icsftok             x86_64             3.21.0-9.el9_3              rhel-9-for-x86_64-baseos-rpms                150 k
    opencryptoki-libs                x86_64             3.21.0-9.el9_3              rhel-9-for-x86_64-baseos-rpms                 91 k
    opendnssec                       x86_64             2.1.10-1.el9                rhel-9-for-x86_64-appstream-rpms             462 k
    openssl-pkcs11                   x86_64             0.4.11-7.el9                rhel-9-for-x86_64-baseos-rpms                 77 k
    sqlite                           x86_64             3.34.1-7.el9_3              rhel-9-for-x86_64-appstream-rpms             749 k

    Transaction Summary
    ====================================================================================================================================
    Install  9 Packages

    Total download size: 2.0 M
    Installed size: 5.0 M
    Is this ok [y/N]: 


### Install IPA Server 

    
    [root@identity-management ~]# ipa-server-install 
    
    The log file for this installation can be found in /var/log/ipaserver-install.log
    ==============================================================================
    This program will set up the IPA Server.
    Version 4.10.2
    
    This includes:
      * Configure a stand-alone CA (dogtag) for certificate management
      * Configure the NTP client (chronyd)
      * Create and configure an instance of Directory Server
      * Create and configure a Kerberos Key Distribution Center (KDC)
      * Configure Apache (httpd)
      * Configure SID generation
      * Configure the KDC to enable PKINIT
    
    To accept the default shown in brackets, press the Enter key.
    
    Do you want to configure integrated DNS (BIND)? [no]: yes
    
    Enter the fully qualified domain name of the computer
    on which you're setting up server software. Using the form
    <hostname>.<domainname>
    Example: master.example.com
    
    
    Server host name [identity-management.ocp4.example.com]: 
    
    Warning: skipping DNS resolution of host identity-management.ocp4.example.com
    The domain name has been determined based on the host name.
    
    Please confirm the domain name [ocp4.example.com]: 
    
    The kerberos protocol requires a Realm name to be defined.
    This is typically the domain name converted to uppercase.
    
    Please provide a realm name [OCP4.EXAMPLE.COM]: 
    Certain directory server operations require an administrative user.
    This user is referred to as the Directory Manager and has full access
    to the Directory for system management tasks and will be added to the
    instance of directory server created for IPA.
    The password must be at least 8 characters long.
    
    Directory Manager password: 
    Password (confirm): 
    
    The IPA server requires an administrative user, named 'admin'.
    This user is a regular system account used for IPA server administration.
    
    IPA admin password: 
    Password (confirm): 
    
    Checking DNS domain ocp4.example.com., please wait ...
    Do you want to configure DNS forwarders? [yes]: yes
    Following DNS servers are configured in /etc/resolv.conf: 192.168.122.2, 8.8.8.8
    Do you want to configure these servers as DNS forwarders? [yes]: yes
    All detected DNS servers were added. You can enter additional addresses now:
    Enter an IP address for a DNS forwarder, or press Enter to skip: 
    DNS forwarders: 192.168.122.2, 8.8.8.8
    Checking DNS forwarders, please wait ...
    Do you want to search for missing reverse zones? [yes]: 
    Reverse record for IP address 192.168.122.2 already exists
    Trust is configured but no NetBIOS domain name found, setting it now.
    Enter the NetBIOS name for the IPA domain.
    Only up to 15 uppercase ASCII letters, digits and dashes are allowed.
    Example: EXAMPLE.
    
    
    NetBIOS domain name [OCP4]: 
    
    Do you want to configure chrony with NTP server or pool address? [no]: 192.168.122.2
    Do you want to configure chrony with NTP server or pool address? [no]: yes
    Enter NTP source server addresses separated by comma, or press Enter to skip: 192.168.122.2
    Enter a NTP source pool address, or press Enter to skip: 192.168.122.2
    
    The IPA Master Server will be configured with:
    Hostname:       identity-management.ocp4.example.com
    IP address(es): 192.168.122.2
    Domain name:    ocp4.example.com
    Realm name:     OCP4.EXAMPLE.COM
    
    The CA will be configured with:
    Subject DN:   CN=Certificate Authority,O=OCP4.EXAMPLE.COM
    Subject base: O=OCP4.EXAMPLE.COM
    Chaining:     self-signed
    
    BIND DNS server will be configured to serve IPA domain with:
    Forwarders:       192.168.122.2, 8.8.8.8
    Forward policy:   only
    Reverse zone(s):  No reverse zone
    
    NTP server:	192.168.122.2
    NTP pool:	192.168.122.2
    Continue to configure the system with these values? [no]: yes
    
    The following operations may take some minutes to complete.
    Please wait until the prompt is returned.
    
    Adding [192.168.122.2 identity-management.ocp4.example.com] to your /etc/hosts file
    Disabled p11-kit-proxy
    Synchronizing time
    Configuration of chrony was changed by installer.
    Attempting to sync time with chronyc.
    Process chronyc waitsync failed to sync time!
    Unable to sync time with chrony server, assuming the time is in sync. Please check that 123 UDP port is opened, and any time server is on network.
    Warning: IPA was unable to sync time with chrony!
             Time synchronization is required for IPA to work correctly
    Configuring directory server (dirsrv). Estimated time: 30 seconds
      [1/43]: creating directory server instance
    Validate installation settings ...
    Create file system structures ...
    Perform SELinux labeling ...
    Create database backend: dc=ocp4,dc=example,dc=com ...
    Perform post-installation tasks ...
      [2/43]: tune ldbm plugin
      [3/43]: adding default schema
      [4/43]: enabling memberof plugin
      [5/43]: enabling winsync plugin
      [6/43]: configure password logging
      [7/43]: configuring replication version plugin
      [8/43]: enabling IPA enrollment plugin
      [9/43]: configuring uniqueness plugin
      [10/43]: configuring uuid plugin
      [11/43]: configuring modrdn plugin
      [12/43]: configuring DNS plugin
      [13/43]: enabling entryUSN plugin
      [14/43]: configuring lockout plugin
      [15/43]: configuring graceperiod plugin
      [16/43]: configuring topology plugin
      [17/43]: creating indices
      [18/43]: enabling referential integrity plugin
      [19/43]: configuring certmap.conf
      [20/43]: configure new location for managed entries
      [21/43]: configure dirsrv ccache and keytab
      [22/43]: enabling SASL mapping fallback
      [23/43]: restarting directory server
      [24/43]: adding sasl mappings to the directory
      [25/43]: adding default layout
      [26/43]: adding delegation layout
      [27/43]: creating container for managed entries
      [28/43]: configuring user private groups
      [29/43]: configuring netgroups from hostgroups
      [30/43]: creating default Sudo bind user
      [31/43]: creating default Auto Member layout
      [32/43]: adding range check plugin
      [33/43]: creating default HBAC rule allow_all
      [34/43]: adding entries for topology management
      [35/43]: initializing group membership
      [36/43]: adding master entry
      [37/43]: initializing domain level
      [38/43]: configuring Posix uid/gid generation
      [39/43]: adding replication acis
      [40/43]: activating sidgen plugin
      [41/43]: activating extdom plugin
      [42/43]: configuring directory to start on boot
      [43/43]: restarting directory server
    Done configuring directory server (dirsrv).
    Configuring Kerberos KDC (krb5kdc)
      [1/11]: adding kerberos container to the directory
      [2/11]: configuring KDC
      [3/11]: initialize kerberos container
      [4/11]: adding default ACIs
      [5/11]: creating a keytab for the directory
      [6/11]: creating a keytab for the machine
      [7/11]: adding the password extension to the directory
      [8/11]: creating anonymous principal
      [9/11]: starting the KDC
      [10/11]: configuring KDC to start on boot
      [11/11]: enable PAC ticket signature support
    Done configuring Kerberos KDC (krb5kdc).
    Configuring kadmin
      [1/2]: starting kadmin 
      [2/2]: configuring kadmin to start on boot
    Done configuring kadmin.
    Configuring ipa-custodia
      [1/5]: Making sure custodia container exists
      [2/5]: Generating ipa-custodia config file
      [3/5]: Generating ipa-custodia keys
      [4/5]: starting ipa-custodia 
      [5/5]: configuring ipa-custodia to start on boot
    Done configuring ipa-custodia.
    Configuring certificate server (pki-tomcatd). Estimated time: 3 minutes
      [1/30]: configuring certificate server instance
      [2/30]: stopping certificate server instance to update CS.cfg
      [3/30]: backing up CS.cfg
      [4/30]: Add ipa-pki-wait-running
      [5/30]: secure AJP connector
      [6/30]: reindex attributes
    =-  [7/30]: exporting Dogtag certificate store pin
      [8/30]: disabling nonces
      [9/30]: set up CRL publishing
      [10/30]: enable PKIX certificate path discovery and validation
      [11/30]: authorizing RA to modify profiles
      [12/30]: authorizing RA to manage lightweight CAs
      [13/30]: Ensure lightweight CAs container exists
      [14/30]: Ensuring backward compatibility
      [15/30]: starting certificate server instance
      [16/30]: configure certmonger for renewals
      [17/30]: requesting RA certificate from CA
      [18/30]: publishing the CA certificate
      [19/30]: adding RA agent as a trusted user
      [20/30]: configure certificate renewals
      [21/30]: Configure HTTP to proxy connections
      [22/30]: updating IPA configuration
      [23/30]: enabling CA instance
      [24/30]: importing IPA certificate profiles
      [25/30]: migrating certificate profiles to LDAP
      [26/30]: adding default CA ACL
      [27/30]: adding 'ipa' CA entry
      [28/30]: Recording random serial number state
      [29/30]: configuring certmonger renewal for lightweight CAs
      [30/30]: deploying ACME service
    Done configuring certificate server (pki-tomcatd).
    Configuring directory server (dirsrv)
      [1/3]: configuring TLS for DS instance
      [2/3]: adding CA certificate entry
      [3/3]: restarting directory server
    Done configuring directory server (dirsrv).
    Configuring ipa-otpd
      [1/2]: starting ipa-otpd 
      [2/2]: configuring ipa-otpd to start on boot
    Done configuring ipa-otpd.
    Configuring the web interface (httpd)
      [1/22]: stopping httpd
      [2/22]: backing up ssl.conf
      [3/22]: disabling nss.conf
      [4/22]: configuring mod_ssl certificate paths
      [5/22]: setting mod_ssl protocol list
      [6/22]: configuring mod_ssl log directory
      [7/22]: disabling mod_ssl OCSP
      [8/22]: adding URL rewriting rules
      [9/22]: configuring httpd
    Nothing to do for configure_httpd_wsgi_conf
      [10/22]: setting up httpd keytab
      [11/22]: configuring Gssproxy
      [12/22]: setting up ssl
      [13/22]: configure certmonger for renewals
      [14/22]: publish CA cert
      [15/22]: clean up any existing httpd ccaches
      [16/22]: enable ccache sweep
      [17/22]: configuring SELinux for httpd
      [18/22]: create KDC proxy config
      [19/22]: enable KDC proxy
      [20/22]: starting httpd
      [21/22]: configuring httpd to start on boot
      [22/22]: enabling oddjobd
    Done configuring the web interface (httpd).
    Configuring Kerberos KDC (krb5kdc)
      [1/1]: installing X509 Certificate for PKINIT
    Done configuring Kerberos KDC (krb5kdc).
    Applying LDAP updates
    Upgrading IPA:. Estimated time: 1 minute 30 seconds
      [1/10]: stopping directory server
      [2/10]: saving configuration
      [3/10]: disabling listeners
      [4/10]: enabling DS global lock
      [5/10]: disabling Schema Compat
      [6/10]: starting directory server
      [7/10]: upgrading server
      [8/10]: stopping directory server
      [9/10]: restoring configuration
      [10/10]: starting directory server
    Done.
    Restarting the KDC
    dnssec-validation yes
    Configuring DNS (named)
      [1/12]: generating rndc key file
      [2/12]: adding DNS container
      [3/12]: setting up our zone
      [4/12]: setting up our own record
      [5/12]: setting up records for other masters
      [6/12]: adding NS record to the zones
      [7/12]: setting up kerberos principal
      [8/12]: setting up LDAPI autobind
      [9/12]: setting up named.conf
    created new /etc/named.conf
    created named user config '/etc/named/ipa-ext.conf'
    created named user config '/etc/named/ipa-options-ext.conf'
    created named user config '/etc/named/ipa-logging-ext.conf'
      [10/12]: setting up server configuration
      [11/12]: configuring named to start on boot
      [12/12]: changing resolv.conf to point to ourselves
    Done configuring DNS (named).
    Restarting the web server to pick up resolv.conf changes
    Configuring DNS key synchronization service (ipa-dnskeysyncd)
      [1/7]: checking status
      [2/7]: setting up bind-dyndb-ldap working directory
      [3/7]: setting up kerberos principal
      [4/7]: setting up SoftHSM
      [5/7]: adding DNSSEC containers
      [6/7]: creating replica keys
      [7/7]: configuring ipa-dnskeysyncd to start on boot
    Done configuring DNS key synchronization service (ipa-dnskeysyncd).
    Restarting ipa-dnskeysyncd
    Restarting named
    Updating DNS system records
    Configuring SID generation
      [1/8]: adding RID bases
      [2/8]: creating samba domain object
      [3/8]: adding admin(group) SIDs
      [4/8]: updating Kerberos config
    'dns_lookup_kdc' already set to 'true', nothing to do.
      [5/8]: activating sidgen task
      [6/8]: restarting Directory Server to take MS PAC and LDAP plugins changes into account
      [7/8]: adding fallback group
      [8/8]: adding SIDs to existing users and groups
    This step may take considerable amount of time, please wait..
    Done.
    Configuring client side components
    This program will set up IPA client.
    Version 4.10.2
    
    Using existing certificate '/etc/ipa/ca.crt'.
    Client hostname: identity-management.ocp4.example.com
    Realm: OCP4.EXAMPLE.COM
    DNS Domain: ocp4.example.com
    IPA Server: identity-management.ocp4.example.com
    BaseDN: dc=ocp4,dc=example,dc=com
    
    Configured /etc/sssd/sssd.conf
    Systemwide CA database updated.
    Adding SSH public key from /etc/ssh/ssh_host_ecdsa_key.pub
    Adding SSH public key from /etc/ssh/ssh_host_ed25519_key.pub
    Adding SSH public key from /etc/ssh/ssh_host_rsa_key.pub
    SSSD enabled
    Configured /etc/openldap/ldap.conf
    Configured /etc/ssh/ssh_config
    Configured /etc/ssh/sshd_config.d/04-ipa.conf
    Configuring ocp4.example.com as NIS domain.
    Client configuration complete.
    The ipa-client-install command was successful
    
    ==============================================================================
    Setup complete
    
    Next steps:
    	1. You must make sure these network ports are open:
    		TCP Ports:
    		  * 80, 443: HTTP/HTTPS
    		  * 389, 636: LDAP/LDAPS
    		  * 88, 464: kerberos
    		  * 53: bind
    		UDP Ports:
    		  * 88, 464: kerberos
    		  * 53: bind
    		  * 123: ntp
    
    	2. You can now obtain a kerberos ticket using the command: 'kinit admin'
    	   This ticket will allow you to use the IPA tools (e.g., ipa user-add)
    	   and the web user interface.
    
    Be sure to back up the CA certificates stored in /root/cacert.p12
    These files are required to create replicas. The password for these
    files is the Directory Manager password
    The ipa-server-install command was successful
    
