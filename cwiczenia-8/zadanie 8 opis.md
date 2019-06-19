Dodanie dwóch sieci w VM
-------------------
LAN1	172.22.144.0/23

LAN2	172.22.128.0/19

PC 0
-------------------
ip link show

ip link set dev enp0s3 up

ip link set dev enp0s8 up

ip link set dev enp0s9 up


apt-get install net-tools


ip addr add	172.22.144.1/23	dev	enp0s8 

ip addr add	172.22.128.1/19	dev	enp0s9



echo 1 > /proc/sys/net/ipv4/ip_forward


ip addr flush dev enp0s*


ping www.google.pl


PC 1
-----------

ip link show

ip link set dev enp0s3 up


ip addr add	172.22.144.2/23	dev	enp0s3 


pico /etc/resolv.conf

nameserver 8.8.8.8

ping www.google.pl


PC 2
-----------
ip link show

ip link set dev enp0s3 up

ip addr add	172.22.128.2/23	dev	enp0s3

pico /etc/resolv.conf

nameserver 8.8.8.8

ping www.google.pl
