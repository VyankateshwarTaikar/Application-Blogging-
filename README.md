# Steps for Demo

1. Create Github Secerct access token  & keep safe with you 

# Create AWS VM 
 Ubuntu  ( 2 server-SonarQubes & Nexus )==>t2.medium ,(Common key pay pair) , storage = 20 Gb

Ubuntu  ( 2 server-jenkins & Nexus )==>t2.medium ,(Common key pay pair) , storage = 20 Gb

Ubuntu  (1 jenkins  )==>t2.large ,(Common key pay pair) , storage = 25 Gb 

##  Security group should be open :  25 , 80 , 443 , 2000-3000 , 22, 6443, 465 

![Screenshot_2](https://github.com/user-attachments/assets/92f51c4b-5bfe-469e-8b8c-2255856aab11) 


# connect to the servers 
Update all the servers by 

``` sudo apt update ```

# Jenkins Server :
- install Java17
  
```  sudo apt install openjdk-17-jre-headless    ```

-install jenkins  

Go tho the jenkins official website & copy it 

# Create file, paste it & run the file 

```  sudo wget -O /usr/share/keyrings/jenkins-keyring.asc \
  https://pkg.jenkins.io/debian-stable/jenkins.io-2023.key
echo "deb [signed-by=/usr/share/keyrings/jenkins-keyring.asc]" \
  https://pkg.jenkins.io/debian-stable binary/ | sudo tee \
  /etc/apt/sources.list.d/jenkins.list > /dev/null
sudo apt-get update
sudo apt-get install jenkins   ```

![image](https://github.com/user-attachments/assets/61abc18a-9845-4b0e-99dd-5de07a542944) 

![image](https://github.com/user-attachments/assets/3e3d6554-a646-4689-9b49-08f160aece1c) 



