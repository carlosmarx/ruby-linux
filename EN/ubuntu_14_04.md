# Ruby and Rails installation baby steps

this tutorial was made based on version 14.04 LTS Ubuntu, but it works in other distros based on Debian 

## 1º upgrade your apt-get

To do this,type in the terminal:

		sudo apt-get update

## 2º Configuring terminal.

Open your terminal, go to the menu 'Edit > Preferencies > title and command' and mark the option
'Execute command as shell session' , done, we can continue. 

## 3º Installing Curl(sometimes, i don't know why, it is not installed)

Just type:
		
		sudo apt-get install curl

## 4º Installing RVM (Ruby Version Manager)

With RVM you can install several different versions of ruby, and change according to your needs.
	
		curl -sSL http://get.rvm.io | bash

## 5º Installing a version of Ruby and setting default 

Enter commands:

		rvm install 2.2.0

then,to leave it as default:

		rvm use ruby-2.2.0 default

At the end of it, the command to be executed:

		ruby -v
		ruby 2.2.0p0 (2014-12-25 revision 49005) [x86_64-linux]

## 6º Installing Rails
		
		gem update --system	
		gem install rails

## 7º Make and run your first application

You can create your application with the following command:

		rails new app_name

Navigate to the project folder and run:

		bundle install

After than, start the server and access you browser to see your running application:

		rails s

The server by default runs on port 3000, then enter in your browser and enter the address below:
	
		localhost:3000

## Observations

This application is running with the sqlite3, wich comes as standard, if you do not specify otherwise, i recommend the installation of a more robust database to put your application in prodution, MySQL or PostgreSQL, for example.
You will also need a text editor or IDE, wich suits you best; 



### OPTIONAL

### Installing MySQL

		sudo apt-get install mysql-client libmysqld-dev

After than:
		
		gem install mysql2

### Installing PostgreSQL

		sudo apt-get install postgresql-9.3 libpq-dev

Then:
		
		gem install pg

## Installing Sublime-text

One of the most text editor used for web development, and in my opinion one of the best
		
		sudo add-apt-repository ppa:webupd8team/sublime-text-3 

Then:
	
		sudo apt-get update

And to finish:
		
		sudo apt-get install sublime-text-installer
