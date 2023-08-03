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