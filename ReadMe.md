# Vision Development Environment

## Overview

This is the Vision Development Environment for the Laboratory at the CTEx. We plan to develop vision algorithms for the SVTRP Project, helping to manipulate hazardous materials with a robotic arm.

## System Requirements

- Docker Engine
- Nvidia Container Toolkit

## System Specification

- Ubuntu 22.04
- ROS2 Humble


# Installation

First, clone this repository:

    git clone https://github.com/wenisbelle/vision_dev_env.git

Then, build the docker image:

    docker build -t vison_dev .

Now, create the container:

    docker compose up --build --detach

We need also to run the following command to give the container access to the display:

    xhost +local:

To interact with the container, just run:

    docker exec -it vision_dev_container /bin/bash