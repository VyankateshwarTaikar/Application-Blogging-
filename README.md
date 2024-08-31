# Steps for Demo

1. Create Github Secerct access token  & keep safe with you 

# Create AWS VM 
 Ubuntu  ( 2 server-SonarQubes & Nexus )==>t2.medium ,(Common key pay pair) , storage = 20 Gb

Ubuntu  ( 2 server-jenkins & Nexus )==>t2.medium ,(Common key pay pair) , storage = 20 Gb

Ubuntu  (1 jenkins  )==>t2.large ,(Common key pay pair) , storage = 25 Gb 

##  Security group should be open :  25 , 80 , 443 , 2000-3000 , 22, 6443, 465 , 8080, 8081, 9000

![Screenshot_2](https://github.com/user-attachments/assets/92f51c4b-5bfe-469e-8b8c-2255856aab11) 


# connect to the servers 
Update all the servers by 

``` sudo apt update ```

 ## 1. Jenkins Server :
- install Java17
  
```  sudo apt install openjdk-17-jre-headless    ```

-install jenkins  

Go tho the jenkins official website & copy it 
web : https://www.jenkins.io/doc/book/installing/linux/ 

## Create file, paste it & run the file 

![image](https://github.com/user-attachments/assets/2a1b6599-6dc6-4a21-b283-0053287ab787) 

![image](https://github.com/user-attachments/assets/befd40cf-1016-4074-878a-5ba129ffb63e)


![image](https://github.com/user-attachments/assets/18126c18-93cc-4638-b036-c54381165790)

![image](https://github.com/user-attachments/assets/e2a0436c-69c8-4416-b7a4-9c32cada195d)


## run the jenkins & start the installation 

![image](https://github.com/user-attachments/assets/52e02e19-f30c-48a7-80d2-dd39d6a59818)

![image](https://github.com/user-attachments/assets/7bb57afe-9942-4906-bedc-c98adf2114d3)

Install these plugins 

![image](https://github.com/user-attachments/assets/e3ab3262-836d-4ecb-b494-57e17d63548d)


Go to the Dashboard > Manage jenkins > Tools 

 ![image](https://github.com/user-attachments/assets/dceb1a4c-d193-4936-80c0-392ce7641014)

 ![image](https://github.com/user-attachments/assets/491cdef2-d802-408d-b91d-47bd5978ee4c)

![image](https://github.com/user-attachments/assets/3de8066d-50d6-497b-94e8-174e824f3bc0)

 ![image](https://github.com/user-attachments/assets/1bea6dd3-ee69-4c42-aed4-c12cc8ceaf8d)


## For Nexus :
- Sudo apt update 

- Nexus create by docker container

![image](https://github.com/user-attachments/assets/4fb28263-d243-40a5-8e3a-ce48a40db2aa) 

create container 

![image](https://github.com/user-attachments/assets/eb03378d-1e26-4543-a8cc-f68bcab0f0cf) 

![image](https://github.com/user-attachments/assets/fe7816aa-e1b3-456b-8bb6-60ecd492706f)


![image](https://github.com/user-attachments/assets/76f5fa67-7999-42dc-bc85-ed7344cb6cb7)

## login inside nexus container & keep safe the nexus password with you 

![image](https://github.com/user-attachments/assets/2bc9a198-ccd6-4cb0-92a0-934b601bef54)

![image](https://github.com/user-attachments/assets/7c379055-0df9-4c7b-b3bb-86a2dd71eb7d)



## for same thing do with SonarQube

$ sudo apt update 

- install docker on machine & then SonarQube container 

![image](https://github.com/user-attachments/assets/6fd23cdb-f00c-43a1-8f12-f7241e8b1af0) 

login to SonarQube Server : by default ID & passwords are same as  :  admin 

![image](https://github.com/user-attachments/assets/6faf03db-a447-4bcb-9e89-7064b51460eb)


Genrate the token :

Administration > security > genrate the token 

![image](https://github.com/user-attachments/assets/2e66823c-4e16-41a5-90f8-7ecfac446612)


keep these token safe with you .



## writing the CICD pipeline 

go to dashboard > name : Blogging-App > select pipeline 

when you are writing pipelines and you are going to utilize lot of plugins tools right that means like maybe have configured Java we have configured MAVEN or so whichever plugin you want to utilize within your pipeline you need to manually Define it somewhere there are multiple ways of defining for example one way of defining MAVEN and Java is that I can use tools block inside that I can provide the details of that for example 


 1. Go to the script & choose the hello world

![image](https://github.com/user-attachments/assets/189f1b78-1301-4ab9-ae4a-16cd95d2951e)

    
![image](https://github.com/user-attachments/assets/45ca16dc-f3ae-48d2-afdf-6d3cb29cbc76) 

2. Do the Git checkout for that purpose choose pipeline syntax
   sample step : git:Git
   insert the Repository URL
   choose proper branch (main or master)
   Add the Credential (if not then add ) -for adding putting username as GithubUserName & password will be genrated Screct accesss token 

![Screenshot_22](https://github.com/user-attachments/assets/8cfabc8e-9a5d-4941-99fd-a91e6d5af3e4)


![Screenshot_23](https://github.com/user-attachments/assets/a8f00d00-49aa-44a8-83f2-8828330dbbf0)

![Screenshot_24](https://github.com/user-attachments/assets/f483fbf9-0c87-487b-8d0f-a3d99dfbb3ed)

## Now, install trivy on jekins server 

link: https://aquasecurity.github.io/trivy/v0.18.3/installation/#debianubuntu


![Screenshot_25](https://github.com/user-attachments/assets/62e9cbb2-061a-4446-8757-92e7d1f6f3cc)

![image](https://github.com/user-attachments/assets/6ed09edc-afcf-40b3-9a57-701afc0b5251)






