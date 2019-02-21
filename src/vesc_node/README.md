# vesc
Vesc ros driver for FW 3.33 -> ?

Minor changes:
1. Updated vesc/vesc_driver/include/vesc_driver/datatypes.h (added COMM_SET_HANDBRAKE to match FW)
2. Updated vesc/vesc_driver/src/vesc_packet.cpp (rearrange bytes to match FW)

To read the rotor position (radians):
rostopic echo /sensors/rotor_position

To control motor position (radians):
rostopic pub -r 20 /commands/motor/position -- std_msgs/Float64 3.9

To view sensor information:
rostopic echo /sensors/core
