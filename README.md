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
  
  
  
  

   
Pipeline Code

pipeline{
    tools{
        ansible 'myansible'
    }
    agent any
    stages{
        stage('checkout'){
            steps{
                git 'https://github.com/darshanarn26/testmay.git'
'
            }
        }
        stage('compile'){
            steps{
                sh 'ansible compile'
            }
        }
        stage('codeReview'){
            steps{
                sh 'ansible pmd:pmd'
            }
        }
        
       
        stage('unitTest'){
            steps{
                sh 'ansible test'
            }
        }
        
        stage('package'){
            steps{
                sh 'ansible package'
            }
            
        }

    }
}


 Public class TestCase1
{
@Test
public void setupmethod()
{
WebDriver driver=new ChromeDriver();
driver.manage().window.maximize();
driver.get("https://github.com/darshanarn26/testmay.git
")
}
@Test
public void Testpage()
{
driver.findElement(by.xpath("//input[@id='searchInput']")).clear();
driver.findElement(by.xpath("//input[@id='searchInput']")).sendKeys("Selenium Automation");

}

}
