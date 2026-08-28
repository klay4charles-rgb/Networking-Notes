# Seven-Second Subnetting Technique

The **Seven-Second Subnetting Technique** is a fast method for calculating IPv4 subnets without repeatedly converting the entire address into binary.

It is especially useful when solving subnetting questions quickly in exams, labs, and networking interviews.

---

## 1. The Magic Number

The key formula is:

**Magic Number = 256 − Subnet Mask Value**

The octet where the subnet mask is **not 255 or 0** is called the **interesting octet**.

### Example

Given:

`192.168.10.0/26`

Subnet mask:

`255.255.255.192`

The interesting octet is the **4th octet**.

So:

`256 − 192 = 64`

**Magic Number = 64**

This means the subnet ranges increase by 64:

* `192.168.10.0`
* `192.168.10.64`
* `192.168.10.128`
* `192.168.10.192`

---

## 2. Finding the Subnet

Suppose we have:

`192.168.10.75/26`

The subnet mask is:

`255.255.255.192`

Magic number:

`256 − 192 = 64`

Subnet boundaries:

* 0
* 64
* 128
* 192

`75` falls between **64 and 128**.

Therefore:

**Network Address:** `192.168.10.64`

**Broadcast Address:** `192.168.10.127`

**Usable Host Range:** `192.168.10.65 – 192.168.10.126`

---

## 3. Finding the Broadcast Address

Once the network address is known:

**Next subnet − 1 = Broadcast Address**

For `192.168.10.64/26`:

Next subnet = `192.168.10.128`

Therefore:

`192.168.10.128 − 1 = 192.168.10.127`

Broadcast:

`192.168.10.127`

---

## 4. Finding Usable Hosts

For most traditional IPv4 subnets:

**First usable IP = Network + 1**

**Last usable IP = Broadcast − 1**

For:

`192.168.10.64/26`

* Network: `192.168.10.64`
* First Host: `192.168.10.65`
* Last Host: `192.168.10.126`
* Broadcast: `192.168.10.127`

---

## 5. Number of Hosts

The number of host bits is:

**32 − CIDR Prefix**

For `/26`:

`32 − 26 = 6 host bits`

Total addresses:

`2⁶ = 64`

Usable hosts:

`64 − 2 = 62`

So a `/26` provides:

**64 total addresses / 62 usable hosts**

---

## 6. The Seven-Second Method

When given an IP address and CIDR:

### Step 1 — Find the subnet mask

Example:

`/27 = 255.255.255.224`

### Step 2 — Find the interesting octet

`224` is the interesting octet.

### Step 3 — Calculate the magic number

`256 − 224 = 32`

### Step 4 — Write subnet boundaries

`0, 32, 64, 96, 128, 160, 192, 224`

### Step 5 — Find where the IP falls

For:

`192.168.1.115/27`

`115` falls between:

`96` and `128`

Therefore:

**Network:** `192.168.1.96`

**Broadcast:** `192.168.1.127`

**Usable:** `192.168.1.97 – 192.168.1.126`

---

## 7. Quick Reference — Common Magic Numbers

| CIDR | Subnet Mask     | Magic Number |
| ---- | --------------- | -----------: |
| /25  | 255.255.255.128 |          128 |
| /26  | 255.255.255.192 |           64 |
| /27  | 255.255.255.224 |           32 |
| /28  | 255.255.255.240 |           16 |
| /29  | 255.255.255.248 |            8 |
| /30  | 255.255.255.252 |            4 |

The smaller the magic number, the more subnets are created within that octet.

---

## Key Takeaways

* **Interesting octet** = the octet containing the subnet boundary.
* **Magic Number = 256 − subnet mask value** in the interesting octet.
* Subnet boundaries are multiples of the magic number.
* **Network address** = beginning of the subnet.
* **Broadcast address** = one address before the next subnet.
* **Usable range** = Network + 1 through Broadcast − 1.
* **Usable hosts** = `2^(host bits) − 2` for normal IPv4 subnets.

### Mental Shortcut

> **Mask → Interesting Octet → 256 − Mask = Magic Number → Find the nearest subnet boundary.**

This technique turns subnetting from a binary-conversion exercise into a quick arithmetic process.
