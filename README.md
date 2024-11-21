# multi-rosbot-sim

Demo showing how to spawn multiple ROSbots in Gazebo

## Quick start

1. Pull Docker images with:

```bash
docker compose pull
```

2. start the simulation with:

```bash
xhost +local:docker && docker compose up
```

3. open a shell inside a docker container:

```bash
docker compose exec -it rosbot bash
```

4. for controlling `robot1` with teleop run:

```bash
ros2 run teleop_twist_keyboard teleop_twist_keyboard --ros-args -r __ns:=/robot1
```