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
