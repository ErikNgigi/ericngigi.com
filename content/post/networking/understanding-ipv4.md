---
title: "Networking Fundamentals"
summary: "Networking fundamentals provide the essential building blocks for understanding and navigating the complex world of computer networks. This exploration of foundational concepts, protocols, and technologies lays the groundwork for effective communication, data exchange, and connectivity in the digital age. Dive into the core principles of networking to gain a deeper understanding of how information flows across interconnected devices, enabling the seamless operation of the modern interconnected world."
subtitle: "Building the Foundation: Exploring Networking Fundamentals"
date: 2023-10-04
author: "Eric Ngigi"
tags: ["Networking", "Tutorial"]
---

# Understanding IPv4 and the Basics of IPv4 Addresses
In the world of networking, the Internet Protocol (IP) is the backbone that enables devices to communicate and share data across the global network. One of the most well-known versions of the IP is IPv4, which stands for Internet Protocol Version 4. In this article, we'll explore what IPv4 is and delve into the fundamentals of IPv4 addresses.

## IPv4 Address: The Digital Identifiers
The cornerstone of IPv4 is the IP address, a 32-bit numerical label that uniquely identifies a device on a network. IPv4 addresses are typically written in a format known as "dotted-decimal notation," where four octets (sets of 8 bits) are separated by periods (dots). For example, an IPv4 address might look like "192.168.1.1."

- **32-bit Addressing**: IPv4 addresses consist of 32 bits, divided into four octets. Each octet can represent a value from 0 to 255, making a total of over four billion unique IPv4 addresses possible.
- **Network and Host Identification**: In an IPv4 address, the first part (the leftmost octets) identifies the network, while the last part (the rightmost octet) identifies the specific device, or host, within that network. This separation is crucial for routing data across the internet.
- **Address Classes**: IPv4 addresses are categorized into five classes—A, B, C, D, and E—based on the range of values in the first octet. Each class has its own characteristics, address ranges, and default subnet masks, tailored to different network sizes and requirements.
- **Subnetting**: IPv4 supports subnetting, a technique that allows network administrators to divide a larger IP address range into smaller subnetworks. Subnetting enhances network management, security, and efficiency.

## IPv4 Address Format
IPv4 addresses are represented as four decimal numbers separated by dots, a format commonly referred to as 'dotted decimal.' Each of these four numbers is termed an 'octet' due to its composition of 8 bits. Below, you can see the binary representation of each octet in the IPv4 address 192.168.10.100:

|Format   	        |1st Octet   	|2nd Octet   	|3rd Octet   	|4th Octet   	|
|---	            |---	        |---	        |---	        |---	        |
|Dotted Decimal   	|192   	        |168   	        |10   	        |100   	        |
|Binary   	        |11000000   	|10101000   	|00001010   	|01100100   	|

An octet can contain values ranging from 0 to 255, resulting in the entire IPv4 address space spanning from 0.0.0.0 to 255.255.255.255. Within an IPv4 address, there are distinct segments: the network portion and the host portion. To identify these sections, a subnet mask is employed. 

### Network Address
The network part of the IPv4 address is on the left-hand side of the IP address. It specifies the particular network to where the IPv4 address belongs. The network portion of the address also identifies the IP address class of the IPv4 address.

For example, we have the IPv4 address 192.168.10.100 and a /24 subnet mask. /24 simply means that the first 24 bits, starting from the left side, is the network portion of the IPv4 address. The 8 remaining bits of the 32 bits will be the host portion.


### Host Address
The host portion of the IPv4 address uniquely identifies the device or the interface on your network. Hosts that have the same network portion can communicate with one another directly, without the need for the traffic to be routed.

# Converting the Decimal IP Address to Binary
IP addresses can be interpreted either in their decimal or binary forms; however, it's important to note that network devices exclusively comprehend the binary representation. Therefore, it becomes crucial for us to grasp the process of converting a decimal IP address into its binary equivalent.

## Decimal Number
Decimal is a base-10 numbering system that's widely familiar to us. In this system, we employ ten distinct numerals to symbolize numbers ranging from zero to nine. These numerals are 0, 1, 2, 3, 4, 5, 6, 7, 8, and 9. When we reach the value ten, there is no specific numeral to denote it. Instead, we transition to the next place value, advancing from ones to tens and beyond.

## Binary Number
Binary numbers constitute an alternative numerical system predominantly employed to express machine language. In stark contrast to the decimal system, binary utilizes merely two numerals for representation, namely, 1 and 0. Each placeholder in the binary system possesses a distinct value, which is why it is often referred to as the Base 2 Numbering System.

## Converting Decimal to Binary IP Address
Below is an example of an IPv4 address in dotted decimal format and its corresponding binary format.

IP Address = 192.168.32.47

**NB**: The 1st Octet of the IPv4 address is used in the calculation below: 

|Division by 2   |Quotient   	|Remainder(Digit)  	|Bit #   	|
|---	         |---	        |---	            |---	    |
|(192)/2   	    |96   	|0   	|0   	|
|(96)/2   	    |48 	|0   	|1   	|
|(48)/2   	    |24   	|0   	|2   	|
|(24)/2   	    |12   	|0   	|3   	|
|(12)/2   	    |6   	|0   	|4   	|
|(6)/2   	    |3   	|0   	|5   	|
|(3)/2   	    |1   	|1   	|6   	|
|(1)/2   	    |0   	|1   	|7   	|

## Converting Binary IP Address to Decimal
Below is an example of an IPv4 address in binary format and its corresponding dotted decimal format.

Binary format = 11000000

(11000000)₂ = (1 × 2⁷) + (1 × 2⁶) + (0 × 2⁵) + (0 × 2⁴) + (0 × 2³) + (0 × 2²) + (0 × 2¹) + (0 × 2⁰) = 192

The answer above corresponds to the 1st Octet of the following IP Address(192.168.32.47)

# Subnet Mask Explained
An IP address is typically split into two distinct components: the network part and the host part. Take, for instance, a Class A IP address, where 8 bits are dedicated to identifying the network, leaving the remaining 24 bits to identify the host. This allocation aligns with the default subnet mask for a Class A IP address, which is 8 bits in length and is expressed in dotted decimal notation as 255.0.0.0. 

To comprehend this concept further, it's important to recognize that both an IP address and a subnet mask consist of 32 bits in total. Computers employ the subnet mask to differentiate between the network and host portions of an address. In this context, the '1s' in the subnet mask denote the network segment, while the '0s' represent the host portion.

## Slash Notation
In addition to the familiar dotted decimal format, subnet masks can also be represented using slash notation. This notation consists of a forward slash ('/') followed by the number of subnet mask bits. To determine the slash notation for a subnet mask, first, convert the dotted decimal format into binary, then count the consecutive '1s' in the binary representation, and finally, add the slash notation at the beginning.

For instance, consider the dotted decimal subnet mask of 255.0.0.0. When expressed in binary, it becomes 11111111.00000000.00000000.00000000. By counting the consecutive '1s,' which in this case are 8, we can determine that the slash notation for 255.0.0.0 is /8.

| Value of the First Octet   | Class    |
|--------------- | --------------- |
| 0 - 127   | A    |
| 128 - 191    | B    |
| 192 - 223    | C   |

# IP Address Classes
TCP/IP categorizes IP addresses into five distinct classes: Class A, Class B, Class C, Class D, and Class E. The designation of a class is determined by the value of the first octet of the IP address. The first three classes (A, B, and C) encompass IP addresses that can be utilized as host addresses. The remaining two classes, Class D and Class E, serve alternative functions, with Class D designated for multicast purposes and Class E reserved for experimental use.

In Class A IP addresses, the initial 8 bits (or the first decimal number) are allocated to represent the network segment, leaving the remaining 24 bits to denote the host portion. For Class B addresses, the first 16 bits (or the first two decimal numbers) are designated for the network part, while the subsequent 16 bits serve as the host part. In the case of Class C, the initial 24 bits are reserved to define the network component, while the final 8 bits are utilized for specifying the host segment.

| Class    | Public IP Range | Network Bits| Default Subnet Mask| Slash Notation |
|---------------- | ------------------------ | --------------- | --------------- | --------------- |
| A    | 1.0.0.0 - 127.0.0.0     | 8    | 255.0.0.0     | /8   |
| B    | 128.0.0.0 - 191.255.0.0    | 16   | 255.255.0.0    | /16    |
| C    | 192.0.0.0 - 223.255.255.0   | 24    | 255.255.255.0   | /24   |

# Subnetting Explained
Subnetting involves the partitioning of a network into multiple smaller networks, a practice employed to bolster routing efficiency, fortify network security, and diminish the size of broadcast domains. An evident drawback of having all hosts within a single network is the creation of a unified broadcast domain where any broadcast transmission initiated by any device permeates throughout the entire network, leading to a surfeit of unnecessary traffic.

This setup also introduces security concerns, as every device gains unrestricted access to communicate with any other device on the network. This unrestricted access can pose potential security risks, for instance, having a server housing sensitive information coexist in the same network as user workstations.

Subnetting also aids in addressing organizational concerns, particularly in extensive networks. In larger networks, different departments or units are often segregated into distinct subnets, streamlining network management and administration.

# CIDR (Classless inter-domain routing)
CIDR (Classless Inter-Domain Routing) is a method of assigning public IP addresses that was introduced in 1993 by the Internet Engineering Task Force (IETF). It was devised to address two primary objectives:

1. **Mitigating IPv4 Address Exhaustion:** CIDR was developed in response to the pressing issue of IPv4 address depletion. It sought to optimize IP address allocation in the face of dwindling available addresses.

2. **Curbing the Expansion of Internet Routing Tables:** Another key aim of CIDR was to slow down the proliferation of routing tables within Internet routers. This helped alleviate the strain on the core infrastructure of the internet.

Before the advent of CIDR, public IP address assignment adhered to class-based boundaries:

- **Class A:** The classful subnet mask was /8, offering a total of 16,777,216 possible IP addresses (2 to the power of 24).
- **Class B:** The classful subnet mask was /16, providing 65,536 addresses.
- **Class C:** The classful subnet mask was /24, with only 256 addresses available.

CIDR introduced a more flexible approach to IP address allocation, enabling the allocation of varying block sizes and allowing for a more efficient utilization of the dwindling IPv4 address space. It ushered in a more scalable and sustainable way of managing IP addresses on the internet.

## Subnet Creation
There are a couple of methods to create subnets. In this article, we'll be focusing on subnetting a default Class C address, which is 192.168.0.0, and comes with 24 subnet bits and 8 host bits as per the default configuration.

Before diving into subnetting, it's essential to address two crucial questions:

1. **Determining the Number of Subnets Needed:**
   To calculate the number of subnets required, we can employ the formula 2^x, where 'x' represents the count of '1s' in the subnet mask. For instance, with just one subnet bit, we can generate 2^1, or 2 subnets. By extending this logic, using 2 bits yields 2^2, or 4 subnets, while 3 bits provide 2^3, or 8 subnets, and so forth.

2. **Defining the Hosts per Subnet:**
   For ascertaining the number of hosts per subnet, we utilize the formula 2^y - 2, where 'y' corresponds to the count of '0s' in the subnet mask. This calculation excludes two addresses: one for the network address and another for the broadcast address, ensuring that we reserve these addresses for network identification and broadcast transmissions.

### Subnetting Example
To illustrate the concept of subnetting, consider the following scenario. Suppose we need to subnet a Class C address, specifically 192.168.0.0/24, into two subnets, each accommodating up to 50 hosts. Here's how we can calculate and implement this:

1. **Determining the Subnet Mask:**
   To create two subnets, we require 2^1, or 2, subnet bits. In our case, this necessitates borrowing one bit from the host portion. Let's convert the Class C address and its default subnet mask to binary form:

   - 192.168.0.0 = 11000000.10101000.00000000.00000000
   - 255.255.255.0 = 11111111.11111111.11111111.00000000

   By taking a single '0' from the host part of the subnet mask, we obtain the new subnet mask:

   - 255.255.255.128 = 11111111.11111111.11111111.10000000

   It's important to remember that the '1s' in the subnet mask denote the network portion.

2. **Calculating Hosts per Subnet:**
   With one bit allocated for subnetting, we're left with seven bits for hosts. This raises the question: can these seven bits accommodate at least 50 hosts per subnet? To ascertain this, we apply the formula 2^y - 2, where 'y' represents the number of host bits. In this case, 2^7 - 2 equals 126, which is more than sufficient for our requirements.

3. **Creating the Subnets:**
   Our network now consists of two subnets, structured as follows:

   - 192.168.0.0/25: The first subnet has a subnet number of 192.168.0.0. The range of IP addresses within this subnet spans from 192.168.0.0 to 192.168.0.127.

   - 192.168.0.128/25: The second subnet bears a subnet number of 192.168.0.128. The IP addresses in this subnet fall within the range of 192.168.0.128 to 192.168.0.255.

This subnetting approach allows us to efficiently manage our network, dividing it into smaller, manageable segments while ensuring adequate host capacity for each subnet.
