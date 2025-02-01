When we go to configuration sub directory in openlane (cd Desktop/work/tools/openlane_working_dir/openlane/configuration), we get to see many files including README.md (by typing ls -ltr command at the prompt.
When we run this README.md file by usinng less command, we get the screen as under.  This README file contains all the floor plan related details including aspect ratio, core utilization etc.
![VirtualBox_vsdworkshop_01_02_2025_14_19_10](https://github.com/user-attachments/assets/a2197c67-863d-4369-82ed-e833be13cc76)
Next, when we open floorpla.tcl, we can see the parameter that  have not been set to.  These are default parameters which are set for floorplanstage in openlane.
![VirtualBox_vsdworkshop_01_02_2025_14_26_33](https://github.com/user-attachments/assets/ced952cd-18c1-4db3-9068-6665e3859df4)
![VirtualBox_vsdworkshop_01_02_2025_14_26_46](https://github.com/user-attachments/assets/406b30ca-6b9c-4724-aaa8-40a168055947)
After checking the required files, we run floorplan by typing command run_floorplan and we get the screen as under.
![VirtualBox_vsdworkshop_01_02_2025_14_49_05](https://github.com/user-attachments/assets/eee18aee-1ce7-42f8-b1f4-566a1b83dceb)
now, just like how we did for synthesis, we will go to the runs folder to see the latest file that got generated.
![VirtualBox_vsdworkshop_01_02_2025_14_51_19](https://github.com/user-attachments/assets/589c8db3-7cba-4883-81c2-920f14dab0d5)
we see that a folder 01-02_09-15 get generated.  Now we will go to that folder and see the contets of this folder.  then wee go to logs folder/floorplan, we see that metal layer IO can see seen here in 4ioplacer.log file.
![VirtualBox_vsdworkshop_01_02_2025_14_59_17](https://github.com/user-attachments/assets/10c54f5d-3ae2-4f99-a7ed-66d48692deab)

now when we go to floorplan directory in the results directory. We see one file picorv32a.floorplan.def file.  when we run  this file, we get the dimensions of our die in the form (Lower left x value, lower  left y value) (upper right x value, upper right y value) co-ordinates.  using this we can claculate the area of the die and unit would be distance microns.  i microns = 1000 database units.  If we divide values of upper right x and y figures with 1000, we get the dimensions of chip in micrometer.
![VirtualBox_vsdworkshop_01_02_2025_15_18_44](https://github.com/user-attachments/assets/62422ffb-01a0-4f01-abe7-0b4fae668dfc)
to see the actual layout floorplan it is first done in magic.   
