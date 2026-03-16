
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

This command is used to query DNS (Domain Name System) recr
