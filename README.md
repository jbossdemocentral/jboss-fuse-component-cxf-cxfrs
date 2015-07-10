CXF & CXFRS Claim DEMO
======================================================
This demoCreate web services that takes in customer's insurance claim application, also provide another cancel function in case they have changed their mind. 
Using Camel CXF and CXFRS component to build the web service. And deploy the bundle onto JBoss Fuse Fabric. 
In this demo, it uses 2 SOAP web service and 2 Restful Web Service, and the restCancel operation is actually reusing the cancel SOAP web service by using the CXF producer component.


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

Under Runtime, you will see list of containers, and click on the small icon on the righthand-side of the cxfrscon container
![Fabric list](https://raw.githubusercontent.com/weimeilin79/claim-cxf-cxfrs/master/doc/pic/01-fabric-container-list.png?raw=true)
You can also checkout the registry
![Fabric list](https://raw.githubusercontent.com/jbossdemocentral/claim-cxf-cxfrs/master/doc/pic/02-registry.png?raw=true)

In the APIs view you will also find all the avaliable web services regiestered in the fabric
![Fabric list](https://raw.githubusercontent.com/jbossdemocentral/claim-cxf-cxfrs/master/doc/pic/05-webservices.png?raw=true)

And either use browser to run it 
![Fabric list](https://raw.githubusercontent.com/jbossdemocentral/claim-cxf-cxfrs/master/doc/pic/03-browser.png?raw=true)

Or you can use SOAP UI to play with the SOAP Web Services.
![Fabric list](https://raw.githubusercontent.com/jbossdemocentral/claim-cxf-cxfrs/master/doc/pic/04-soapui.png?raw=true)


The demo video are located here too:
(The videos are base on version Fuse 6.1)

https://vimeo.com/115418661
https://vimeo.com/115560431
