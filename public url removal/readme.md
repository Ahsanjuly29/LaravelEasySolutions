How To remove '/public' from 'Url' #laravel(6 - upper version(old versions not sure! ))...
Go to 'public_html' folder. 'unzip' your 'Laravel' project here Or git pull.
Then, create an '.htaccess'file and write the below code:

RewriteEngine On
RewriteCond %{REQUEST_FILENAME} -d [OR]
RewriteCond %{REQUEST_FILENAME} -f
RewriteRule ^ ^$1 [N]
RewriteCond %{REQUEST_URI} (\.\w+$) [NC]
RewriteRule ^(.*)$ public/$1 
RewriteCond %{REQUEST_FILENAME} !-d
RewriteCond %{REQUEST_FILENAME} !-f
RewriteRule ^ server.php

problem Solved. Now your Project is running on your domain.extention
#HappyCoding