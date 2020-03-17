# prc-labs

A Docker container for Programming in C labs in Military University of Technology.

## Requirements

It is recomennded to use this environment on Linux operating system (Ubuntu or Debian). It is not tested on Windows systems.

### Git

To install git:

```sudo apt-get install git```

### Docker

To install docker run commands:
- Ubuntu (https://docs.docker.com/install/linux/docker-ce/ubuntu/):
```
sudo apt-get remove docker docker-engine docker.io containerd runc
sudo apt-get update
sudo apt-get install apt-transport-https ca-certificates curl gnupg-agent software-properties-common
curl -fsSL https://download.docker.com/linux/ubuntu/gpg | sudo apt-key add -
sudo apt-key fingerprint 0EBFCD88
sudo add-apt-repository "deb [arch=amd64] https://download.docker.com/linux/ubuntu $(lsb_release -cs) stable"
sudo apt-get update
sudo apt-get install docker-ce docker-ce-cli containerd.io
sudo docker run hello-world
```
- Debian (https://docs.docker.com/install/linux/docker-ce/debian/)
```
sudo apt-get remove docker docker-engine docker.io containerd runc
sudo apt-get update
sudo apt-get install apt-transport-https ca-certificates curl gnupg2 software-properties-common
curl -fsSL https://download.docker.com/linux/debian/gpg | sudo apt-key add -
sudo apt-key fingerprint 0EBFCD88
sudo add-apt-repository "deb [arch=amd64] https://download.docker.com/linux/debian $(lsb_release -cs) stable"
sudo apt-get update
sudo apt-get install docker-ce docker-ce-cli containerd.io
sudo docker run hello-world
```

For other systems see: https://docs.docker.com/install/

## Usage

In order to facilitate the use of this image, scripts are provided to run, attach, and stop the container. The scripts are available through the github repository (https://github.com/sszwaczyk/prc-labs.git) to get execute the command:

``` git clone https://github.com/sszwaczyk/prc-labs.git```

1. Run container:  
```./run.sh```
If you run it first time it might take a while to download docker image from repository. It will also connect you to running container console.

2. You can attach to console of running container using:  
```./attach.sh```

3. Start eclipse when you attached to conatiner:  
```$ eclipse```  
or using script:  
```./eclipse_student.sh```  
or run as root user:  
```./eclipse_root.sh```


