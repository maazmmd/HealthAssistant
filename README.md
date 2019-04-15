### Prerequisites
- Node JS Version 6  
- MongoDB
- Node Packages - Bower (Install Globally)

##### Installation (In Mac OSx)
- Nodejs Installation
McFarland, D. 2014. How to Install Node.js and NPM on a Mac. Available [Link](https://medium.com/@katopz/how-to-install-specific-nodejs-version-c6e1cec8aa11) 
```
$$ brew install node@6
$$ brew link node@6
$$ node -v
```
- MongoDB Installation [Link](https://treehouse.github.io/installation-guides/mac/mongo-mac.html)
```
$$ brew update
$$ brew install mongo
```

#### Important
Below are the versions of Nodejs, make sure to as mentioned below as after node 6 , its will give you compilation error as above node 6 javascript is ES6
```
$$ node -v
v6.17.0
$$ npm -v
3.10.10
$$ npm install -g bower // Install bower globally

```
### Clone the Repo and follow other commands 
```
$$ git clone https://github.com/maazmmd/HealthAssistant.git
$$ cd HealthAssist
$$ bower install 
$$ npm install
```
### In db.js (Inside models folder) Change your DB URI or database name cretaed.  
Eg. var dbURI = 'mongodb://localhost/test';
```
$$ show dbs;
$$ use test; // Create and use Database (Eg. here is test) via MongoShell and configure the same in db.js   
```

### Make sure MongoDB Server is already running before running the application 
```
$$ sudo mongod  // Running Mongo on Mac OSX
$$ sudo mongo
```

### Then finally run the aplication
```
$$ node server.js
```
OR
```
$$ npm start
```
#### Application will be running on port 8080
Open the browser
Type the URL http://localhost:8080/


## Email Configuration
Connect to Internet (Good if no firewall settings are enabled)  

1. XML File Path should be changed in emailClient.js  
2. All the paths and deatils like SMTP and others inside Email Confuration xml file should be changed (email/emailSMSConfig.xml).  
   a. SMTP Server address, port, username, address  
   b. Sending email via gmail (Configure your Gmail account to send emails by turning On low level apps from other application) [Link](https://www.hostinger.com/tutorials/how-to-use-free-google-smtp-server ) 
   - gmail -> Settings -> Forwarding POP/IMAP -> Select enable IMAP 
   - Goto Google Account (Privacy) Security in the below u will find allow less secure apps (Select YES/ON)   
   gmail -> google account -> security (scrool down) -> Turn on low level access for apps
   
   Make sure you follow above steps (Most important else your email will not be sent via gmail SMTP)  
   
Common Inputs for gmail  
```
<smtpServer>smtp.gmail.com</smtpServer>  
<port>465</port>  
<authentication>true</authentication>
```

- Email Template created Online using Email template Engine, free online Professional Email Templates [Link](https://beefree.io/)  

#### References
MongoDB, Inc. 2008. Documents. Available: [Link](https://docs.mongodb.com/manual/core/document)  
Sending an email in Node JS – [Link](https://nodemailer.com/about/)  
Auth0, Inc. 2015. What is JSON Web Token? Available: [Link](https://jwt.io/introduction)  


