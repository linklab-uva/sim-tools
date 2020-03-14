## Sim-Tools: Experimental Offsite Learning

To connect to your team car, change the ROS network settings in `~/.bashrc`

```
export ROS_MASTER_URI=http://172.27.99.242:11311
export ROS_IP=<your_IP_through_UVA_VPN>
```

Once connected, you should be able to read data using `rostopic echo $`, and all publish and subscribe functions will be able to communicate with your team car. To visualize the data using `rviz`:

```
user@remote-computer: roslaunch sim-tools remote-access.launch car_name:=<your_team_car_name>
```
