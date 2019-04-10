### Prerequisites
Node JS V6  
MongoDB
Node Packages - Bower (Install Globally)

##### Installation - Nodejs
McFarland, D. 2014. How to Install Node.js and NPM on a Mac. Available: http://blog.teamtree-house.com/install-node-js-npm-mac. 

```
$$ node -v
v6.17.0
$$ npm -v
3.10.10
$$ npm install -g bower // Install bower globally

```
### Clone the Repo and follow other commands 
```
$$ git clone url
$$ bower install 
$$ npm install
```
### In server.js (Inside models folder) Change your DB URI Eg. var dbURI = 'mongodb://localhost/test';
```
$$ show dbs;
$$ use test; // Create and use test Database via MongoShell

$$ sudo mongod  // Running Mongo on Mac OSX
$$ sudo mongo   
```

### Make sure MongoDB Server is already running before running the application 
### Then run 
```
$$ node server.js
```
OR
```
$$ npm start
```
#### Application will be running on port 8080

## Email Configuration
Connect to Internet (Good if no firewall settings are enabled)  

1. XML File Path (Email Configurations) should be changed in emailClient.js  
2. All the paths and other necessary fields inside Email Confuration should be changed.  
   a. SMTP Server address, port, username, address  
   b. If sending via gmail (Configure your Gmail account to send emails) Link below  
   https://www.hostinger.com/tutorials/how-to-use-free-google-smtp-server  
   
   Make sure you follow above steps along with below steps (Most impoerant else your email will not be sent)  
   a. Goto Google Account (Privacy) Security in the below u will find allow less secure apps (Select YES/ON)  
   
Common Inputs for gmail  
```
<smtpServer>smtp.gmail.com</smtpServer>  
<port>465</port>  
<authentication>true</authentication>
```

#### References
MongoDB, Inc. 2008. Documents. Available: https://docs.mongodb.com/manual/core/document.   
Sending an email in Node JS – https://nodemailer.com/about/  
Auth0, Inc. 2015. What is JSON Web Token? Available: https://jwt.io/introduction.   

##### Contact 
Mohammed Maaz, Student ID : 0877744  
e: mmoham10@lakeheadu.ca


