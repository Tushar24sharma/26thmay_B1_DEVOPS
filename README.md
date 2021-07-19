Day17 Task:

# Install docker
### sudo apt-get update

Fetched 114 kB in 0s (317 kB/s)                      
Reading package lists... Done
ubuntu@ip-172-31-63-211:~$ sudo apt-get install \
>     apt-transport-https \
>     ca-certificates \
>     curl \
>     gnupg \
>     lsb-release
Reading package lists... Done
Building dependency tree       
Reading state information... Done
lsb-release is already the newest version (11.1.0ubuntu2).
ca-certificates is already the newest version (20210119~20.04.1).
curl is already the newest version (7.68.0-1ubuntu2.5).
gnupg is already the newest version (2.2.19-3ubuntu2.1).
apt-transport-https is already the newest version (2.0.6).
0 upgraded, 0 newly installed, 0 to remove and 81 not upgraded.
ubuntu@ip-172-31-63-211:~$ curl -fsSL https://download.docker.com/linux/ubuntu/gpg | sudo gpg --dearmor -o /usr/share/keyrings/docker-archive-keyring.gpg
echo \
  "deb [arch=amd64 signed-by=/usr/share/keyrings/docker-archive-keyring.gpg] https://download.docker.com/linux/ubuntu \
  $(lsb_release -cs) stable" | sudo tee /etc/apt/sources.list.d/docker.list > /dev/nullubuntu@ip-172-31-63-211:~$ sudo apt-get update
Hit:1 http://us-east-1.ec2.archive.ubuntu.com/ubuntu focal InRelease
Hit:2 http://us-east-1.ec2.archive.ubuntu.com/ubuntu focal-updates InRelease                           
Hit:3 http://us-east-1.ec2.archive.ubuntu.com/ubuntu focal-backports InRelease                         
Hit:4 http://security.ubuntu.com/ubuntu focal-security InRelease                                       
Get:5 https://download.docker.com/linux/ubuntu focal InRelease [52.1 kB]  
Get:6 https://download.docker.com/linux/ubuntu focal/stable amd64 Packages [9960 B]
Fetched 62.1 kB in 0s (148 kB/s)
Reading package lists... Done
 ###sudo apt-get install docker-ce docker-ce-cli containerd.io
 
 <img src=dockerinstall.png>
 <img src=pull.png>
 
 ##start pause and stop the docker container
 sudo docker run ubuntu:20.04 sleep 100
sudo docker pause Docker_name 
sudo docker unpause Docker_name 
sudo docker stop Docker_name

 #GET BASH OF THE CONTAINER
 
 ## sudo docker exec -it container_name bash
 
 <img src=bash.png>
