File & JDBC Bank DEMO
======================================================
This demo demonstrates the use of File and JDBC connector in Camel, also added the use if Spilt pattern and Exception handling method. 
The scenario of the demo is to mimic the transaction process between bank accounts, where it takes in XML file from different branch in a directory, each contains cash deposit, cash withdraw and transfer information of bank accounts, depending on the type of transaction, spilt up each transaction retrieve balance from a database, does the transaction and calculate the transaction fee and then place the balance back to the database storage. 



Setup and configuration
-----------------------

Download JBoss Fuse from jboss.org, and place the downloaded zip file under installs folder.

Add fabric server passwords for Maven Plugin to your ~/.m2/settings.xml file the fabric server's user and password so that the maven plugin can login to the fabric.

```
<server>
  <id>fabric8.upload.repo</id>
  <username>admin</username>
  <password>admin</password>
</server>
```

run 
```
init.sh
```

It will setup JBoss Fuse, install fabric, build and deploy the profile. 

To run the demo, in browser enter http://localhost:8181 and login with ID/PWD of admin/admin

Under Runtime, you will see list of containers, and click on the small icon on the righthand-side of the testcon container
![Fabric list](https://raw.githubusercontent.com/weimeilin79/filenjdbc/master/doc/pic/01-fabric-container-list.png?raw=true)
Inside the Container, under Camel tab, you will see the list of routes we have.
![Container Route List](https://raw.githubusercontent.com/weimeilin79/filenjdbc/master/doc/pic/02-container-route-list.png?raw=true)
Click on Endpoint on the lefthand-side, choose the file endpoint, and send the xml.
![Containter Endpoint Send](https://raw.githubusercontent.com/weimeilin79/filenjdbc/master/doc/pic/03-container-send.png?raw=true)
You will see the transfer result in the log. 
![Container Log](https://raw.githubusercontent.com/weimeilin79/filenjdbc/master/doc/pic/04-container-log.png?raw=true)
 


The demo video are located here too:

1.	https://vimeo.com/113289566
2.	https://vimeo.com/114960456 
