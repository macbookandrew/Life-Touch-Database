#LifeTouch Database

##Description
This is a snapshot of an app build on the Drupal content management framework. For system requirements, installation troubleshooting, and other help, go to http://drupal.org  
The only custom code is found in:  
    `/sites/all/modules/lt_student`
    `/sites/all/themes/evangelism_manager`
    `/sites/all/themes/evangelism_manager_admin`  
All other code is from the http://drupal.org website.

##Requirements and Recommendations
This should run on most Linux servers (needs PHP and MySQL).  
If your church already has a website, I would recommend using a sub-domain for this app (i.e., lifetouch.firstbaptistmytown.org). You should be able to use the same server if you set up a new Apache virtual host.  
Note: This app will be slow if you do not have the [APC php module] (http://php.net/manual/en/book.apc.php) installed on your server.  

##Installation
1. Put the files into your web root folder
2. Create a MySQL database using the sql file snapshot from the root directory.
3. Edit `/sites/default/settings.php` line 92 with the credentials for your database.
4. You should now be able to access the site.
5. Log in as:
    `username: admin`  
    `password: password`  
This is the super user account. Use this account only for changing system configurations.

##Customization
Go to `/user/1/edit` to change your password and email.  
Go to `/admin/settings/site-information` and set the site email address.  
Go to `/admin/user/user/create` to create a new user.  
Give this user the Admin-edit role and log in as this user to do all the day-to-day administration of the database. (adding users, classes, students etc. via the Management link at the bottom of the page.)