IPv4 Addresses (Professor Messer) – GitHub Notes
IPv4 Basics
Every device on a network requires a unique IPv4 address to communicate.
IPv4 addresses operate at OSI Layer 3 (Network Layer).
An IPv4 address identifies both the network and the host.
Subnet Mask

Example: 255.255.255.0

Determines which subnet (network) a device belongs to.
Used by the local device to decide whether traffic is local or must be sent to a router.
The subnet mask is not usually transmitted across the network.
Network administrators frequently need to know the subnet mask when configuring devices.
Default Gateway

Example: 192.168.1.1

The router's IP address on the local subnet.
Allows devices to communicate outside their local network.
The default gateway must be on the same subnet as the device.
Special IPv4 Addresses
Loopback Address
Used to communicate with your own device.
Address range:
127.0.0.1 – 127.255.255.254
Commonly used for testing network software and services.
Often referred to as localhost.
Reserved Addresses (Class E)
Reserved for future use, research, and testing.
Address range:
240.0.0.1 – 254.255.255.254
Not used for normal network communication.
Virtual IP (VIP)
An IP address not tied to a physical network adapter.
Common uses:
Virtual Machines (VMs)
Load Balancers
Internal router interfaces
High-availability systems
DHCP (Dynamic Host Configuration Protocol)
Automatically assigns IPv4 addresses to devices.
Eliminates the need for manual IP configuration.
Also provides:
IP Address
Subnet Mask
Default Gateway
DNS Server information
APIPA (Automatic Private IP Addressing)

Also known as Link-Local Addressing.

Used when a device cannot reach a DHCP server.
Devices automatically assign themselves an address.
Can only communicate with other devices on the same local network.
Routers do not forward APIPA traffic.
APIPA Range

169.254.0.1 – 169.254.255.254

Note: The last 256 addresses (169.254.255.0/24) are reserved and cannot be assigned to hosts.

How APIPA Works
DHCP request fails.
Device randomly selects an APIPA address.
Uses ARP (Address Resolution Protocol) to verify the address isn't already in use.
If unused, the device assigns itself that address.
The IPv4 Address Exhaustion Problem

IPv4 provides approximately 4.3 billion unique addresses.

As the Internet grew:

The number of connected devices increased rapidly.
IP address allocations became inefficient.
Many organizations owned large unused address blocks.
Address ranges were often non-contiguous, making management difficult.
Eventually, the pool of available public IPv4 addresses became exhausted.
Private IPv4 Addresses

Private IP addresses help conserve public IPv4 addresses.

Benefits
Allows organizations to build large internal networks.
Improves scalability.
Reduces the number of required public IP addresses.
Key Points
Private IP addresses are not routable on the Internet.
They can be routed internally within private networks.
Communication with the Internet requires NAT (Network Address Translation).
Key Takeaways
Every network device requires a unique IPv4 address.
Subnet masks identify the local network.
The default gateway connects devices to other networks.
DHCP automatically assigns network settings.
APIPA provides temporary addressing when DHCP is unavailable.
Loopback, Reserved, and Virtual IPs each serve specialized purposes.
Private IP addresses combined with NAT help mitigate IPv4 address exhaustion.
