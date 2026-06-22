# Network Architectures

## Main Idea

Network architectures define how network devices are organized and interconnected. Different architectures provide varying levels of scalability, redundancy, performance, and fault tolerance.

## Three-Tier Architecture

A Three-Tier Architecture separates network functions into three layers:

### Core Layer

The Core Layer serves as the high-speed backbone of the network.

Functions:

* Fast packet forwarding
* High availability
* High-speed connectivity between network segments

### Distribution Layer

The Distribution Layer acts as an intermediary between the Core and Access layers.

Functions:

* Traffic aggregation
* Policy enforcement
* Routing
* Network segmentation

### Access Layer

The Access Layer connects end-user devices to the network.

Examples:

* Workstations
* Printers
* Access Points
* IP Phones

Benefits of Three-Tier Architecture:

* High scalability
* Improved redundancy
* Better fault tolerance
* Easier network growth

## Two-Tier Architecture

A Two-Tier Architecture combines the Core and Distribution layers into a single layer known as a Collapsed Core.

### Collapsed Core

The Collapsed Core performs both Core and Distribution functions.

Benefits:

* Simpler design
* Lower cost
* Easier deployment
* Reduced hardware requirements

Disadvantages:

* Reduced redundancy
* Lower fault tolerance
* Less scalability compared to Three-Tier Architecture

Two-Tier Architectures are commonly used in smaller environments where simplicity and cost are more important than maximum resilience.

## Key Takeaway

Network architectures organize network devices into layers to improve performance and manageability. Three-Tier Architectures provide greater scalability and redundancy, while Two-Tier Architectures simplify deployment through the use of a Collapsed Core.
