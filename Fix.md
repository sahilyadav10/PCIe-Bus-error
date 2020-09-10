1. Open the terminal, and type the following code.
   ```
   sudo gedit /etc/default/grub
   ```         
2. Add *pci=nomsi* (without asterisk) to GRUB_CMDLINE_LINUX_DEFAULT="quiet splash"
   ```        
   Before- GRUB_CMDLINE_LINUX_DEFAULT="quiet splash"
   After - GRUB_CMDLINE_LINUX_DEFAULT="quiet splash pci=nomsi"
   ```     
3. Save the file. Next, type the following lines in the terminal.
   ```
   sudo update-grub
   ```         
   Now, reboot the system. If the problem persists follow the next steps.
        
4. Open the terminal, and type the following line.
   ```
   sudo gedit /etc/default/grub
   ```         
5. Change *pci=nomsi* to *pci=noaer* in GRUB_CMDLINE_LINUX_DEFAULT="quiet splash pci=nomsi"
   ```     
   Before- GRUB_CMDLINE_LINUX_DEFAULT="quiet splash pci=nomsi"
   After - GRUB_CMDLINE_LINUX_DEFAULT="quiet splash pci=noaer"
   ```      
6. Save the file. Next, type the following lines in the terminal.
   ```
   sudo update-grub
   ```         
 Now, reboot the system.         
