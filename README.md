---
*This project has been created as part of the 42 curriculum by ymouhib.*

---

# NetPractice

## Description

NetPractice is a networking training project focused on understanding and mastering fundamental TCP/IP concepts. The goal of this project is to correctly configure small virtual networks by applying theoretical knowledge about IP addressing, subnetting, routing, and OSI layers.

Through 10 progressively challenging levels, we analyze network topologies and configure devices (hosts and routers) so that communication between machines becomes possible. Each level requires identifying configuration mistakes or missing parameters and correcting them.

This project strengthens practical understanding of how real networks operate and how routing decisions are made.

---

## Instructions

### Running the Training Interface

To start NetPractice locally:

```bash
./run.sh
```

This will launch the training interface in your browser.

Each level presents a network topology. Your task is to:

- Assign correct IP addresses
- Configure subnet masks
- Set correct default gateways
- Ensure routers are properly configured
- Validate that hosts can communicate

When your configuration is correct, you can export the level configuration.

---

### Exporting Configurations

After successfully completing a level:

1. Click the **Export** button.
2. Save the exported configuration file.
3. Rename it appropriately if needed.
4. Place it at the root of your Git repository.

Repeat this for all 10 levels.

---

## Submission Details

- You must submit **10 exported configuration files (one per level)**.
- All exported files must be placed at the **root of the repository**.
- A valid `README.md` file must also be present at the root.

Repository structure example:

```text
.
├── README.md
├── level1.export
├── level2.export
├── level3.export
├── ...
└── level10.export
```

---

## Networking Concepts Studied

### What Is an IP Address

An IP address is a logical identifier assigned to a device on a network. It allows devices to locate each other and exchange data. An IPv4 address is composed of 32 bits divided into a **network part** (identifying the network) and a **host part** (identifying the device within that network).

---

### TCP/IP Addressing

TCP/IP addressing defines how devices are identified and how data is routed across networks. It includes private and public IP addressing, CIDR notation, and the separation between network and host bits. Correct TCP/IP addressing is essential for communication between hosts and across routers.

---

### Subnet Masks

A subnet mask is used to determine which part of an IP address represents the network and which part represents the host. By applying a subnet mask, we can calculate:

- The network address
- The broadcast address
- The valid range of host addresses
- The maximum number of hosts in a subnet

Subnetting allows efficient use of IP addresses and separation of networks.

---

### Network Address and Broadcast Address

The **network address** identifies the subnet itself and cannot be assigned to a host.
The **broadcast address** is used to send data to all devices within the same subnet and also cannot be assigned to a host.

All usable host addresses exist between these two values.

---

### Default Gateway

A default gateway is the IP address of a router interface that allows a device to communicate with networks outside its own subnet. When a host wants to reach an external network, it sends the packet to its default gateway, which then forwards it to the correct destination.

---

### Routers and Routing

Routers are Layer 3 devices responsible for forwarding packets between different networks. Routing is the process of selecting the best path for data to travel from source to destination, based on routing tables that contain network destinations and next-hop information.

---

### Switches

Switches operate at the Data Link Layer (Layer 2) of the OSI model. They forward frames within the same local network using MAC addresses. Switches do not perform routing or modify IP addresses.

---

### OSI Model

The OSI model is a conceptual framework that explains how data flows through a network using seven layers. In NetPractice, the most relevant layers are:

- **Physical Layer** – Transmission of raw bits
- **Data Link Layer** – MAC addressing and frame delivery
- **Network Layer** – IP addressing and routing
- **Transport Layer** – End-to-end communication

Understanding these layers helps identify where communication problems occur.

---

## Methodology

For each level, the following approach was used:

1. Identify all networks and subnets.
2. Calculate network and broadcast addresses.
3. Determine valid host ranges.
4. Verify subnet mask consistency.
5. Ensure correct default gateway configuration.
6. Validate that router interfaces belong to the correct networks.

Binary subnet calculations were used when necessary to avoid overlapping networks and invalid configurations.

---

## Resources

The following resources were used to understand and complete the project:

- 42 NetPractice subject
- [All notes](https://www.tldraw.com/f/vqNuFD_oI1j_Efbg0Hhi9?d=v-5238.-3932.21299.12341.page)
- [CCNA NetworkChuck playlist](https://www.youtube.com/watch?v=S7MNX_UD7vY&list=PLIhvC56v63IJVXv0GJcl9vO5Z6znCVb1P)
- [Network basics playlist](https://www.youtube.com/watch?v=q6tUCEUqxTQ&list=PL8s4OGp0649_e_Wbz5MlBgW5rBW-9hD0c)

### Use of AI

AI tools were used for:

- Clarifying subnetting calculations
- Verifying IP range computations
- Explaining routing logic
- Reviewing theoretical networking concepts

AI was **not** used to automatically generate solutions for the levels. All configurations were manually calculated and validated.

---

## Key Learnings

- How to calculate network and broadcast addresses manually
- How subnet masks affect host capacity
- How routers connect multiple networks
- Why correct gateway configuration is critical
- How routing failures occur due to incorrect addressing
