# mysql iamge:

take mysql:8.0 as base iamge and set root passowrd

df -hT

concepts > Resize EBS storage

ifconfig > ent5 (docker neetwork)

![alt text](docker-nw-diagram.drawio.svg)

At home, computers, mobiles, smart TV and evry electric devices which connects to internet will get IP address from ISP and router will manage each device.


![alt text](ifconfig.GIF)
Docker Network:

in the above screenshot AWS ISP provides internet to our server.
every VM get access to internet from AWS ISP and IP address is 172.31.29.156  

docker created one virtual network that is docker0, it acts like modem to the containers inside VM. docker0 will allocate IP address to containers.

this is called bridge network.

 

docker containers cant be communicated using default network.
docker network --hlep
docker network create expense  --> bridge network
docker network ls
ifconfig
docker network connect expense mysql

docker network disconnect bridge msyql
docker run -d ==network expense --name backend backend:v1

apt update
apt install telnet
telnet mysql 3306
apt remove telnet -y

docker run -d -p 80:80 --network expense --name frontend frontend:v1