


# LOGIN 
## 1.Open Git Bash:
  Open Git Bash on your Windows machine. If you don't have Git Bash installed, you can download it from https://gitforwindows.org/.

## 2.Navigate to the Directory Containing Your SSH Key (Optional):
If you have an SSH key, navigate to the directory containing your private key 
cd ~/.ssh)
ls ~/.ssh
ssh <username>@<public-ip>

## 3. IF U are not able to access ssh file then u have to give whole path
ssh -i path/to/your/private-key.pem <username>@<public-ip>
# EXAMPLE 
ssh -i "C:/Users/ak meena/Downloads/first-vm_key.pem" azureuser@20.213.20.220

## 4. change permissions if required
chmod 600 ~/.ssh/first-vm_key.pem
This command sets the file permissions to read and write only for the owner.


# 5. now u logged in ubantu virtual machine



# Now we have created and connected to vm  now wee will learn how to deploy it and access from internet 
 lets deploy jenkins application:-
  Jenkins is a powerful and versatile tool for automating various aspects of the software development lifecycle, contributing to the adoption of modern CI/CD practices in software development 
  teams.

## Install Jenkins.
  
### Pre-Requisites:
Java (JDK)

Run the below commands to install Java and Jenkins

### Install Java
sudo apt update
sudo apt install openjdk-11-jre

### Verify Java is Installed
java -version

### Now, you can proceed with installing Jenkins
curl -fsSL https://pkg.jenkins.io/debian/jenkins.io-2023.key | sudo tee \
  /usr/share/keyrings/jenkins-keyring.asc > /dev/null
echo deb [signed-by=/usr/share/keyrings/jenkins-keyring.asc] \
  https://pkg.jenkins.io/debian binary/ | sudo tee \
  /etc/apt/sources.list.d/jenkins.list > /dev/null
sudo apt-get update
sudo apt-get install jenkins

### To check jenkins runnig port 
 ps -ef | grep jenkins

 ### Test locally
Access your application locally on the VM using the VM's private IP address or localhost. Open a web browser and navigate to http://localhost or http://<private-ip>.
example:- http://localhost/8080

By default all ports in azure are blocked we have to open them--> go to azure vm-> network settings --> look inbound/outbound ports --> create port rule 

Now we have successfully deployed our jenkins app on vm 

Above way is static way of deploying or creating vm but for auto scalling way we another way vmss with help of load balancers 


