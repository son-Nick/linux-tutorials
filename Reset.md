### 1 — The first step is to restart the system. The GRUB page will display as soon as the process finishes, as in the following image. Then quickly, we must press the “E” key to not complete the booting.
![step1](/images/step1.png)
### 2- When we press the letter “E,” we enter the OS parameter editing page, and we must modify the code. After locating the line where it starts with the word “Linux,” at the end of that line, we need to change the permission ro (read) to rw (read and write).
![step2](/images/step2.png)

### 3 — The next step is adding or modifying the command line. In some cases, usually when the OS is installed directly on the machine and not a virtual machine, so it is necessary to change from ro to rw and add “int=/bin/bash” at the end, but in VirtualBox, we have to insert the complement of the line. So the command should look like the following for any installation “rw initrd=/install/gtk/initrd.gz quiet init=/bin/bash”. And to save and process these changes, we will use CTRL+x or F10 to continue the boot.

![step3](/images/step3.png)

### 4- Right after a GRUB screen appears again, we should press Enter, which will direct us to the terminal.

![step4](/images/step4.png)

### 5- Resetting the root user password: first is confirming this in the root user, so I used the “whoami” command. Soon I used the command “passwd,” which asked me to enter the new password twice in the terminal. Then it showed a message that the password was successfully modified. Finally, insert the “reboot -f” command to restart the machine.

![step5](/images/step5.png)

### 6- Resetting any user password: the method is the same, with the “passwd username” command and entering the new password twice, in this case, I used the username kali. And after I finished making all the changes necessary to use the command reboot -f.

![step6](/images/step6.png)