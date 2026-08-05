# Classful Subnetting Summary

Classful subnetting is the process of dividing an IPv4 network into smaller subnetworks. The class of an IP address is determined by its first octet.

## IPv4 Address Classes

| Class   | First Octet Range | Default Subnet Mask | Default Prefix |
| ------- | ----------------- | ------------------- | -------------- |
| Class A | 1–126             | 255.0.0.0           | /8             |
| Class B | 128–191           | 255.255.0.0         | /16            |
| Class C | 192–223           | 255.255.255.0       | /24            |

The range 127.x.x.x is reserved for loopback testing.

## Values to Determine

When an IP address and prefix are given, determine:

* **Class:** Found using the first octet.
* **Classful network:** The original network based on the default mask of the class.
* **Subnet or network address:** The first address in the subnet.
* **First usable host:** The network address plus 1.
* **Last usable host:** The broadcast address minus 1.
* **Broadcast address:** The final address in the subnet.

## How to Calculate the Subnet

1. Identify the address class using the first octet.

2. Convert the prefix into a subnet mask.

3. Find the interesting octet, which is the subnet mask octet that is not 255 or 0.

4. Calculate the block size:

   Block size = 256 − subnet mask value

5. List the subnet ranges using the block size.

6. Find the subnet range containing the given IP address.

7. Determine the network, first host, last host and broadcast addresses.

## Example

Given IP address: **192.168.10.77/26**

The first octet is 192, so it is a **Class C** address.

* Default mask: 255.255.255.0
* Subnet mask for /26: 255.255.255.192
* Block size: 256 − 192 = 64

The subnet ranges are:

* 0–63
* 64–127
* 128–191
* 192–255

The value 77 falls in the 64–127 subnet.

| Address Information | Value           |
| ------------------- | --------------- |
| Class               | Class C         |
| Classful network    | 192.168.10.0/24 |
| Network address     | 192.168.10.64   |
| First usable host   | 192.168.10.65   |
| Last usable host    | 192.168.10.126  |
| Broadcast address   | 192.168.10.127  |

## Useful Formulas

* Host bits = 32 − prefix length
* Usable hosts = 2^(host bits) − 2
* First usable host = network address + 1
* Last usable host = broadcast address − 1
* Broadcast address = the address immediately before the next subnet

Classful addressing is mainly used for learning because modern networks use CIDR. However, understanding Classes A, B and C makes subnetting easier to understand.

