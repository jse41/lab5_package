<h1>Modern Robot Programming Lab 4</h1>
<h1>Purpose of the Lab</h1>
The purpose of this laboratory was to create a robot from a robot description using URDF, XACRO, and ROS utilities to perform transforms. <br><br>

<h1>Launch Instruction</h1>
To launch urdf version of robot use <br>
<code>roslaunch lab4_package launch_file.launch</code><br><br>

To launch xacro version of robot use <br>
<code>roslaunch lab4_package launch_file.launch use_xacro:==true</code><br><br>

Both versions launch with GUI and joint_state_publisher by default<br>
To disable both the gui and joint_state_publisher use <code>use_gui:=false</code> such as<br>
<code>roslaunch lab4_package launch_file.launch use_gui:=false</code><br><br>

<h1>General Comments</h1>
The 3 lasers for the xacro version gave me a strange red mesh. I also had manually adjust the base of the robot as it was off and didn't see any instructions on how to correct it.
