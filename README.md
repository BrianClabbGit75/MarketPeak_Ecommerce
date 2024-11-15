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
