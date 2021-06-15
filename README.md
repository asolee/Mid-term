# Mid-term
This repository is an exercise of BDP2 course

# docker command

**docker run -p 80:8888 asolega/mid-term:latest**

use this command for run a container with the new images created, use -p to specify the port exposed and insert the username and repository of the image in docker hub

# docker run WITH bind mount

**docker run -p 80:8888 -v <host volume>:<container volume> <user ID>/<docker repo>**

the new command include the flag -v, used to sicronize the host volume with the container volume.
with this command we are able to save locally the changes in a specific volume of the container.

in my case the command is:
**docker run -p 80:8888 -v /home/ubuntu/review/Mid-term/work:/home/jovyan/work asolega/mid-term**

in case of permiss denied errors try to use this command to give permiss to the user
**sudo chown -R user <host volume>  

# docker-compose-yml

to complete this part we create forst of all dowload the docker-compose with this command

**sudo apt update && sudo apt install -y docker-compose**

then we add the file docker-compose.yml in the main directory, this file contain important informations used by docker-compose to run multiple containers.
download docker-composer.yml

**wget https://raw.githubusercontent.com/asolee/Mid-term/main/docker-compose.yml**
  
 we set the correct build volume, in this way the portainer can acess directly to the VM1, and jupyter notebooks are saved in the host folder /work.
  
 then we use the token found in the portainer to access on jupyter:
 <img width="1440" alt="Screenshot 2021-06-15 at 17 48 21" src="https://user-images.githubusercontent.com/85689006/122086833-5f5c2f00-ce04-11eb-9612-cbeb20c47189.png">

  
  

