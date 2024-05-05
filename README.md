# Edge Computing Project
Student Name:-Nilay Mahajan  Sudent Number:-23211073

Student Name:-Emuru Geyasree  Sudent Number:-23211073

# Introduction:
5G networks demand ultra-low latency and higher bandwidth, driving the emergence of edge computing paradigms like MEC and Fog computing. These bring storage and processing capabilities closer to mobile networks, enabling versatile services for IoT deployments. Lightweight virtualization enhances edge infrastructure, while mobile offloading extends battery life and enables sophisticated services beyond device capabilities, defining the future of edge computing.



# Tasks to perform
1.to understand the significance of lightweight virtualization for edge computing 

2.to learn basic knowledge of docker virtualization technology 

3.to develop a dockerized environment emulating an edge computing platform

4.to establish an edge-to-edge connectivity between two docker containers 

5.to develop a mobile offloading scenario in the established edge platform 

# TASKS

Task1:Basic Docker Virtualization

In this first we created a dockerized environment using VM and ran 3 well-known docker images from the docker hub.i.e(hello-world, BusyBox, Nginx)
![image](https://github.com/NIlayMahajan/wireless_edge_computing/assets/150139448/75183ba5-7e41-4873-9530-31fb3e00dcc3)

Fig 1 : Running hello-world image 

![image](https://github.com/NIlayMahajan/wireless_edge_computing/assets/150139448/1ce74c60-0ec3-415f-a454-c431fd318d6d)

Fig 2: Running BussyBox image

![image](https://github.com/NIlayMahajan/wireless_edge_computing/assets/150139448/fb4b5109-63b7-41b2-ae1b-d82e1008291c)

Fig 3: Running Nginx

![image](https://github.com/NIlayMahajan/wireless_edge_computing/assets/150139448/902b33a2-742c-43bc-87c2-f033b44295cc)

Fig 4 :We displayed all the containers that were used.

![image](https://github.com/NIlayMahajan/wireless_edge_computing/assets/150139448/6089d630-4868-49b1-b0d6-49a5523c15ec)

Fig 5:All the images and containers were removed


The basic nginx webserver is pulled 

![image](https://github.com/NIlayMahajan/wireless_edge_computing/assets/150139448/70c0f63e-6c6e-4143-a25f-51dcbfc6cea9)



The customized HTML code is saved in nano to get a  webpage to display the group members.Upon saving and running this code a webpage is displayed

![image](https://github.com/NIlayMahajan/wireless_edge_computing/assets/150139448/414da002-6807-4bf5-a12b-b5b91d8d76ed)

![image](https://github.com/NIlayMahajan/wireless_edge_computing/assets/150139448/f1672cc4-1cd0-4c74-8635-740be94eda7f)



A basic ubuntu container is pulled and linux package inside  the container (nano) is installed.
![image](https://github.com/NIlayMahajan/wireless_edge_computing/assets/150139448/56c5bcd1-8f0b-48c3-a6c7-e4d39bb094f8)

A directory with “my-group” name inside the container is created. Members.txt is the text file which includes the members names is created inside the container.
![image](https://github.com/NIlayMahajan/wireless_edge_computing/assets/150139448/976a9575-b43f-477d-9d78-2e41c897ef5b)
Fig: Text file with members names

https://hub.docker.com/r/geyasree/my-ubuntu-custom/tags On committing the container ,and the image is pushed to the cocker hub.

![image](https://github.com/NIlayMahajan/wireless_edge_computing/assets/150139448/63510ab3-6e83-42f6-9550-fc2b5f98693e)

# Task2: Docker Networking:
Three containers are created with names alpine, alpine1 and alpine2
![image](https://github.com/NIlayMahajan/wireless_edge_computing/assets/150139448/fc37dfd2-5abd-4b8a-9f2c-31c408649420)
Since the containers are running in background ,docker attach is used to connect to alpine, apline1 and alpine2 .

With inspect bridge , the IP addresses of each container are know, and used to ping with the other containers.

During pinging -c 2 flag limits the command to two ping attempts, where the pings were successful.
![image](https://github.com/NIlayMahajan/wireless_edge_computing/assets/150139448/fe05db36-6ee3-4491-86f1-c5e2f11324d4)


we created a simple python scripts for server(ipc_server.py) and client(ipc_client.py)  for sockets-based IPC and tested the scripts. A file called ‘Dockerfile’ in the same directory as Python scripts .
![image](https://github.com/NIlayMahajan/wireless_edge_computing/assets/150139448/fcaf72da-261a-4257-b388-604de332fc9a)
Upon running the commands of server and client on different terminal, the message ‘Hello, world. IPC success!’ printed on the terminal of client. The message is simply echoed by the server.

We have been successful in demonstrating the  IPC using sockets in Python between a container that is running the server code and a client script running on the host.
But we were unable to the part , where client Python script is inside another container and demonstrate IPC between containers.
Since we were unbale to create a connection , we were unbale to calculate the mean median and standard deviation.













