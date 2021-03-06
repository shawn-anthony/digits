<img src="doc/Landing.png">  

Digits is an application that allows users to:  
  
* Register an account.
* Create and manage a set of contacts.
* Add a set of timestamped notes regarding their interactions with each contact.

Installation  
First, [install Meteor](https://www.meteor.com/install).  

Second, [download a copy of Digits](https://github.com/shawn-anthony/digits). Note that Digits is a private repo and so you will need to request permission from the author to gain access to the repo.  

Third, cd into the app directory install the required libraries with:  

```
$ meteor npm install  
```
Once the libraries are installed, you can run the application by invoking:  

```
$ meteor npm run start
```

The first time you run the app, it will create some default users and data. Here is the output:

```
meteor npm run start

[[[[[ C:\Users\Shawn\Documents\GitHub\digits\app ]]]]]

=> Started proxy.
=> Started MongoDB.
I20190327-22:20:47.655(-10)? Creating the default user(s)
I20190327-22:20:47.655(-10)?   Creating user admin@foo.com.
I20190327-22:20:47.656(-10)?   Creating user john@foo.com.
I20190327-22:20:47.656(-10)? Creating default contacts.
I20190327-22:20:47.657(-10)?   Adding: Johnson (john@foo.com)
I20190327-22:20:47.657(-10)?   Adding: Casanova (john@foo.com)
I20190327-22:20:47.658(-10)?   Adding: Binsted (admin@foo.com)
=> Started your app.

=> App running at: http://localhost:3000/
   Type Control-C twice to stop.
```

Note regarding bcrypt warning. You will also get the following message when you run this application:

```
Note: you are using a pure-JavaScript implementation of bcrypt.
While this implementation will work correctly, it is known to be
approximately three times slower than the native implementation.
In order to use the native implementation instead, run

  meteor npm install --save bcrypt

in the root directory of your application.
```

On some operating systems (particularly Windows), installing bcrypt is much more difficult than implied by the above message. Bcrypt is only used in Meteor for password checking, 
so the performance implications are negligible until your site has very high traffic. You can safely ignore this warning without any problems during initial stages of development.

If all goes well, the template application will appear at [http://localhost:3000](http://localhost:3000). You can login using the credentials in [settings.development.json](https://github.com/ics-software-engineering/meteor-application-template-react/blob/master/config/settings.development.json), 
or else register a new account.

Lastly, you can run ESLint over the code in the imports/ directory with:  

```
meteor npm run lint
```

__User Interface Walkthrough__

__Landing Page__  
When you first bring up the application, you will see the landing page that provides a brief introduction to the capabilities of Digits:

<img src="doc/Landing.png">

__Register__    
If you do not yet have an account on the system, you can register by clicking on “Login”, then “Sign Up”:

<img src="doc/Register.png">

__Sign in__  
Click on the Login link, then click on the Signin link to bring up the Sign In page which allows you to login:

<img src="doc/Login.png">

__User home page__  
After successfully logging in, the system takes you to your home page. It is just like the landing page, but the NavBar contains links to list contact and add new contacts:

<img src="doc/Home.png">

__List Contacts__    
Clicking on the List Contacts link brings up a page that lists all of the contacts associated with the logged in user:

<img src="doc/Contacts.png">

__Edit Contacts__    
From the List Contacts page, the user can click the “Edit” link associated with any Contact to bring up a page that allows that Contact information to be edited:

<img src="doc/Edit.png">

__Admin mode__   
It is possible to designate one or more users as “Admins” through the settings file. When a user has the Admin role, they get access to a special NavBar link that retrieves a page listing all Contacts associated with all users:

<img src="doc/Admin.png">