<h2 color="red">How To remove '/public' from 'Url'</h2>
<h5 style="color:yellow;">#laravel(6 - upper version(old versions not sure! ))...</h5>

<ul>
   	<li>Go to 'public_html' folder.</li>
	<li>'unzip' your 'Laravel' project here Or use command:git pull.</li>
	<li>Then, create an '.htaccess'file and write the below code:</li>
</ul>
```
 RewriteEngine On </br>
 RewriteCond %{REQUEST_FILENAME} -d [OR] </br>
 RewriteCond %{REQUEST_FILENAME} -f </br>
 RewriteRule ^ ^$1 [N] </br>
 RewriteCond %{REQUEST_URI} (\.\w+$) [NC] </br>
 RewriteRule ^(.*)$ public/$1  </br>
 RewriteCond %{REQUEST_FILENAME} !-d </br>
 RewriteCond %{REQUEST_FILENAME} !-f </br>
 RewriteRule ^ server.php </br>
```

<p><strong><span style="color:green;">Yeah!</span> Problem Solved. Now your Project is running on your domain.extention</strong></p>
<h2> #HappyCoding </h2>
<img src="Screenshot_2.png">
