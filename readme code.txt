composer global require laravel/installer

#git

https://github.com/Phanurat/myproject.git

git remote add origin https://github.com/Phanurat/myproject.git

#Up file ไปบน git ต้องเอา

#Check Where URL
git remote -v
#Show
origin  https://github.com/Phanurat/myproject.git (fetch)
origin  https://github.com/Phanurat/myproject.git (push)

#Change branch master to main
git branch -m master main

#Upload to git
git push origin main 

#if error
git push -f origin main

#first cmd clone or deploy
git clone https://github.com/Phanurat/myproject.git myproject1 #Name myproject1

#other or update code
git pull 

#before clone git >> Laravel
composer install # Run in /myproject1

#problem from laravel
sudo php artisan config:cache
sudo php artisan optimize

sudo php artisan route:cache
sudo php artisan migrate #migrate last 3 #run 4 to clear config cache route

#every thing for user forever to in file gitignore not about database

======================================================================
<VirtualHost *:8000>
ServerName 192.168.18.134
ServerAdmin admin@localhost.com
DocumentRoot /var/www/html/myproject1/public
<Directory /var/www/html/myproject1>
AllowOverride All
</Directory>
ErrorLog ${APACHE_LOG_DIR}/error.log
CustomLog ${APACHE_LOG_DIR}/access.log combined
</VirtualHost>
========================================================================

========================================================================
sudo chown -R www-data:www-data /var/www/html/myproject1
sudo chmod -R 775 /var/www/html/myproject1/storage
========================================================================

========================================================================
#edit by
chmod -R ugo+rwx storage
#or
sudo chmod -R ugo+rwx /path/to/folder
========================================================================

========================================================================
#create database
GRANT ALL PRIVILEGES ON *.* TO 'db_myproject1'@'localhost' IDENTIFIED BY 'P@s$w0rd123!';

========================================================================

========================================================================

#laravel
.haccess #edit

========================================================================