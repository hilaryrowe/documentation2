# Tutorial: Deploying FactoryTX

There are two supported methods for FTX edge deployment:

* An edge industrial PC appliance \(the Intel NUC\)

* A Virtual Machine file in VMDK \(Virtual Machine Disk\) or QEMU format for use with Oracle VirtualBox

The Resin.io platform is recommended because it provides infrastructure for managing edge devices. It includes an operating system that is off-limits so you cannot brick your device, and lets you deploy arbitrary containers/applications on top of that operating system. It also handles phoning home for updates, the compression of images for fast remote upgrades, VPN support if you SSH in to a given device, and a Web-based portal for device management, version control, etc.

The graphic below shows how FTX can be installed on edge devices to pull data from the factory floor and transmit it to Sight Machine via various cloud environments, using the Resin.io platform to manage the process.

**FactoryTX Installation Flow**

![](/tutorial-deploying-factorytx/FTX Installation Flow w Lines.png)

Follow the steps in the next sections to complete the FactoryTX deployment.

## Determining the Edge Device Target

You must specify if the target is an appliance or a VM. This is based solely on the customer engagement. You need to determine this up front before continuing with the deployment.

## Logging In to Resin

Browse to [https://resin.io/](https://resin.io/). You can log in using a free account that you create, or by linking to your Google or GitHub account. We recommend that each site create a user that individuals can be added to as collaborators.

