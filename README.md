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
