# Local Area Network (LAN)
- Let say we have 3 computers and a printer. In order for us to connect the computers and the printer together we will need "Ethernet Switch"
- Ethernet Switch is a physical network device with a bunch of ports on it
- It can be a WiFi as well
- That is the purpose of the local area network

# NIC - Network Interface Card
- usually built in in your computer. 
- This will connect to the ethernet switch.

# MAC - Media Access Control Address
- Every computer has it's own unique MAC 
- This is hardcoded in the Network Interface Card
- Physical Address is the MAC Address. 

PS C:\Users> ipconfig /all

Windows IP Configuration


Ethernet adapter Ethernet 2:

   Connection-specific DNS Suffix  . : lhric.org
   Link-local IPv6 Address . . . . . : fe80::9ecb:2782:38fc:fef3%9
   Link-local IPv6 Address . . . . . : fe80::b207:468f:4cc7:2ece%9
   IPv4 Address. . . . . . . . . . . : 10.2.14.232
   Subnet Mask . . . . . . . . . . . : 255.255.255.0
   Default Gateway . . . . . . . . . : ::

Ethernet adapter Ethernet:

   Media State . . . . . . . . . . . : Media disconnected
   Connection-specific DNS Suffix  . : swboces.lhric.local

Wireless LAN adapter Local Area Connection* 1:

   Media State . . . . . . . . . . . : Media disconnected
   Connection-specific DNS Suffix  . :

Wireless LAN adapter Local Area Connection* 2:

   Media State . . . . . . . . . . . : Media disconnected
   Connection-specific DNS Suffix  . : 

Wireless LAN adapter Wi-Fi:

   Connection-specific DNS Suffix  . :
   Link-local IPv6 Address . . . . . : fe80::3c4:aeb2:ad93:7b7%16
   IPv4 Address. . . . . . . . . . . : 192.168.1.134
   Subnet Mask . . . . . . . . . . . : 255.255.255.0
   Default Gateway . . . . . . . . . : 192.168.1.1

Ethernet adapter Bluetooth Network Connection:

   Media State . . . . . . . . . . . : Media disconnected
   Connection-specific DNS Suffix  . :

# If the computer MAC1 wants to communicate with MAC3
- The ethernet frame 
- The frame is the Payload - All of the data that is document or data has been created
- Typically the frame has Payload, Dest MAC, Source MAC
- Think of the Envelope how you put the address. 

# Summary
- LAN = Local Area Network
- Ethernet is used to connect LAN devices
- Every NIC (Network Interface Card) has a unique MAC (Media Access Control) address.
- To find it use command prompt PC: ipconfic /all or Mac users ifconfig /all

# Hub, Bridges and Switches
- Hub isn't gret since it cast to all the MACs, collision happens way too often
- A hub is a collision domain
- A bridge help fixes the collision, breaks it in half aka switch.
- Current we use the swich now which has it's own port for only that collision

# Broadcast 
- A switch is a broadcast domain
- More devices = more broadcast traffic
- More devices = larger MAC table
- A router is used to break up L2 broadcasr domains


# Summary
- Unicast is one-to-one
- Hubs are dumb
- Switches have MAC Tables
- L2 segments = broadcast domain
- Routers break up broadcast domains

# Bum Traffic
- Broadcast Unknown Unicast and Multi-cast
- IP Addresss - we can control and we assign it to this machine. It is similar to the phone number, it is unique
- ARP Request: Broadcast to discover MAC associated with an IP Address. This is a layer 2 Ethernet broadcast, used to discover a MAC address associated with the particular IP Address. It then broadcasts to every port with the right IP Address and it will respond back with the MAC address, hence ARP Response
- ARP Table is basically a table full of the connection association.
- If you want to find out the ARP Table -> Command Line -> arp -a
- Unknown Unicast - the switch port doesn't know which MAC address is on. The switch will respond with the unknown and send out to all switches. 
- Multicast - Sent to members of a group, Multi-destination traffic
# Summary
- Unique IP Address per machine - Layer 3 unique address. 
- ARP requests are L2 broadcasts
- Unknown unicast - If a switch doesn't know how to get traffic to a certain MAC addrress, it will issue and unknown unicast to ascertain the correct destination MAC. 
- Multicast - A single source sens a multicast in order to reach a group of specific recipients. 


# Router
- When the network gets larger it cn be problematic when we broadcast to too many switches
- Break up the llayer 2 broadcast domain by using the router
- We have to break it down to a smaller ethernet network, this is when a router comes in. 
- Router - is a machinne that connects between the switches
- Router breaks each switch into a segment, Segment 1 - 10.1.1x /24 Segment2 - 10.1.2x /24
- Will cut the broadcast in half and so does the MAC address table
- There is a default gateway that the router knows what to do with it so it can connect to the destination computer. 

# Summary
- Routers break up the L2 network
- Each L2 segment has a subnet
- Routers do not pass L2 broadcasts


