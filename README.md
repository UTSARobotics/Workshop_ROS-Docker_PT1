# __Docker on windows__

# WLS2 install
### Install WSL on windows
- Paste this next line into your windows terminal
```
wsl --install
```
### or (if already installed) 
- This will update your "Windows Subsystem for Linux" if you already have it installed
```
wsl --update
```
### Install Docker Desktop
- Go to this website and download the appropriate Docker Desktop installation
```
https://docs.docker.com/desktop/setup/install/windows-install/
```
### Reboot computer when asked to
#   Docker-intructions
### Test that docker is running correctly
```
docker run hello-world
```
## Run test docker container on windows
```
docker run -it --rm -v /run/desktop/mnt/host/wslg/.X11-unix:/tmp/.X11-unix -v /run/desktop/mnt/host/wslg:/mnt/wslg -e DISPLAY=:0 -e WAYLAND_DISPLAY=wayland-0 -e XDG_RUNTIME_DIR=/mnt/wslg/runtime-dir -e PULSE_SERVER=/mnt/wslg/PulseServer utsarobotics/ros2-humble:1.0.0 bash
```
