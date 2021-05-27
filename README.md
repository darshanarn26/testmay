# testmay
- hosts: webservers
  become: true
  become_user: root
  tasks:
  - name: install docker
   yum: name=docker state=present
-name: start docker
service:  name=docker state=started
-name: Pull the image from docker hub
get_url:
 url=https://hub.docker.com/_/ubuntu
  - name: run the docker image
    command: docker run -itd -P deployimage:ubuntu
   - name: port mapping for the image 
   command:  docker run --name c1 -d -p 8888:80 ubuntu 
  

   
