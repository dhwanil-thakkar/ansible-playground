### Example Usage for Building the Docker Image
``` 
sudo docker build -t ansible_child .  
```

### Example Usage for Running the Docker
```
sudo docker run -d --name="child2" ansible_child
```
### The Dockerfile file
- This file is how the docker is built, any additonal thing that needs to be packed into the container image could be added there. 
- The default user created is **john** with the password **doe**. You can change the user/password on this file.

### The sshd_config file
- The sshd_config file is used to setup the ssh connection required for ansible to work with.  

- Setting up a file helps with manintaing consistency instead of using default files and can also be customized to need.

### The id_rsa.pub file 
 - This file is intended to hold the public key that you would like to use to authenticate ansible commands with, this file will be built into the docker image.
