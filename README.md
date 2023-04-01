# gitlab-runner-demo

This repository contains an example setup of a gitlab runner, which utilizes docker and sysbox.
Normal jobs can be executed inside of a standard docker container. Jobs requiring access to docker itself can utilize sysbox, and use a dind image, or the already setup docker service out of the box.
This ensures that all jobs are isolated between each other and the host, without requiring privileged containers or similar widespread solutions. 

## Setup
- Install Docker
- Install Sysbox: https://github.com/nestybox/sysbox#installation
- Install ShiftFs: https://github.com/nestybox/sysbox/blob/master/docs/user-guide/install-package.md#installing-shiftfs
- Obtain two runner tokens from gitlab and insert them in the config.toml
- Deploy the docker-compose stack
