# Test with Artdc

## How to use

Take a look at `Makefile`, and update variables as you need. The default container
is Ubuntu 14.04, and the default variables are set to work for the default environment
of the Docker Toolbox on Mac OS X.

If your docker machine is your localhost, the following setting should work:

```
docker_machine_ip = 127.0.0.1
docker_config =
```

If you're using Docker for Mac, the following setting should work:

```
docker_machine_ip = 192.168.64.2
docker_config =
docker_ssh_timeout = 30
```

> **Note:** On Docker for Mac, it somehow takes long for Ansible to log in to container,
> and the default timeout(10 seconds) isn't long enough on my MacBook. That's the reason
> I set the timeout as 30 seconds.

Here's the commands

```bash
# Initialize the environment
$ ./artdc.sh init

# Test your playbook
$ ./artdc.sh provision

# Log into the container
$ ./artdc.sh ssh

# Destroy container and provision it from scratch
$ ./artdc.sh reprovision

# Clean container and image
$ ./artdc.sh clean
```
