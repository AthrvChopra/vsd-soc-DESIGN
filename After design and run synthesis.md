Now we can cross check and see that we have created a runs dub directory in picorv32a subdirectory, by typing this path in command prompt (in new tab) Desktop/work/tools/openlane_working_dir/openlane->designs->picorv32a and then list the files/directories by ls -ltr
![VirtualBox_vsdworkshop_31_01_2025_10_24_26](https://github.com/user-attachments/assets/31fdb82c-c345-4087-837c-b8df677672b5)
when we change directory to runs and list we find one sub-directory 30-01_15-53 and by again moving to this sub-directory by typing cd 30-01_15-53 and then list the content by  ls -ltr command, we get to see the subb-directories created during our working (in my case between Jan 28-31, 2025), including tmp.  Again when we move into this sub-directory, and list the contents, we get to see the files created on Jan 30 and 31, 2025 (during my working on virtual machine).
![VirtualBox_vsdworkshop_31_01_2025_10_37_07](https://github.com/user-attachments/assets/dd7eb619-9af3-4a76-a6f1-fa6ce8f8e017)
One of the files we found is merged.lef, when we open this file by less command (less merged.lef), we see the different layers as we can in the screen shot below.
![VirtualBox_vsdworkshop_31_01_2025_10_46_59](https://github.com/user-attachments/assets/0bd658de-8461-48a9-8d2d-346f9ac3e3b1)
We can get back to our original screen by pressing q
in our  sub-directory 30-01_15-53 there is one file config.tcl and when we run this file by less command (less config.tcl), we get the screen as under
![VirtualBox_vsdworkshop_31_01_2025_11_22_12](https://github.com/user-attachments/assets/4f64c5ce-97d8-4836-b7fb-98bbe1233b2a)
![VirtualBox_vsdworkshop_31_01_2025_11_22_31](https://github.com/user-attachments/assets/39103c1a-a226-4d06-81d6-9b8225a30fb1)
Here we exit the screen by pressing q.  
thereafter we run run_synthesis, we get the screen with synthesis successful
![VirtualBox_vsdworkshop_31_01_2025_12_11_59](https://github.com/user-attachments/assets/87a83d6c-b7d9-4713-81ff-cae0065b9153)
