# Running a Virtual Device Using Oracle VirtualBox

You will need to convert the image file into a format that Oracle VirtualBox can use.

**To run a virtual device using Oracle VirtualBox:**

1. Use the .img file and convert it to VMDK:  
   **`qemu-img convert <your_image_filename.img> -O vdi outputImage.vdi`**

2. Resize the .vdi file to use appropriate space:  
   **`vboxmanage modifyhd <your_image_filename.vdi> --resize 2288`**  
  
   **NOTE: **The last parameter is space in MB; this is ~2GB.

3. Start Oracle VirtualBox.

4. Follow the instructions and use Linux Ubuntu 64-bit.

5. Set the memory size to 1024MB.

6. Use the existing .vdi file as your virtual hard disk.

7. Go to the Resin.io Applications page and verify that the new VM device is added.



