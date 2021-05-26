# testmay
- hosts: webservers
  become: true
  become_user: root
  tasks:
  - name: install python
    yum: name=python state=present
  - name: start python
    service: name=python state=started
  - name: deploy war file
       dest=/usr/share/python/webapps
   
