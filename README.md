usage: redhcp.py [-h] [-x EXCLUDE] [-i INCLUDE_ONLY] [-r] [-nw] [-l {CRITICAL,ERROR,WARNING,INFO,DEBUG}]

program to restart and dhcp-renew your interfaces fast, uses dhclient for dhcp

options:
  -h, --help            show this help message and exit
  -x EXCLUDE, --exclude EXCLUDE
                        exclude interfaces from being redhcped seperated by ',' .recommanded to have lo always excluded
  -i INCLUDE_ONLY, --include-only INCLUDE_ONLY
                        redhcp only the following interfaces seperated byte ','
  -r, --restart-only    set if you want the interfaces to just restart and not renew their ip
  -nw, --renew-only     set if you want the interfaces to just renew their ip and not restart
  -l {CRITICAL,ERROR,WARNING,INFO,DEBUG}, --log-level {CRITICAL,ERROR,WARNING,INFO,DEBUG}
                        set the log level of logger

    usage example:
        only restart the interfaces, don't dhcp-renew
        ./redhcp.py -r

        only renew the interface's ip, don't restart them
        ./redhcp.py -nw

        ignore lo interface (recommanded)
        ./redhcp.py -x lo

        execute for eth0 and wlan0 (don't lookup for interfaces) 
        ./redhcp.py -l eth0,wlan0
    
                                                                                                                                                                                                                                             
