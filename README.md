# Virtual-Network-Design-and-Sniffing

## Project Overview

Welcome to the Virtual Network Design and Sniffing project! This hands-on endeavor is geared towards providing a practical learning experience in network design and protocols. By engineering a detailed network design topology within VirtualBox, I aim to explore the intricacies of networking concepts and gain a deeper understanding of network protocols.

![All VMs](https://res.cloudinary.com/dkqvrhzs3/image/upload/v1700278365/screenshots/all_VMs_ou5byz.png)


## Project Features

### 1. Detailed Network Design Topology

I've meticulously designed a network topology within VirtualBox, seamlessly integrating three key components: `RouterVM`, `PC1`, and `PC2`. This setup reflects a real-world network scenario, allowing for a comprehensive exploration of routing strategies and IP address assignments to establish a robust network structure.

### 2. Ubuntu Server for RouterVM, Ubuntu for PC1 and PC2

To mirror real-world scenarios, I've chosen an Ubuntu Server for `RouterVM` and a regular Ubuntu Desktop for `PC1` and `PC2`. This mix of operating systems provides a practical environment for network design and protocol implementation.

### 3. Wireshark and TShark Integration

For in-depth analysis and protocol sniffing, I've implemented Wireshark on `PC1` and TShark on `RouterVM`. This combination allows me to capture and dissect network protocols, providing valuable insights into the communication flow within our designed network topology.

## Purpose

The primary goal of this project is to facilitate a practical learning experience in network design and protocols. By actively engaging with the setup, you can enhance your understanding of real-world networking scenarios, routing strategies, and the analysis of network protocols using tools like Wireshark.

## Getting Started

To get started with the project, follow these detailed steps:

### Step 1: Install VirtualBox

If VirtualBox is not already installed on your machine, download and install it from the official [VirtualBox website](https://www.virtualbox.org/).
![Virtual Box Interface](https://res.cloudinary.com/dkqvrhzs3/image/upload/v1700278523/screenshots/virtual_box_interface_fniauc.png)

### Step 2: Create New Virtual Machines

1. Open VirtualBox and click on "New" to create a new virtual machine for `RouterVM`
2. Follow the prompts in the wizard to set up the new VM. When prompted for the operating system, choose "Linux" and select "Ubuntu(64-bit)" for `RouterVM`
3. Repeat the process to create new virtual machines for `PC1` and `PC2`, choosing "Ubuntu(64-bit)" for both

![VMs grouped](https://res.cloudinary.com/dkqvrhzs3/image/upload/v1700284945/screenshots/vms_group_zibmzn.png)

Ubuntu Server ISO: https://ubuntu.com/download/server <br>
Ubuntu Desktop ISO: https://ubuntu.com/download/desktop

### Step 3: Configure Virtual Machines Network Settings

1. In VirtualBox, go to "Tools" -> "Network" -> "Host-only Networks"
2. Click on "Create" to add a new network. Name anything you like. In my case, I have named it as 'vboxnet0'
3. Go to each VM's settings
4. Under "Adapter 2," select the newly created Host-Only Network (`vboxnet0`)
5. Click "OK" to apply the changes

![vboxnet0 configuration](https://res.cloudinary.com/dkqvrhzs3/image/upload/v1700278361/screenshots/vboxnet0_Host-only_Network_gpv5ls.png)

### Step 4: Configure Virtual Machines

1. Select each VM in VirtualBox and click on "Settings"
2. Under the "Systems" tab, make some changes to Motherboard and processor if needed
3. Under the "Network" tab, make changes to Adapter 1 and Adapter 2

For detailed instructions with visual guidance, please refer to the screenshots provided below:
![RouterVM](https://res.cloudinary.com/dkqvrhzs3/image/upload/v1700278521/screenshots/Router_hiwsip.png)
![PC1](https://res.cloudinary.com/dkqvrhzs3/image/upload/v1700278520/screenshots/PC1_syjn05.png)
![PC2](https://res.cloudinary.com/dkqvrhzs3/image/upload/v1700278521/screenshots/PC2_mmtb3f.png)
![VMs General Setting Sample](https://res.cloudinary.com/dkqvrhzs3/image/upload/v1700278518/screenshots/general_settings_k78qkm.png)
![RouterVM System Setting](https://res.cloudinary.com/dkqvrhzs3/image/upload/v1700278522/screenshots/system_settings_hlvogh.png)
![PCs System Setting](https://res.cloudinary.com/dkqvrhzs3/image/upload/v1700278521/screenshots/System_Setting_for_PC1_and_PC2_elsmge.png)
![Adapter1](https://res.cloudinary.com/dkqvrhzs3/image/upload/v1700278519/screenshots/network_setting_1_jdpw3j.png)
![Adapter2](https://res.cloudinary.com/dkqvrhzs3/image/upload/v1700278519/screenshots/network_setting_2_tc4eep.png)
![Host-only Network Dropdown](https://res.cloudinary.com/dkqvrhzs3/image/upload/v1700278361/screenshots/host-only_network_b177gm.png)

### Step 5: Start Virtual Machines

1. With the VMs selected, click "Start" to launch each VM.
2. Follow the on-screen instructions to install Ubuntu on each VM.
   
You can also check some YouTube videos if you get any issues while installing Ubuntu.

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
![ping example](https://res.cloudinary.com/dkqvrhzs3/image/upload/v1700278361/screenshots/ping_example_wyvurh.png)

### Step 7: Protocol Analysis with Wireshark

1. Launch Wireshark on PC1 and TShark on RouterVM.
2. Capture and analyze network protocols actively.

![Wireshark example](https://res.cloudinary.com/dkqvrhzs3/image/upload/v1700278363/screenshots/wireshark_jsuejs.png)
![TShark example](https://res.cloudinary.com/dkqvrhzs3/image/upload/v1700278361/screenshots/tshark_ffpqsl.png)

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

This project is licensed under the MIT License - see the [LICENSE.txt](LICENSE.txt) file for details.

--- 
