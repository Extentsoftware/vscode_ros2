FROM althack/ros2:galactic-dev 

# ** [Optional] Uncomment this section to install additional packages. **
#
RUN apt update
ENV DEBIAN_FRONTEND=noninteractive
RUN apt-get update 
RUN apt-get -y install --no-install-recommends ubuntu-desktop mesa-utils
RUN apt-get -y install --no-install-recommends ros-galactic-rviz2
RUN apt-get -y install --no-install-recommends ros-galactic-rqt ros-galactic-rqt-common-plugins
RUN apt-get autoremove -y 
RUN apt-get clean -y 
RUN rm -rf /var/lib/apt/lists/*
ENV DEBIAN_FRONTEND=dialog

# Set up auto-source of workspace for ros user
ARG WORKSPACE
RUN echo "if [ -f ${WORKSPACE}/install/setup.bash ]; then source ${WORKSPACE}/install/setup.bash; fi" >> /home/ros/.bashrc