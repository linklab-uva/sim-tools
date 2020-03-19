## Sim-Tools: Experimental Offsite Learning

To connect to your team car, change the ROS network settings in `~/.bashrc`

```
export ROS_MASTER_URI=http://gpusrv05.cs.virginia.edu:11311
export ROS_IP=<your_IP_through_UVA_VPN>
```

Once connected, you should be able to read data using `rostopic echo $`, and all publish and subscribe functions will be able to communicate with your team car. To **only** visualize the data using `rviz`:

```
user@remote-computer: roslaunch sim-tools remote-access.launch \
> uva_ID:=<your_UVA_ID> \
> car_name:=<your_team_car_name> \
> visualize:=true \
> remote_teleop:=false
```

** Note: Only one computer per team can launch control nodes **
To control the car in addition to the visualization node, enter the following command:

```
user@remote-computer: roslaunch sim-tools remote-access.launch \
> uva_ID:=<your_UVA_ID> \
> car_name:=<your_team_car_name> \
> visualize:=false \
> remote_teleop:=true \
> listen_offboard:=<true/false>
```
