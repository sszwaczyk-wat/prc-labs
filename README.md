# prc-labs

A Docker container for Programming in C labs in Military University of Technology.

## Usage

In order to facilitate the use of this image, scripts are provided to run, attach, and stop the container. The scripts are available through the github repository (https://github.com/sszwaczyk/prc-labs.git) to get execute the command:

``` git clone https://github.com/sszwaczyk/prc-labs.git```

1. Run container:  
```./run.sh```  
or  
```xhost +```  
```docker run -tid --privileged --rm -e DISPLAY=$DISPLAY -v /tmp/.X11-unix:/tmp/.X11-unix --name=prc-labs sszwaczyk/prc-labs```  

2. You can attach to running container using:  
```./attach.sh```  
or  
```docker exec -t -i prc-labs bash -c 'su student'```  

3. Also you can can connect via SSH protocol:  
```./attach_ssh.sh```  
or  
```ssh -X -o UserKnownHostsFile=/dev/null -o StrictHostKeyChecking=no student@<container_ip>```  

4. Start eclipse when you attached to conatiner:  
```$ eclipse```  
or using script:  
```./eclipse_student.sh```  
or run as root user:  
```./eclipse_root.sh```  

