# Running on an Intel NUC

**NOTE: **This procedure requires a USB drive.

You will need to burn the image file that you downloaded from resinOS to a USB drive so you can use it on the NUC. To do this, you should use Etcher, an image burner tool by [Resin.io](http://resin.io), to flash installable images onto USB.

**To run on a Intel NUC:**

1. Download and install Etcher at [http://etcher.io](http://etcher.io), and then follow the steps in the Etcher interface to burn the resinOS image \(i.e., &lt;your\_image\_filename.img&gt;\) onto a USB drive.

2. Insert the USB key and power up the NUC.

3. On the Add a New Device page, follow the instructions.  
   ![](/tutorial-deploying-factorytx/Running on Intel NUC1.png)

4. If resinOS cannot boot from the correct boot partition, reset the BIOS to the default, and then check the following items in the BIOS:

   * Boot option:  
     ![](/tutorial-deploying-factorytx/Running on Intel NUC2.png)

   * Hard drive BBS priority:  
     ![](/tutorial-deploying-factorytx/Running on Intel NUC3.png)

   * Boot override:  
     ![](/tutorial-deploying-factorytx/Running on Intel NUC4.png)

5. Go to the Resin.io Applications page and verify that the new NUC device is added. You should see an image similar to:  
   ![](/tutorial-deploying-factorytx/Running on Intel NUC5.png)

6. When the device is powered down, and on the Applications page the Status is Post Provisioning, remove the USB drive and press the NUC power button.  
   ![](/tutorial-deploying-factorytx/Running on Intel NUC6.png)

7. The status will change to Online or Downloading. Wait for the status to be Online.  
   ![](/tutorial-deploying-factorytx/Running on Intel NUC7.png)



