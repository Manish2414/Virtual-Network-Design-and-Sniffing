# Virtual-Network-Design-and-Sniffing

## Project Overview

Welcome to the Virtual Network Design and Sniffing project! This hands-on endeavor is geared towards providing a practical learning experience in network design and protocols. By engineering a detailed network design topology within VirtualBox, I aim to explore the intricacies of networking concepts and gain a deeper understanding of network protocols.

## Project Features

### 1. Detailed Network Design Topology

I've meticulously designed a network topology within VirtualBox, seamlessly integrating three key components: RouterVM, PC1, and PC2. This setup reflects a real-world network scenario, allowing for a comprehensive exploration of routing strategies and IP address assignments to establish a robust network structure.

### 2. Ubuntu Server for RouterVM, Ubuntu for PC1 and PC2

To mirror real-world scenarios, I've chosen Ubuntu Server for RouterVM and regular Ubuntu for PC1 and PC2. This mix of operating systems provides a practical environment for network design and protocol implementation.
ISO download links:


### 3. Wireshark and TShark Integration

For in-depth analysis and protocol sniffing, I've implemented Wireshark on PC1 and TShark on RouterVM. This combination allows me to capture and dissect network protocols, providing valuable insights into the communication flow within our designed network topology.

## Getting Started

To get started with the project, follow these detailed steps:

### Step 1: Install VirtualBox

If VirtualBox is not already installed on your machine, download and install it from the official [VirtualBox website](https://www.virtualbox.org/).

### Step 2: Create New Virtual Machines

1. Open VirtualBox and click on "New" to create a new virtual machine for RouterVM.
2. Follow the prompts in the wizard to set up the new VM. When prompted for the operating system, choose "Linux" and select "Ubuntu(64-bit)" for RouterVM.
3. Repeat the process to create new virtual machines for PC1 and PC2, choosing "Ubuntu(64-bit)" for both.

Ubuntu Server ISO: https://ubuntu.com/download/server <br>
Ubuntu Desktop ISO: https://ubuntu.com/download/desktop

### Step 4: Configure Virtual Machines

1. Select each VM in VirtualBox and click on "Settings"
2. Under the "Systems" tab, make some changes to Motherboard and processor if needed
3. Under the "Network" tab, make changes to Adapter 1 and Adapter 2

For detailed instructions with visual guidance, please refer to the screenshots provided below:


### Step 5: Configure Virtual Machines Network Settings

1. In VirtualBox, go to "Tools" -> "Network" -> "Host-only Networks"

2. Click on "Create" to add a new network. Name that anything you like. In my case, I have named it as 'vboxnet0'

3. Go to each VM's settings

4. Under "Adapter 2," select the newly created Host-Only Network (`vboxnet0`)

5. Click "OK" to apply the changes

### Step 5: Start Virtual Machines

1. With the VMs selected, click "Start" to launch each VM.
2. Follow the on-screen instructions to install Ubuntu on each VM.
   
You can also check some youtube videos if you get any issue while installing Ubuntu.

#### Test Connection Status

Once the VMs are up and running, you can verify the connectivity between the devices by pinging them. Open a terminal window on each VM and use the `ping` command:

```bash
# On PC1, ping RouterVM
ping 192.168.56.1

# On PC1, ping PC2
ping 192.168.56.3

# On PC2, ping RouterVM
ping 192.168.56.1

# On PC2, ping PC1
ping 192.168.56.2

# On RouterVM, ping PC1
ping 192.168.56.2

# On RouterVM, ping PC2
ping 192.168.56.3
```

### Step 7: Protocol Analysis with Wireshark

1. Launch Wireshark on PC1 and TShark on RouterVM.
2. Capture and analyze network protocols actively.

## Purpose

The primary goal of this project is to facilitate a practical learning experience in network design and protocols. By actively engaging with the setup, you can enhance your understanding of real-world networking scenarios, routing strategies, and the analysis of network protocols using tools like Wireshark.

Feel free to explore, experiment, and expand upon this project to further your knowledge in the fascinating realm of networking!

# Future Explorations

As the project evolves, I envision delving into additional aspects to further enrich the learning experience and expand the capabilities of the network design. Here are some areas I'm considering exploring in the future:

## 1. Security Protocols and Configurations

Enhance the project's focus on security by implementing and exploring various security protocols and configurations. This could involve implementing firewalls, intrusion detection systems, or VPN configurations within the virtual network.

## 2. Scalability and Performance Optimization

Investigate methods for scaling the network design to accommodate a larger number of devices. Explore performance optimization strategies to ensure the network operates efficiently even under increased load.

## 3. Integration with Cloud Services

Explore the integration of virtual network setups with cloud services. This could involve connecting the on-premise virtual network to cloud-based resources, providing insights into hybrid cloud architectures.

## 4. Network Automation and Orchestration

Implement network automation tools and explore orchestration techniques to streamline and automate routine network management tasks. This could involve using tools like Ansible or Puppet to manage network configurations.

## 5. Advanced Protocol Analysis and Threat Detection

Expand the protocol analysis capabilities by incorporating advanced techniques for threat detection. Explore methods to identify and mitigate potential security threats within the network traffic.

## License

This project is licensed under the MIT License - see the [LICENSE.tx](LICENSE.txt) file for details.

--- 
