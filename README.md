# testmay
- hosts: webservers
  become: true
  become_user: root
  tasks:
  - name: install docker
   yum: name=docker state=present
- name: start docker
service:  name=docker state=started
 - name: install git
    yum: name=git state=present
  - name: get the dockerfile from githib
    git: repo=https://github.com/darshanarn26/testmay.git dest=/tmp/gitrepo
    - name: build dockerfile
    command: chdir=/tmp/gitrepo docker build -t deployimage:ubuntu
- name: Pull the image from docker hub
get_url:
 url=https://hub.docker.com/_/ubuntu
  - name: run the docker image
    command: docker run -itd -P deployimage:ubuntu
   - name: port mapping for the image 
   command:  docker run --name c1 -d -p 8888:80 ubuntu 
  

   
