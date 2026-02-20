# Lab1

Comandos usados practica 2

DHCP

su
sudo apt update
sudo apt install isc-dhcp-server
sudo nano /etc/dhcp/dhcpd.conf
subnet 192.168.253.0 netmask 255.255.255.192
range 192.168.253.11 192.168.253.6;
option domain-name "SO3";
option routers 192.168.253.1;
option broadcast-address 192.168.253.63;
ctrl+O

IP ESTATICA

nano /etc/network/interfaces
iface enp0s3 inet static
address 192.168.1.254
netmask 255.255.255.255
gateway 192.168.1.1
network 192.168.1.0
broadcast 192.168.1.255
ctrl+0

DNS 

nano /etc/network/interfaces
nano /etc/resolv.conf

nameserver 1.1.1.1
ctrl+0
/etc/init.d/networking restart
cat /etc/network/interfaces
cat /etc/resolv.conf
ping 8.8.8.8
