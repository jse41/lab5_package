<h1>Modern Robot Programming Lab 5</h1>
<h1>Purpose of the Lab</h1>
The purpose of this laboratory was to gain experience using ROS bags and message playback to view sensor data to display a 3D map. <br><br>

<h1>Launch Instruction</h1>
To launch new XACRO version of robot use <br>
<code>roslaunch lab4_package launch_file.launch</code><br>
You can also launch while in launch directory using <br>
<code>roslaunch launch_file.launch</code>

To launch lab 4 XACRO version of robot use code below. Otherwise XACRO for lab 5 will launch. The full path of the XACRO file can be passed into the launch file as well. <br>
<code>roslaunch lab4_package launch_file.launch use_old_xacro:=true</code><br>
If in launch directroy, you can use <br>
<code>roslaunch launch_file.launch use_xacro:=true</code><br><br>

Both versions launch with GUI and joint_state_publisher by default<br>
To disable both the gui and joint_state_publisher use <code>use_gui:=false</code> such as<br>
<code>roslaunch lab4_package launch_file.launch use_gui:=false</code><br>
If in launch directory, then it would be <br>
<code>roslaunch launch_file.launch use_gui:=false</code> <br><br>

External clock is NOT used by default. To use the external clock on start up, set use_sim_time:=true as shown via the code below. This code is meant to be used within the launch directory. <br>
<code>roslaunch launch_file.launch use_sim_time:=true</code> <br>
If set to true, one of the rosbags must be set to provide the external clock signal as shown below. This command is meant to be used within the rosbags directory<br>
<code>rosbag play --clock glennan_5_basic.bag /tf_trajectory:=/tf</code> <br><br>

<h1>General Comments</h1>
Even though this is lab5, some of the files are still named lab4 as I worked directly off of the previous lab files without creating a new folder. In the future I will try to avoid doing that to keep things consistent. Also I'm not sure if launching with <br>
<code>roslaunch lab4_package launch_file.launch</code><br>
Which is why I included how to do it from within the launch directory. In the future I will include the lab package folder itself on github.
