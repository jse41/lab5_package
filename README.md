<h1>Modern Robot Programming Lab 5</h1>
<h1>Purpose of the Lab</h1>
The purpose of this laboratory was to gain experience using ROS bags and message playback to view a map with sensor data that was taken within the mapped area. <br><br>

<h1>General Comments</h1>
I included how to launch the simulator from within the launch directory just in case. In the future I will include the lab package folder itself on github. I didn't include the rosbags or the maps as they are somewhat confidential. <br> <br>
I left some irrelevant files in the urdf folder such as robot.xml and robot.bak as they were mostly leftover from the last lab. In the launch folder there is also a file called launch_file that isn't used in the lab, but that was the original code provided. The code that is used in my package is launch_file.launch. I didn't delete these files yet as I don't want any issues when pushing my files to github but they may be deleted as the deadline nears.<br><br>

<h1>Launch Instruction</h1>
To launch the new lab 5 XACRO version of robot use <br>
<code>roslaunch lab5_package launch_file.launch</code><br>
You can also launch while in launch directory using <br>
<code>roslaunch launch_file.launch</code>

To launch the old lab 4 XACRO version of robot use code below. Otherwise XACRO for lab 5 will launch. use_old_xacro determines whether lab4 or lab5 version will launch, and it is set to false by default so it launches lab5. The full path of the XACRO file can be passed into the launch file as well. <br>
<code>roslaunch lab5_package launch_file.launch use_old_xacro:=true</code><br>
If in launch directroy, you can use <br>
<code>roslaunch launch_file.launch use_xacro:=true</code><br><br>

Both versions launch with GUI and joint_state_publisher by default<br>
To disable both the gui and joint_state_publisher use <code>use_gui:=false</code> such as<br>
<code>roslaunch lab5_package launch_file.launch use_gui:=false</code><br>
If in launch directory, then it would be <br>
<code>roslaunch launch_file.launch use_gui:=false</code> <br><br>

External clock is NOT used by default. To use the external clock on start up, set use_sim_time:=true as shown via the code below. This code is meant to be used within the launch directory. <br>
<code>roslaunch launch_file.launch use_sim_time:=true</code> <br>
If set to true, one of the rosbags must be set to provide the external clock signal as shown below. This command is meant to be used within the rosbags directory<br>
<code>rosbag play --clock glennan_5_basic.bag /tf_trajectory:=/tf</code> <br><br>

<h1>Video</h1>
I provided an edited video named lab5_video.mp4 which shows the following: <br>
-rvis launching <br>
-the rosbag starting <br>
-the mapserver starting<br>
-changing the "Fixed Frame" to the base<br>
-adding the 3 lasers to view the sensor data<br>
-changing the decay rate to 10<br>
-showing all links are working successfully

<h1>Other</h1>
<a href="https://github.com/mjh244/lab5_package"> Original Package </a>
Most of this lab was done following an unconventional naming scheme that impacted its ability to be run across platforms, so this package was created to resolve those issues. For this reason, if any runtime errors are to occur, please reference the original package and its README for how to configure the origial package. Both packages were written by students of this lab group. 

