Steps (all in terminal brianlinux2) 

Initialised Git Repository 

mkdir MarketPeak_Ecommerce 

cd MarketPeak_Ecommerce 

git init 

 

Downloaded web template 2130_waso_strategy.zip 

Extracted into -  brianlinux2@brianlinux2:~/MarketPeak_Ecommerce 

unzip 2130_waso_strategy.zip -d ~/MarketPeak_Ecommerce 

 

Stage & Commit template to Git ( from MarketPeak_Ecommerce) 

git add . 

git config --global user.name BrianClabby 

git config --global user.email brianclabby1@gmail.com 

git commit -m "Initial commit with basic e-commerce site structure" 

 

Created github repo (on github.com  MarketPeak_Ecommerce, no readme, no gitignore nor license  

Within MarketPeak_Ecommerce folder –add repo url to local repo config 

git remote add origin https://github.com/BrianClabbGit75/MarketPeak_Ecommerce.git 

 

Push code –upload local repo to Github 

git push -u origin master 

Username for 'https://github.com': BrianClabbGit75 

Password  ******  (git pat classic pwd) 

Have connected to Linux AMI EC2 instance: 

 

sudo chmod 600 Linux1.pem 

ssh -i "Linux1.pem" ec2-user@ec2-13-60-197-129.eu-north-1.compute.amazonaws.com 


 

 

 

Instances I EC 
Horne - N... 
O Brianclabl 
a 
0- 
Imported 
Learning path 
devops-bootc Connect to yc 
github.com/3rianClabbGit75/Marketpeak Ecommerce 
pem 
- brianclü 
Q 
How to Fix "C' 
Type to search 
O. copy gnome 
All Bookmarks 
o 
BrianClabbGit75 / Marketpeak 
@ Issues Pull requests 
< > Code 
Ecommerce 
@ Actions 
Projects 
Public 
Wiki 
Q Goto file 
Security 
Clone 
HTTPS 
Insights 
MarketPeak Ecommerce 
Settings 
Pin 
Add file 
@ Unwatch 
< > Code 
star O 
E.' master 
1 Branch O Tags 
BrianClabbGit75 Initial commit with basic e-commerce site structure 
Local 
SSH 
Codespaces 
o 
2130_waso_strategy 
[I] README 
Initial commit with 
Add a READ 
GitHub CLI 
Help people interested in this repository understanC 
Add a READM 
https://github.com/BrianClabbGit75/Marketpeak_Ecommerce# 
You don't have any public SSH keys in your GitHub 
account. You can add a new or try 
cloning this repository via HTTPS. 
git@github.com : BrianC labbGit 75/Mar ketPeak_E 
use a password-protected SSH key. 
Download ZIP 
About 
No descrlptlon, website, or topics 
provided. 
-A,r Activity 
O stars 
@ 1 watching 
o forks 
Releases 
No releases published 
Create a new release 
Packages 
No packages published 
Publish your first package 
 

Cloning the Repo- see above – using SSH 

On EC2 instance – generate SSH Keypair using ssh-keygen 

 


 

..now to Display and copy Public Key: 

 


 

 

 

 

...added SSH public key  to Github: 

 

ssh-rsa AAAAB3NzaC1yc2EAAAADAQABAAABgQCqlKhmxienIiqWZ+ZwuCJh7LOaRCSfAO9ITLAmSY5Spmgzhi1qxH6FJ868LBhxmdk4ep2wurHYuTBVBNkinf779FJgr+zGvGEUz0IHYhXU93wZRnu5Snpbnn90tR/YuHICT20F1kaBf2pqYgueWRHq122od8eTjijxruG3Ni9MNzRSFG/211sckT6O5Sg0dNF90dss2Yl73s+GBVVfhhRhMxVg3n1EfsVq8laFwx+VpDypDPbQn9Wkw4GSX7YQoXIb8u5IMzj+pUCEj9MNFB4bovnV/7v8CiBJ8AivkdKnwiVF39R96e4leTGqpVQyd5oAkEQzlIeCwNiSq7e8L2UdqAHmWpFi/a87fGmNdocNLUg2nSwvQTR1pIzsaXuEOeg4WIyzCSSC0Slm7zAxKm3tiIJbdiLgqYNa7dNg+d5Dl9PeDprPwE/uVa4y1+nI3+h03rj3YcBCN7NvNsrh78s9JIIXidIGI0SKF5LOAXPBzMixZTTODcC2yx2qcJYthKU 

 

 


 

 

 

Will now use SSH clone, to clone the repo: 

 

git clone git@github.com:yourusername/MarketPeak_Ecommerce.git 

Ie: git@github.com:BrianClabbGit75/MarketPeak_Ecommerce.git 

 

[ec2-user@ip-172-31-41-118 ~]$ git clone git@github.com:BrianClabbGit75/MarketPeak_Ecommerce.git 

Cloning into 'MarketPeak_Ecommerce'... 

The authenticity of host 'github.com (4.225.11.194)' can't be established. 

ED25519 key fingerprint is SHA256:+DiY3wvvV6TuJJhbpZisF/zLDA0zPMSvHdkr4UvCOqU. 

This key is not known by any other names 

Are you sure you want to continue connecting (yes/no/[fingerprint])? yes 

Warning: Permanently added 'github.com' (ED25519) to the list of known hosts. 

remote: Enumerating objects: 39, done. 

remote: Counting objects: 100% (39/39), done. 

remote: Compressing objects: 100% (37/37), done. 

remote: Total 39 (delta 1), reused 39 (delta 1), pack-reused 0 (from 0) 

Receiving objects: 100% (39/39), 1.85 MiB | 3.08 MiB/s, done. 

Resolving deltas: 100% (1/1), done. 

[ec2-user@ip-172-31-41-118 ~]$  

 

 

 

 

Installing Apache web server on my EC2 

 

 

sudo yum update -y 

sudo yum install httpd -y 

sudo systemctl start httpd 

sudo systemctl enable httpd 

 

ec2-user@ip-172-31-41-118 ~]$ sudo systemctl start httpd  

[ec2-user@ip-172-31-41-118 ~]$ sudo systemctl enable httpd  

Created symlink /etc/systemd/system/multi-user.target.wants/httpd.service → /usr/lib/systemd/system/httpd.service. 

[ec2-user@ip-172-31-41-118 ~]$  

 

 

 


 

 

You can see that we have cleared the httpd web directory, and then copied MarketPeak_Ecommerce website files. 

 

The directory /var/www/html is a standard directory structure on linux servers that store web content, particularly Apache HTTP Server 

 


 

With httpd reloaded-the website now displays in my browser: 

 


 

Now with the website working for cicd purposes we create a new branch called Development, for Bugs and Fixes: 

 


 

Stage changes to git: 

 

 

 


 

 

Commit changes 

Brianlinux2@brianlinux2:~/MarketPeak_Ecommerce$ git commit -m "Add new features or fix bugs" 

On branch development 

nothing to commit, working tree clean 

 

Brianlinux2@brianlinux2:~/MarketPeak_Ecommerce/2130_waso_strategy$ git push origin development 

Username for 'https://github.com': BrianClabbGit75 

Password for 'https://BrianClabbGit75@github.com':  
