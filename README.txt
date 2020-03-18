This tool is used for converting the recorded data to OpenSim format. 

First of all, please organize the data with this format. The input and output data will follow the same format
Data -> <Subject_no> -> <Date of experiment> -> Dynamic/Static 
Output -> <Subject_no> -> <Date of experiment> -> Dynamic/Static 
Example: 
Data/Subject_01/2020_02_07/Static/TPose.csv 

To convert to the .trc format used in OpenSim's Inverse Kinematics, please open the configuration file named: "setting_motion.csv"
In this file, 
------Motion Data: The location of motion file (markers' recorded motion from Optitrack) stored in the Data folder. 
------Output_path: The location of the converted file you want to save in the Output folder.
------Output_name: The name of the converted motion file

To convert to the .sto format used in OpenSim's Inverse Dynamics, please open the configuration file named: "setting_grf.csv"
In this file, 
------Data_R: The location of force data applied to right leg stored in the Data folder. 
------Data_L: The location of force data applied to left leg stored in the Data folder. 
------Motion Data: The location of motion file (markers' recorded motion from Optitrack) stored in the Data folder. 
------Output_path: The location of the converted file you want to save in the Output folder.
------Output_name: The name of the converted motion file

After finishing the configuration files:
------To convert the motion file: please run "Motion_Convert.ipynb" in Jupyter notebook.
------To convert the grf file: please run "Force_Convert.ipynb" in Jupyter notebook. NOTICE: please change the start time and end time in the script to match with your desire. 