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
