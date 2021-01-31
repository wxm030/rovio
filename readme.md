# build 
mkdir catkin_ws/src
cd src
git clone git@github.com:wxm030/rovio.git
cd rovio
git submodule update --init --recursive
cd catkin_ws
catkin build rovio --cmake-args -DCMAKE_BUILD_TYPE=ReleaseWithInfo

# run
source devel/setup.bash
roslaunch rovio  rovio_rosbag_node.launch

