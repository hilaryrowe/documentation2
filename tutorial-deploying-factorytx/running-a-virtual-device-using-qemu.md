# Running a Virtual Device Using QEMU

If you need to install QEMU for your platform, go here for more information:[https://www.qemu.org/download/](https://www.qemu.org/download/)

QEMU is a lightweight virtualization service. We recommend QEMU for the development or testing of FactoryTX, but for production deployments, we recommend using VMWare or VirtualBox.

**To run a virtual device using QEMU:**

1. Install qemu-kvm and Virtual Machine Manager \(AKA, virt-manager\), the tool that allows you to use a graphical interface to interact with KVM. Go to:[https://help.ubuntu.com/community/KVM/VirtManager](https://help.ubuntu.com/community/KVM/VirtManager)

2. In virt-manager, select Import Existing Disk Image &gt; Browse &gt; Browse Local to locate the Resin \*.img file \(raw file format\).

3. Accept the default memory and CPU settings.

4. Define the VM name, and then clickFinish.

5. Go to the Resin.io Applications page and verify that the new VM device is added.





