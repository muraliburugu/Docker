

#### docker version check
```
docker --version
```


### step-1 ; got to docker website to download

https://docs.docker.com/desktop/setup/install/windows-install/

### step 2:

![Screenshot (9)](https://github.com/user-attachments/assets/efec5328-d4a4-41ef-b0e0-f456d894eb82)



#### step 3 :

![Screenshot (10)](https://github.com/user-attachments/assets/5b0cc127-edf3-4a96-af3a-1cd82533fd68)




#### step 4 :
![Screenshot (11)](https://github.com/user-attachments/assets/64af2297-b950-4954-9512-2cf1f336bd5b)






### step 5:

```
wsl --set-default-version 2

```


### step 6 (if we have any problem)
-----------------------------

https://learn.microsoft.com/en-us/windows/wsl/install-manual#step-4---download-the-linux-kernel-update-package




















### for ubuntu installation


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






