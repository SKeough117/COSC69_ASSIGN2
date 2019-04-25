# COSC69_ASSIGN2
Sean Keough
Professor Alberto Quattrini Li
Spring 2019


This program is designed as a program to allow a Turtlebot3 to connect to a Wifi source, and then approach that source and
attempt to follow it. The downloads include a tar.gz file and you'll have to have at least two Turtlebots.

1. First, start up your turtlebots and open up the zip file, with the package called follow_source.

2. Start up your roscore and then connect to your "follower" turtlebot via SSH ($~ ssh dartmouth@192.168.1<turtle id>.<turtle id>)

3. Once you're into your turtlebot, ensure that the networking is using the OTHER turtlebot as it's wifi "source." This will 
effectively make the other turtlebot our hypothetical wifi source, which we will be seeking out.

4. Before trying to run your command, you need to make sure that our package is on the turtlebot. You can do this with the
command line (of the computer, not turtlebot), typing: $ scp -r src/follow_source dartmouth@192.168.1<turtle id>.<turtle id>
Note: For all future code changes you want on the turtlebot simply command line: $ rsync -rav src/follow_source dartmouth@192.168.1<turtle id>.<turtle id>

5. Now that our files are on the turtlebot, all we have to do is launch one launch file to both initialize the follower node as
well as setup our turtlebot. The file is called follow_source.launch.

(Alternative) 6. If the above command does not work, bringup and launch the turtlebot with the following commands:
$ roslaunch turtlebot3_bringup turtlebot3_robot.launch
$ rosrun follow_source follower_node.py

7. At this point, your robot should be trying to explore its environment to identify where the wifi source is.
