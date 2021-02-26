# HOW TO USE THIS PROJET

1. You should clone this project in the src folder in your workspace

   To do this, use the command git clone as follows:

   `git clone https://github.com/MohammadZaheer/tp_ros_zaheer.git`

2. Now open a terminal and type the following command:

   `catkin build`

3. You must source your setup.bash. This step is very important. If you    skip this step, you will always have an error message "Project not found".

   There are two methods to do this.

   The first is to open a terminal and type the following command:

   `source ~/workspace_name/devel/setup.bash`

   Note: Replace `workspace_name` with the actual name of your workspace.

   You have to do this each time you open a new terminal. This method is not practical and time consuming and often people tends to forget to do it. This problem leads us to use the second option.

   The second option is to include it in the .bashrc file. You must do it only once.

   To do this, open a terminal and type the following command:

   `sudo nano ~/.bashrc`

   In this file, write `source ~/workspace_name/devel/setup.bash` BUT replace `workspace_name` with the actual name of your workspace.

   Save the modification and exit the file

4. Start the server(roscore) in another terminal

   This is done by using the command `roscore`

5. Now in the folder tp_ros_zaheer, there is two sub-folders:

   - src
   - launch

   In the src folder, there is a script called `pub.py`. You have to give this file the right of execution. To do this, on the terminal, type `chmod +x pub.py`

   In the launch folder, there is a file called `button_launch`

6. To launch the file `button_launch`, in the launch folder, open a terminal and type the followimg command:

   `roslaunch tp_ros_zaheer button_launch`

   After doing this step, you will notice that a small box will apear ann in it there will be a button named `toggle`. You can press on this button to change the state each time.

   You will also notice that rviz will open.

7. In rviz, do the following steps:

   1. Click on the option `Add`
   2. Under `By topic`, click on `Pose`

   You will see a PoseStamped that follows a specific path to make the design of the number `8`

   Each time you click on the button `toggle`, the state of the PoseStamped will change

8. To view the state of the button, open a new terminal and type `rostopic echo /button_state`

   




 


