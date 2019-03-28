<img src="doc/landing.png">  

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