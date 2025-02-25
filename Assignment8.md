# Assignment 8 - Firewall

## Install UFW:

        sudo apt update

        sudo apt install ufw -y

![Install](img/1.png)


## Define Firewall Rules:

- Reset UFW to deafult

        sudo ufw --force reset

- Default policies that blocks everything except allowed 

        sudo ufw default deny incoming

        sudo ufw default allow outgoing

![](img/2.png)

- Allow SSH, It's port is 22

        sudo ufw allow 22/tcp

- Allow HTTP, It's port is 80

        sudo ufw allow 80/tcp

- Allow HTTPS, It's port is 443

        sudo ufw allow 443/tcp

![ports](img/3.png)

- Prevent SYN Flood attacks

        sudo ufw limit proto tcp from any to any port 22

        sudo ufw limit proto tcp from any to any port 80

        sudo ufw limit proto tcp from any to any port 443

![SYN](img/4.png)

- Enable logging

        sudo ufw logging on

![loging](img/5.png)

- Verify the Configuration

        sudo ufw status verbose

![verify](img/6.png)