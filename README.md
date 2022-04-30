# libuvc_camera_ros_sandbox

## Usage
Check the camera connetction and bus_id, device_id.
```sh
lsusb
```

Check the settings available on the camera.
```sh
v4l2-ctl --list-formats-ext
```

Change the camera permissions. It is also possible to add udev and change the permissions.
```sh
sudo chmod 666 /dev/bus/usb/bus_id/device_id
```

launch
Change config/test_params.yaml depending on your camera.
```sh
roslaunch libuvc_camera_ros_sandbox test.launch
```

# Dependencies
Refer to package.xml to install the required dependent packages.
```sh
cd ~/catkin_ws
rosdep install -i --from-paths src/libuvc_camera_ros_sandbox
```