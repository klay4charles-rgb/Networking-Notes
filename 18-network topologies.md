# Network Topologies

## Main Idea

A network topology describes how devices are connected within a network and how data travels between them. Different topologies provide different levels of performance, redundancy, scalability, and fault tolerance.

## Star Topology

A Star Topology connects all devices to a central device, such as a switch or hub.

Characteristics:

* All communication passes through the central device
* Commonly used in Ethernet networks
* Easy to manage and troubleshoot
* Failure of an individual connection affects only one device

Example:

* Switched Ethernet network

## Mesh Topology

A Mesh Topology provides multiple paths between devices.

Types:

### Full Mesh

Every device is connected to every other device.

### Partial Mesh

Only selected devices have multiple connections.

Benefits:

* High redundancy
* Fault tolerance
* Load balancing
* Multiple communication paths

Commonly used in:

* WAN environments
* Critical network infrastructure

## Hybrid Topology

A Hybrid Topology combines multiple topology types within the same network.

Examples:

* Star + Mesh
* Star + Point-to-Point

Benefits:

* Flexibility
* Scalability
* Custom network design

Organizations often use hybrid topologies to meet different networking requirements.

## Leaf and Spine Architecture

Leaf and Spine is a modern data center topology designed for high performance and scalability.

### Leaf Switches

* Connect directly to servers and network racks
* Often used as Top-of-Rack (ToR) switches

### Spine Switches

* Connect all leaf switches together
* Provide fast communication paths

Rules:

* Every leaf connects to every spine
* Leaf switches do not connect directly to other leaf switches
* Spine switches do not connect directly to other spine switches

Benefits:

* High performance
* Low latency
* Redundancy
* Simplified cabling
* Scalability

Disadvantages:

* Increased hardware costs
* More switches required

## Point-to-Point Topology

A Point-to-Point topology creates a direct connection between two devices.

Characteristics:

* Dedicated communication path
* Simple design
* Reliable connection

Examples:

* T1 WAN connections
* Building-to-building links

## Key Takeaway

Network topologies define how devices communicate within a network. Star, Mesh, Hybrid, Leaf-and-Spine, and Point-to-Point topologies each provide different advantages depending on performance, scalability, and redundancy requirements.
