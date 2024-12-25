# PersonalizedARCatalog

![image](https://github.com/user-attachments/assets/a1064176-f9e6-4dee-acd8-c82c13b28a9b)



you can access with this url. (Please do not try find bugs :) I know that you can find)
http://45.143.99.170/

if you are going to use a web server, I show below how I use it in my own nginx, you can change it accordingly

***
    server {
    listen 80;
    server_name your-domain.com; # Alan adını veya IP adresini yaz

    location / {
        proxy_pass http://127.0.0.1:3000; 
        proxy_http_version 1.1;
        proxy_set_header Upgrade $http_upgrade;
        proxy_set_header Connection 'upgrade';
        proxy_set_header Host $host;
        proxy_cache_bypass $http_upgrade;
    }

    location /api/catalogs {
        proxy_pass http://127.0.0.1:5000; 
        proxy_http_version 1.1;
        proxy_set_header Upgrade $http_upgrade;
        proxy_set_header Connection 'upgrade';
        proxy_set_header Host $host;
        proxy_cache_bypass $http_upgrade;
        }
    }


This project consists of three main parts:

1. **Frontend** → User interface ([Frontend Deposu](https://github.com/Berkayft/MoreThanYouSeeF))
2. **Backend** → API and Business Logic ([Backend Deposu](https://github.com/Berkayft/MoreThanYouSeeB))
3. **Machine Learning** → Artificial intelligence module ([Machine Learning Deposu](https://github.com/Berkayft/flaskImageRetrivial))


## Setup
Each sub-module has its own instructions on how to install it.
