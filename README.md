Awesome rails new
===================

Do you work with RVM and use one gemset for each project? Then, you know the hard work involved in creating a project:

```
# create and use the new RVM gemset
rvm use --create 2.1.2@project_name

# install rails into the blank gemset
gem install --no-rdoc --no-ri rails

# generate the new rails project
rails new project_name

# go into the new project directory and create an .rvmrc for the gemset
echo 2.1.2 > .ruby-version
echo project_name > .ruby-gemset

# verify the rvmrc
cd ..; cd -

# create database
mysql -u root -e "create database `database_name` CHARACTER SET utf8 COLLATE utf8_general_ci"
```

I've created a shell script for doing all this work for us!


----------


Shell Script installation
-------------
Add this shell script in a local path like /my-bash-process

Add this path to PATH variable.
```
sudo nano /etc/paths
```

That's it! To test it, open new terminal and type:
```
echo $PATH
```

----------

Shell Script usage
-------------
```
railsnew mywebsite.com 2.1.2 mywebsite_com_development
```

----------
> **Note:**

> - Only works for **Ruby on Rails** projects using **RVM**.
> - Project is created using mysql for DB.
