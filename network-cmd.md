# Networking Commands & Significance

### `ip addr`
This command is used to show IP addresses.
```bash
manav@manav-HP-Pavillion-Laptop-15-eh1xxx:~$ ip addr
1: lo: <LOOPBACK,UP,LOWER_UP> mtu 65536 qdisc noqueue state UNKNOWN group default qlen 1000
    link/loopback 00:00:00:00:00:00 brd 00:00:00:00:00:00
    inet 127.0.0.1/8 scope host lo
       valid_lft forever preferred_lft forever
    inet6 ::1/128 scope host noprefixroute 
       valid_lft forever preferred_lft forever
2: wlo1: <BROADCAST,MULTICAST,UP,LOWER_UP> mtu 1500 qdisc noqueue state UP group default qlen 1000
    link/ether 94:bb:43:39:b3:85 brd ff:ff:ff:ff:ff:ff
    altname wlp2s0
    inet 100.129.171.184/20 brd 100.129.175.255 scope global dynamic noprefixroute wlo1
       valid_lft 85945sec preferred_lft 85945sec
    inet6 fe80::fdd5:4307:7dfc:897f/64 scope link noprefixroute 
       valid_lft forever preferred_lft forever
3: docker0: <NO-CARRIER,BROADCAST,MULTICAST,UP> mtu 1500 qdisc noqueue state DOWN group default 
    link/ether 56:53:54:dd:be:6b brd ff:ff:ff:ff:ff:ff
    inet 172.17.0.1/16 brd 172.17.255.255 scope global docker0
       valid_lft forever preferred_lft forever
    inet6 fe80::5453:54ff:fedd:be6b/64 scope link 
       valid_lft forever preferred_lft forever
```

### `ifconfig`
This cmd is used to show network interface configuration.
```bash
manav@manav-HP-Pavillion-Laptop-15-eh1xxx:~$ ifconfig 
docker0: flags=4099<UP,BROADCAST,MULTICAST>  mtu 1500
        inet 172.17.0.1  netmask 255.255.0.0  broadcast 172.17.255.255
        inet6 fe80::5453:54ff:fedd:be6b  prefixlen 64  scopeid 0x20<link>
        ether 56:53:54:dd:be:6b  txqueuelen 0  (Ethernet)
        RX packets 82  bytes 12230 (12.2 KB)
        RX errors 0  dropped 0  overruns 0  frame 0
        TX packets 114  bytes 14120 (14.1 KB)
        TX errors 0  dropped 53 overruns 0  carrier 0  collisions 0

lo: flags=73<UP,LOOPBACK,RUNNING>  mtu 65536
        inet 127.0.0.1  netmask 255.0.0.0
        inet6 ::1  prefixlen 128  scopeid 0x10<host>
        loop  txqueuelen 1000  (Local Loopback)
        RX packets 5552  bytes 707921 (707.9 KB)
        RX errors 0  dropped 0  overruns 0  frame 0
        TX packets 5552  bytes 707921 (707.9 KB)
        TX errors 0  dropped 0 overruns 0  carrier 0  collisions 0

wlo1: flags=4163<UP,BROADCAST,RUNNING,MULTICAST>  mtu 1500
        inet 100.129.171.184  netmask 255.255.240.0  broadcast 100.129.175.255
        inet6 fe80::fdd5:4307:7dfc:897f  prefixlen 64  scopeid 0x20<link>
        ether 94:bb:43:39:b3:85  txqueuelen 1000  (Ethernet)
        RX packets 275777  bytes 204131322 (204.1 MB)
        RX errors 0  dropped 709  overruns 0  frame 0
        TX packets 49643  bytes 24831737 (24.8 MB)
        TX errors 0  dropped 72 overruns 0  carrier 0  collisions 0

```

### `hostname`
this cmd is used to display the system's hostname.
```bash
manav@manav-HP-Pavillion-Laptop-15-eh1xxx:~$ hostname
 manav-HP-Pavillion-Laptop-15-eh1xxx
```

### `whoami`
this cmd is used to display the current user.
```bash
manav@manav-HP-Pavillion-Laptop-15-eh1xxx:~$ whoami
 manav
```

### `ping <n/w url>`
this cmd is used to test n/w connectivity.
```bash
manav@manav-HP-Pavillion-Laptop-15-eh1xxx:~$ ping www.scaler.com
PING www.scaler.com (108.158.61.25) 56(84) bytes of data.
64 bytes from server-108-158-61-25.bom78.r.cloudfront.net (108.158.61.25): icmp_seq=1 ttl=248 time=291 ms
64 bytes from server-108-158-61-25.bom78.r.cloudfront.net (108.158.61.25): icmp_seq=2 ttl=248 time=117 ms
64 bytes from server-108-158-61-25.bom78.r.cloudfront.net (108.158.61.25): icmp_seq=3 ttl=248 time=27.1 ms
64 bytes from server-108-158-61-25.bom78.r.cloudfront.net (108.158.61.25): icmp_seq=4 ttl=248 time=63.7 ms
64 bytes from server-108-158-61-25.bom78.r.cloudfront.net (108.158.61.25): icmp_seq=5 ttl=248 time=83.7 ms
64 bytes from server-108-158-61-25.bom78.r.cloudfront.net (108.158.61.25): icmp_seq=6 ttl=248 time=155 ms
64 bytes from server-108-158-61-25.bom78.r.cloudfront.net (108.158.61.25): icmp_seq=7 ttl=248 time=57.3 ms
64 bytes from server-108-158-61-25.bom78.r.cloudfront.net (108.158.61.25): icmp_seq=8 ttl=248 time=131 ms
64 bytes from server-108-158-61-25.bom78.r.cloudfront.net (108.158.61.25): icmp_seq=9 ttl=248 time=28.4 ms
64 bytes from server-108-158-61-25.bom78.r.cloudfront.net (108.158.61.25): icmp_seq=10 ttl=248 time=301 ms
64 bytes from server-108-158-61-25.bom78.r.cloudfront.net (108.158.61.25): icmp_seq=11 ttl=248 time=120 ms
64 bytes from server-108-158-61-25.bom78.r.cloudfront.net (108.158.61.25): icmp_seq=12 ttl=248 time=145 ms
64 bytes from server-108-158-61-25.bom78.r.cloudfront.net (108.158.61.25): icmp_seq=13 ttl=248 time=25.4 ms
64 bytes from server-108-158-61-25.bom78.r.cloudfront.net (108.158.61.25): icmp_seq=14 ttl=248 time=293 ms
64 bytes from server-108-158-61-25.bom78.r.cloudfront.net (108.158.61.25): icmp_seq=15 ttl=248 time=285 ms
64 bytes from server-108-158-61-25.bom78.r.cloudfront.net (108.158.61.25): icmp_seq=16 ttl=248 time=35.3 ms
64 bytes from server-108-158-61-25.bom78.r.cloudfront.net (108.158.61.25): icmp_seq=17 ttl=248 time=113 ms
64 bytes from server-108-158-61-25.bom78.r.cloudfront.net (108.158.61.25): icmp_seq=18 ttl=248 time=38.2 ms
64 bytes from server-108-158-61-25.bom78.r.cloudfront.net (108.158.61.25): icmp_seq=19 ttl=248 time=88.6 ms
64 bytes from server-108-158-61-25.bom78.r.cloudfront.net (108.158.61.25): icmp_seq=20 ttl=248 time=28.7 ms
64 bytes from server-108-158-61-25.bom78.r.cloudfront.net (108.158.61.25): icmp_seq=21 ttl=248 time=25.2 ms
64 bytes from server-108-158-61-25.bom78.r.cloudfront.net (108.158.61.25): icmp_seq=22 ttl=248 time=54.2 ms
64 bytes from server-108-158-61-25.bom78.r.cloudfront.net (108.158.61.25): icmp_seq=23 ttl=248 time=277 ms
64 bytes from server-108-158-61-25.bom78.r.cloudfront.net (108.158.61.25): icmp_seq=24 ttl=248 time=312 ms
64 bytes from server-108-158-61-25.bom78.r.cloudfront.net (108.158.61.25): icmp_seq=25 ttl=248 time=256 ms
64 bytes from server-108-158-61-25.bom78.r.cloudfront.net (108.158.61.25): icmp_seq=26 ttl=248 time=464 ms
64 bytes from server-108-158-61-25.bom78.r.cloudfront.net (108.158.61.25): icmp_seq=27 ttl=248 time=25.1 ms
64 bytes from server-108-158-61-25.bom78.r.cloudfront.net (108.158.61.25): icmp_seq=28 ttl=248 time=84.6 ms
64 bytes from server-108-158-61-25.bom78.r.cloudfront.net (108.158.61.25): icmp_seq=29 ttl=248 time=151 ms
64 bytes from server-108-158-61-25.bom78.r.cloudfront.net (108.158.61.25): icmp_seq=30 ttl=248 time=63.4 ms
64 bytes from server-108-158-61-25.bom78.r.cloudfront.net (108.158.61.25): icmp_seq=31 ttl=248 time=295 ms
64 bytes from server-108-158-61-25.bom78.r.cloudfront.net (108.158.61.25): icmp_seq=32 ttl=248 time=66.9 ms
64 bytes from server-108-158-61-25.bom78.r.cloudfront.net (108.158.61.25): icmp_seq=33 ttl=248 time=56.3 ms
64 bytes from server-108-158-61-25.bom78.r.cloudfront.net (108.158.61.25): icmp_seq=34 ttl=248 time=49.4 ms
64 bytes from server-108-158-61-25.bom78.r.cloudfront.net (108.158.61.25): icmp_seq=35 ttl=248 time=180 ms
^C
--- www.scaler.com ping statistics ---
35 packets transmitted, 35 received, 0% packet loss, time 34050ms
rtt min/avg/max/mdev = 25.069/136.771/464.402/112.312 ms

```

### `nslookup <n/w url>`
this cmd is used to query the DNS information.
```bash
manav@manav-HP-Pavillion-Laptop-15-eh1xxx:~$ nslookup www.google.com
;; communications error to 127.0.0.53#53: timed out
;; communications error to 127.0.0.53#53: timed out
Server:		127.0.0.53
Address:	127.0.0.53#53

Non-authoritative answer:
Name:	www.google.com
Address: 142.251.152.119
Name:	www.google.com
Address: 142.251.157.119
Name:	www.google.com
Address: 142.251.155.119
Name:	www.google.com
Address: 142.251.154.119
Name:	www.google.com
Address: 142.251.156.119
Name:	www.google.com
Address: 142.251.151.119
Name:	www.google.com
Address: 142.251.150.119
Name:	www.google.com
Address: 142.251.153.119
Name:	www.google.com
Address: 2001:4860:4828:7700::
Name:	www.google.com
Address: 2001:4860:482b:7700::
Name:	www.google.com
Address: 2001:4860:482d:7700::
Name:	www.google.com
Address: 2001:4860:4826:7700::
Name:	www.google.com
Address: 2001:4860:482a:7700::
Name:	www.google.com
Address: 2001:4860:4829:7700::
Name:	www.google.com
Address: 2001:4860:482c:7700::
Name:	www.google.com
Address: 2001:4860:4827:7700::
```

### `curl <n/w url>`
this cmd is used to transfer data from or to a server.
```html
manav@manav-HP-Pavillion-Laptop-15-eh1xxx:~$ curl http://localhost:80
<!DOCTYPE html>
<html>
<head>
<title>Welcome to nginx!</title>
<style>
html { color-scheme: light dark; }
body { width: 35em; margin: 0 auto;
font-family: Tahoma, Verdana, Arial, sans-serif; }
</style>
</head>
<body>
<h1>Welcome to nginx!</h1>
<p>If you see this page, nginx is successfully installed and working.
Further configuration is required for the web server, reverse proxy, 
API gateway, load balancer, content cache, or other features.</p>

<p>For online documentation and support please refer to
<a href="https://nginx.org/">nginx.org</a>.<br/>
To engage with the community please visit
<a href="https://community.nginx.org/">community.nginx.org</a>.<br/>
For enterprise grade support, professional services, additional 
security features and capabilities please refer to
<a href="https://f5.com/nginx">f5.com/nginx</a>.</p>

<p><em>Thank you for using nginx.</em></p>
</body>
</html>

```

### `ss -tuln`
this command is used to list open ports and connections.
```bash
manav@manav-HP-Pavillion-Laptop-15-eh1xxx:~$ ss -tuln
Netid          State           Recv-Q          Send-Q                     Local Address:Port                      Peer Address:Port          Process          
udp            UNCONN          0               0                                0.0.0.0:60371                          0.0.0.0:*                              
udp            UNCONN          0               0                                0.0.0.0:5353                           0.0.0.0:*                              
udp            UNCONN          0               0                             127.0.0.54:53                             0.0.0.0:*                              
udp            UNCONN          0               0                          127.0.0.53%lo:53                             0.0.0.0:*                              
udp            UNCONN          0               0                                   [::]:42129                             [::]:*                              
udp            UNCONN          0               0                                   [::]:5353                              [::]:*                              
tcp            LISTEN          0               511                            127.0.0.1:33575                          0.0.0.0:*                              
tcp            LISTEN          0               4096                           127.0.0.1:631                            0.0.0.0:*                              
tcp            LISTEN          0               70                             127.0.0.1:33060                          0.0.0.0:*                              
tcp            LISTEN          0               4096                       127.0.0.53%lo:53                             0.0.0.0:*                              
tcp            LISTEN          0               151                            127.0.0.1:3306                           0.0.0.0:*                              
tcp            LISTEN          0               4096                          127.0.0.54:53                             0.0.0.0:*                              
tcp            LISTEN          0               4096                             0.0.0.0:80                             0.0.0.0:*                              
tcp            LISTEN          0               511                                    *:27121                                *:*                              
tcp            LISTEN          0               4096                               [::1]:631                               [::]:*                              
tcp            LISTEN          0               4096                                [::]:80                                [::]:*     
```

### `traceroute <host url>`
this cmd is used to trace the route/path n/w packets take to reach the host n/w.
```bash
manav@manav-HP-Pavillion-Laptop-15-eh1xxx:~$ traceroute www.google.com
traceroute to www.google.com (142.251.152.119), 64 hops max
  1   100.129.160.1  7.700ms  3.196ms  3.093ms 
  2   202.131.133.5  6.403ms  6.508ms  3.271ms 
  3   115.117.125.189  6.479ms  6.651ms  * 
  4   *  *  * 
  5   115.112.15.114  21.139ms  33.895ms  8.874ms 
  6   142.251.152.119  38.066ms  11.429ms  8.871ms 
```