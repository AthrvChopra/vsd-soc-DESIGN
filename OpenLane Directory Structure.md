# vsd-soc-DESIGN
Open the virtual Machine ans start the terminnal.  You get the following screen:
![VirtualBox_vsdworkshop_30_01_2025_10_43_26](https://github.com/user-attachments/assets/ee90d529-e5e2-4990-82fd-22a5cb1b221a)
Type cd Desktop the folder gets changed to Desktop 
Then type cd work/tools and your the directory chnages to Work -> Tools.  You get the screen as under
![VirtualBox_vsdworkshop_30_01_2025_10_50_17](https://github.com/user-attachments/assets/cf81cd9e-10e3-489b-bd01-7acb4c958a21)
Now we will work on Tools directory.  to list the contents (file and folders) of tools directory we will giev command ls -ltr.  As shown in the image below there are total 8 files/folders are there, out of which we can see 2 (csdflow and openlane_working_dir)
![VirtualBox_vsdworkshop_30_01_2025_10_53_17](https://github.com/user-attachments/assets/fe9bb373-0af1-4cf9-80e0-aa59c86e0c5e)
Here, for our work, we will use openlane_working_dir.  Hence, we give command cd openlane_working_dir and also list the contents of this directory by giving ls -ltr command.  We can see 3 files/folders in openla_working_dir folder.  These are pdks,  openlane_old and openlane.  We will be using pdks and Openlane. 
First we open pdks directory, henec  we type cd pdks and then we will list the contents of pdks by typeing ls -ltr.  we get the below image, where we can see 3 files and folders (skywater-pdk, open_pdks and sky130A)
![VirtualBox_vsdworkshop_30_01_2025_11_00_26](https://github.com/user-attachments/assets/803d0a56-30da-4b2f-a3fa-d8b1a4a87c6c)
we will be working with skywater 130nm.  So we will again change the directory to sky130A and then list the contents with ls -ltr command.  We see there are 3 diretories (libs.tech, libs.ref and sources).  libs.tech contains are the tools related files and on chnaging directory and listing the files of libs.tech, we see directories as klayout. netgen, magic,openlane etc.  
![VirtualBox_vsdworkshop_30_01_2025_11_09_09](https://github.com/user-attachments/assets/1439db19-52bf-4950-a40d-9820f27862ed)
Now we will see the files in libs.ref.  For this first we go back one directory (move to sky130A) by typing cd .. (in my case by mistake i gave cd\ and i went to parent directory, hence repeated the commmands to go to libs.ref). Once we are in libs.ref we will list the contents of this directory and we see that libs.ref contains all skywater (foundry) related files/information.
![VirtualBox_vsdworkshop_30_01_2025_11_19_01](https://github.com/user-attachments/assets/91fe7f1a-7f4f-4b50-9539-ca5b70ac3446)
we completed exploring our pdks.  now we will explore opnelane. so we will give command cd .. untill we go back to opnelane_working_dir and then chnage the directory to openlane  by cd openlane.  Thereafter we will list the contents of openlane directory by giving ls -ltr. We see many file and folders as flow.tcl, design etc which we can in the image as under.
![VirtualBox_vsdworkshop_30_01_2025_11_25_17](https://github.com/user-attachments/assets/b5c7172e-9b84-4cfb-9534-bb219a3dcaf8)
Since we will be working with sky130A, we will go to that directory and list the contents/folders of this directory.  from the listed dircetories of sky130A, we found all the technology related sub-directories.  one of the dub directories is sky130_fd_sc_hd.  When we enter sky130_fd_sc_hd directory, we found many files, like libb, lef, doc etc.  When we go to Lib directory, we get time related information.
Since we will be working with openlane directory, we go back to openlane directory in openlane_working_dir.  Now we have to invoke the tools.
![VirtualBox_vsdworkshop_30_01_2025_17_00_10](https://github.com/user-attachments/assets/fa376698-75e5-4ea1-8abd-751c663d722e)
To invoke the tools, we give command docker.  With this command the prompt now changes to bash-4.2$.  Now with the prompt bash-4.2$ we type ls -lrth, we get some list of files/sub-directories. Then we give command //flow.tcl -interactive and with this openlane would open, as per the screen below. With this the prompt changes to %. 
![VirtualBox_vsdworkshop_30_01_2025_19_44_58](https://github.com/user-attachments/assets/abaa189d-3f16-4540-b39c-c9f6bc9277b8)
now the following 3 steps are to be done everytime: (1) package require openlane 0.9 - with this we are ready to execute the command (2) 
in openlane directory there is a sub directory design, which has some 30-40 designs (we can build our own designs as well).  We can get list of designs by invoking command ls -ltr in design sub directory of openlane directory.  We will be doing for picorv32a
Next we  give the command prep -design picorv32a. With this two lef's get merged and preparation of design is completed, we get the below screen.
![VirtualBox_vsdworkshop_30_01_2025_21_25_32](https://github.com/user-attachments/assets/a03b5f53-c44c-49e1-a33a-115b5d2869d3)

Now we can cross check and see that we have created a runs dub directory in picorv32a subdirectory, by typing this path in command prompt (in new tab) Desktop/work/tools/openlane_working_dir/openlane->designs->picorv32a and then list the files/directories by ls -ltr
![VirtualBox_vsdworkshop_31_01_2025_10_24_26](https://github.com/user-attachments/assets/31fdb82c-c345-4087-837c-b8df677672b5)
when we change directory to runs and list we find one sub-directory 30-01_15-53 and by again moving to this sub-directory by typing cd 30-01_15-53 and then list the content by  ls -ltr command, we get to see the subb-directories created during our working (in my case between Jan 28-31, 2025), including tmp.  Again when we move into this sub-directory, and list the contents, we get to see the files created on Jan 30 and 31, 2025 (during my working on virtual machine).
![VirtualBox_vsdworkshop_31_01_2025_10_37_07](https://github.com/user-attachments/assets/dd7eb619-9af3-4a76-a6f1-fa6ce8f8e017)
One of the files we found is merged.lef, when we open this file by typing merged.lef, we see the different layers as we can in the screen shot below.
![VirtualBox_vsdworkshop_31_01_2025_10_46_59](https://github.com/user-attachments/assets/0bd658de-8461-48a9-8d2d-346f9ac3e3b1)





