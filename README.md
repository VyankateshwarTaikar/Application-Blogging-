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


 






