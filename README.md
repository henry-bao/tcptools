# tcptools

## Ping

```bash
henry@HENRYPC:~$ ping www.google.com
PING www.google.com (142.250.217.100) 56(84) bytes of data.
64 bytes from sea09s30-in-f4.1e100.net (142.250.217.100): icmp_seq=1 ttl=117 time=3.66 ms
64 bytes from sea09s30-in-f4.1e100.net (142.250.217.100): icmp_seq=2 ttl=117 time=3.06 ms
64 bytes from sea09s30-in-f4.1e100.net (142.250.217.100): icmp_seq=3 ttl=117 time=2.47 ms
64 bytes from sea09s30-in-f4.1e100.net (142.250.217.100): icmp_seq=4 ttl=117 time=3.04 ms
64 bytes from sea09s30-in-f4.1e100.net (142.250.217.100): icmp_seq=5 ttl=117 time=3.25 ms
--- www.google.com ping statistics ---
5 packets transmitted, 5 received, 0% packet loss, time 4005ms
rtt min/avg/max/mdev = 2.466/3.094/3.655/0.384 ms
```

```bash
henry@HENRYPC:~$ ping www.microsoft.com
PING e13678.dscb.akamaiedge.net (23.36.53.236) 56(84) bytes of data.
64 bytes from a23-36-53-236.deploy.static.akamaitechnologies.com (23.36.53.236): icmp_seq=1 ttl=55 time=2.86 ms
64 bytes from a23-36-53-236.deploy.static.akamaitechnologies.com (23.36.53.236): icmp_seq=2 ttl=55 time=3.38 ms
64 bytes from a23-36-53-236.deploy.static.akamaitechnologies.com (23.36.53.236): icmp_seq=3 ttl=55 time=2.67 ms
64 bytes from a23-36-53-236.deploy.static.akamaitechnologies.com (23.36.53.236): icmp_seq=4 ttl=55 time=3.21 ms
64 bytes from a23-36-53-236.deploy.static.akamaitechnologies.com (23.36.53.236): icmp_seq=5 ttl=55 time=2.93 ms
--- e13678.dscb.akamaiedge.net ping statistics ---
5 packets transmitted, 5 received, 0% packet loss, time 4006ms
rtt min/avg/max/mdev = 2.673/3.008/3.376/0.251 ms
```

```bash
henry@HENRYPC:~$ ping www.amazon.com
PING d3ag4hukkh62yn.cloudfront.net (13.224.30.153) 56(84) bytes of data.
64 bytes from server-13-224-30-153.sea19.r.cloudfront.net (13.224.30.153): icmp_seq=1 ttl=247 time=2.76 ms
64 bytes from server-13-224-30-153.sea19.r.cloudfront.net (13.224.30.153): icmp_seq=2 ttl=247 time=3.47 ms
64 bytes from server-13-224-30-153.sea19.r.cloudfront.net (13.224.30.153): icmp_seq=3 ttl=247 time=2.53 ms
64 bytes from server-13-224-30-153.sea19.r.cloudfront.net (13.224.30.153): icmp_seq=4 ttl=247 time=3.34 ms
64 bytes from server-13-224-30-153.sea19.r.cloudfront.net (13.224.30.153): icmp_seq=5 ttl=247 time=3.04 ms
--- d3ag4hukkh62yn.cloudfront.net ping statistics ---
5 packets transmitted, 5 received, 0% packet loss, time 4006ms
rtt min/avg/max/mdev = 2.528/3.029/3.467/0.350 ms
```

1. The minimum/average/maximum/standard deviation (stdev) statistics for each are:

   - www.google.com: min/avg/max/stdev = 2.466/3.094/3.655/0.384 ms
   - www.microsoft.com: min/avg/max/stdev = 2.673/3.008/3.376/0.251 ms
   - www.amazon.com: min/avg/max/stdev = 2.528/3.029/3.467/0.350 ms
2. There was no packet loss on any of the pings.
3. The IP address did not change for any of the websites between the pings.

## Tracert

```bash
henry@HENRYPC:~$ traceroute www.amazon.com
traceroute to www.amazon.com (13.224.30.153), 30 hops max, 60 byte packets
 1  HENRYPC.mshome.net (172.24.64.1)  0.183 ms  0.173 ms  0.167 ms
 2  modem.domain (192.168.0.1)  0.840 ms  1.836 ms  1.003 ms
 3  75-172-192-254.tukw.qwest.net (75.172.192.254)  6.376 ms  7.443 ms  7.148 ms
 4  63-226-198-73.tukw.qwest.net (63.226.198.73)  4.025 ms  4.801 ms  4.906 ms
 5  99.82.182.74 (99.82.182.74)  5.057 ms  4.985 ms  6.521 ms
 6  52.95.55.219 (52.95.55.219)  6.756 ms 52.95.55.209 (52.95.55.209)  5.959 ms 52.95.55.219 (52.95.55.219)  6.213 ms
 7  205.251.225.21 (205.251.225.21)  6.268 ms 205.251.225.35 (205.251.225.35)  5.899 ms 205.251.225.49 (205.251.225.49)  6.079 ms
 8  * * *
 9  * * *
10  * * *
11  * * *
12  * * *
13  server-13-224-30-153.sea19.r.cloudfront.net (13.224.30.153)  3.672 ms  3.421 ms  3.238 ms
```

```bash
henry@HENRYPC:~$ traceroute www.google.com
traceroute to www.google.com (142.250.217.100), 30 hops max, 60 byte packets
 1  HENRYPC.mshome.net (172.24.64.1)  0.120 ms  0.107 ms  0.142 ms
 2  modem.domain (192.168.0.1)  0.940 ms  2.373 ms  1.490 ms
 3  75-172-192-254.tukw.qwest.net (75.172.192.254)  4.686 ms  4.326 ms  4.116 ms
 4  63-226-198-73.tukw.qwest.net (63.226.198.73)  3.991 ms  4.645 ms  5.984 ms
 5  * * *
 6  * 142.250.167.78 (142.250.167.78)  5.366 ms  5.357 ms
 7  * * *
 8  142.251.55.198 (142.251.55.198)  4.035 ms 142.251.50.242 (142.251.50.242)  4.488 ms 74.125.243.177 (74.125.243.177)  5.168 ms
 9  142.251.55.203 (142.251.55.203)  3.372 ms 74.125.243.179 (74.125.243.179)  8.521 ms 74.125.243.194 (74.125.243.194)  3.579 ms
10  108.170.245.113 (108.170.245.113)  3.361 ms 108.170.245.97 (108.170.245.97)  4.696 ms 108.170.245.113 (108.170.245.113)  3.450 ms
11  sea09s30-in-f4.1e100.net (142.250.217.100)  3.192 ms 142.251.55.203 (142.251.55.203)  3.416 ms sea09s30-in-f4.1e100.net (142.250.217.100)  2.334 ms
```

```bash
henry@HENRYPC:~$ traceroute www.microsoft.com
traceroute to www.microsoft.com (23.44.161.156), 30 hops max, 60 byte packets
 1  HENRYPC.mshome.net (172.24.64.1)  0.193 ms  0.181 ms  0.175 ms
 2  modem.domain (192.168.0.1)  1.757 ms  1.228 ms  2.447 ms
 3  75-172-192-254.tukw.qwest.net (75.172.192.254)  4.894 ms  4.816 ms  5.450 ms
 4  63-226-198-73.tukw.qwest.net (63.226.198.73)  13.217 ms  13.142 ms  4.174 ms
 5  * * *
 6  4.69.219.206 (4.69.219.206)  27.464 ms  26.897 ms 4.69.219.210 (4.69.219.210)  5.633 ms
 7  4.53.158.126 (4.53.158.126)  4.826 ms  5.173 ms  4.661 ms
 8  ae13.digfort-sea2.netarch.akamai.com (23.203.145.161)  13.632 ms  11.959 ms  11.413 ms
 9  a23-44-161-156.deploy.static.akamaitechnologies.com (23.44.161.156)  2.792 ms  2.666 ms  2.535 ms
 ```

1. Target server's IP address:
   - www.amazon.com: 13.224.30.153
   - www.google.com: 142.250.217.100
   - www.microsoft.com: 23.44.161.156

2. Number of hops needed to reach the target:
   - www.amazon.com: 13 hops
   - www.google.com: 11 hops
   - www.microsoft.com: 9 hops
   - Yes, ISP can be identified from the intermediate server DNS names. It appears to be Qwest, as seen in the DNS names like "tukw.qwest.net".

3. The class of IP address for each major step in the trip:
   - www.amazon.com:
     - HENRYPC.mshome.net (172.24.64.1) - Class B
     - modem.domain (192.168.0.1) - Class C
     - server-13-224-30-153.sea19.r.cloudfront.net (13.224.30.153) - Class A
   - www.google.com:
     - HENRYPC.mshome.net (172.24.64.1) - Class B
     - modem.domain (192.168.0.1) - Class C
     - sea09s30-in-f4.1e100.net (142.250.217.100) - Class B
   - www.microsoft.com:
     - HENRYPC.mshome.net (172.24.64.1) - Class B
     - modem.domain (192.168.0.1) - Class C
     - a23-44-161-156.deploy.static.akamaitechnologies.com (23.44.161.156) - Class A
