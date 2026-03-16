
Computers are often connected through a network and communicate by sending packets from a source to a host destination. Linux provides commands for network configuration, testing connectivity, and troubleshooting network-related issues.

## Using Ping (Packet Internet Groper) Command

The ping command ensures a computer can communicate with a specified device of the network by sending an Internet Control Message Protocol (ICMP) Echo Request message in the form of packets to the destination computer, and then waits for a response. Once the packets are received by the destined computer, it sends the packets back. This is executed until interrupted.

The command provides details such as:
- Number of packets transmitted and received
- Time taken for the packet to return

It is generally used for:
- Measuring the time taken by the packets to determine connection speed
- Making sure that the network connection between host and destined computer can be established.

![[ping command example.png]]

## Using the nslookup command

This command is used to query DNS (Domain Name System) records. It helps retrieve the IP address of a domain name or the domain name associated with an IP address. This command is commonly used for DNS troubleshooting.

![[nslookup command example.png]]

## Using the traceroute command

The traceroute command is used to determine the path taken by packets from the source to the destination host. It also shows the number of hops required to reach the destination. 

The output displays a list of intermediate routers through which the packet travels for identifying network delays or failures.

![[traceroute command example.png]]


## Using host command

The host command is used to perform DNS lookups. It can find:

- The IP address associated with a domain name
- The domain name associated with an IP address

The returned IP address may be IPv4 or IPv6

![[host command example.png]]

## Using netstat Command

The netstat (Network Statistics) command displays information about:
- Network connections
- Routing tables
- Interface statistics
- Port status

This command works with the Linux networking subsystem and primarily displays information from the /proc/net directory.

![[netstat command example.png]]

## Using Arp Command

The ARP (Address Resolution Protocol) command is used to display and modify the ARP cache containing the mapping of IP address to MAC address. The system's TCP/IP stack uses ARP to determine the MAC address associated with an IP address.

![[arp command example.png]]

## Using the ifconfig Command

The ifconfig (interface configuration) command is used to display or configure network interfaces. It can:

- Assign IP addresses
- Configure netmasks
- Enable or disable interfaces
- Display MTU (Maximum transmission unit) values

![[Pasted image 20260316203411.png]]






