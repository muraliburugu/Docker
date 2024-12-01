

#### docker version check
```
docker --version
```
![Screenshot (10)](https://github.com/user-attachments/assets/437b58ba-780b-49f6-a3dc-5541301abbb7)

![Screenshot (9)](https://github.com/user-attachments/assets/efec5328-d4a4-41ef-b0e0-f456d894eb82)


![Uploading Screenshot (11).png…]()







###### for ubuntu installation


 ### docker installation commandas

 ```
# Add Docker's official GPG key:
sudo apt-get update
sudo apt-get install ca-certificates curl
sudo install -m 0755 -d /etc/apt/keyrings
sudo curl -fsSL https://download.docker.com/linux/ubuntu/gpg -o /etc/apt/keyrings/docker.asc
sudo chmod a+r /etc/apt/keyrings/docker.asc

# Add the repository to Apt sources:
echo \
  "deb [arch=$(dpkg --print-architecture) signed-by=/etc/apt/keyrings/docker.asc] https://download.docker.com/linux/ubuntu \
  $(. /etc/os-release && echo "$VERSION_CODENAME") stable" | \
  sudo tee /etc/apt/sources.list.d/docker.list > /dev/null
sudo apt-get update

```

To install the latest version, run:

```
sudo apt-get install docker-ce docker-ce-cli containerd.io docker-buildx-plugin docker-compose-plugin

```






