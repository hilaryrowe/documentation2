# Setting Up a FactoryTX Network Configuration

FactoryTX will be easiest to deploy when you are using DHCP \(automatic network configuration\) over a wired Ethernet connection and you have access to external IPs. If this is the case, you can use the same deployment image/USB to deploy multiple devices.

If you are running a Virtual Machine, default network settings are usually sufficient, assuming that the host OS is already on the correct network. You can make any advanced or specific settings within the VM manager \(e.g., VirtualBox or VMWare\). If you are looking to connect to the Web interface from outside of the host system, you may need to create a “bridged” network to the VM.

If you have other needs, such as using static IPs, configuring WiFi, or using an outbound proxy, we recommend consulting the Resin.io documentation directly: [https://docs.resin.io/](https://docs.resin.io/)

