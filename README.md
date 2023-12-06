# Networking on Linux *commands*

## IP address

Check your IP address
`ifconfig`
`ip addr` or `ip addr show`
change your ip address
`sudo ifconfig eth0 192.168.1.101` 
call to dhcp server to get and asign an ip address
`sudo dhclient eth0`
you can also change your mac address ;p
`sudo ifconfig eth0 down`
`sudo ifconfig eth0 hw ether 00:00:00:11:11:11`
`sudo ifconfig eth0 up`

## ICMP

ICMP is often associated with Ping and Traceroute.
`ping google.com`

IPv4
`ping -4 google.com`
IPv6
`ping -6 google.com`

## Traceroute

To perform a traceroute on Linux (not installed by default):
`traceroute google.com`

## DNS ("Domain Name System")

To do a DNS lookup:
`dig google.com` The IP address of google.com can be seen in the ;; ANSWER SECTION.
`dig google.com ns` show the name server
`dig google.com mx` show the mail server

The Authoritative Name Server is the DNS server which is responsible for giving the definitive answer to a question. Finding authoritative name server on Linux:
`dig -t SOA google.com`

## DHCP ("Dynamic Host Configuration Protocol")

If you are curious if you are using DHCP right now you can type:
`nmcli dev status`
Your computer might have multiple network interfaces
`nmcli dev show <device>`

## ARP ("Address Resolution Protocol")

ARP, like DNS, is a protocol which resolves one address into another. Every time a system tries to communicate to an IP address which is on the LAN it will check its ARP cache to see if has recently been resolved.
You can inspect your own ARP. Simply run the command:
`arp -a`
This reveals which systems your system has recently communicated with.

## Usefull tools to explore

### nmap

### wireshark

