# IsaacSim-exe

1. 단독으로 rviz2를 실행하고 싶을 때
터미널에 아래 명령어를 입력하여 ROS 2용 RViz를 실행합니다.

Bash
rviz2
2. 앞서 셋팅한 내비게이션 런치 파일로 실행할 때 (추천)
우리가 이전에 다루었던 turtlebot3_navigation2 런치 스크립트에는 내비게이션 노드들과 함께 ROS 2 버전에 맞는 rviz2를 자동으로 띄워주고, 맵과 로봇의 환경 설정(.rviz)까지 한 번에 로드해 주는 옵션이 있습니다.

새 터미널을 열고 아래와 같이 런치 파일을 다시 실행해 보세요. (use_rviz:=true 옵션이 ROS 2용 RViz 창을 자동으로 올바르게 띄워줍니다.)

Bash
# 1. 환경 소싱 및 모델 설정
cd /home/gotree94/IsaacSim-ros_workspaces/humble_ws
source install/setup.bash
export TURTLEBOT3_MODEL=waffle

# 2. 런치 파일 실행
ros2 launch turtlebot3_navigation2 navigation2.launch.py \
  map:=/home/gotree94/IsaacSim-ros_workspaces/humble_ws/src/navigation/carter_navigation/maps/carter_warehouse_navigation.yaml \
  use_rviz:=true

  
