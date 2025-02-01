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
we see that a folder 01-02_09-15 get generated.  Now we will go to that folder and see the contets of this folder.  then wee go to logs folder/florrplan, we see that metal layer IO can see seen here in 4ioplacer.log file.

