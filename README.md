# apacheTomcat

## for testing and running the war and ear file, what do we use?
we use the appllication servers like
|server|versions|
|:---:|:---:|
JBoss | 1.x to 7.x, it is a free version
wildfly | From redhat, Jboss is named as wildfly from the 8.x version, it is a free version  
tomcat | Apache, it is a free version 
websphere application server (WAS) | from IBM, it is a paid version
weblogic | From Bea weblogic but accuired by the Oracle, it is a paid version

## In Tomcat we can only deploy WAR files(these are web application server), but in the JBoss/Wildfly/websphere/weblogic we can deploy the WAR and EAR files also(these are enterprise application servers)

## when to use the Binary and source code distributions while downloading the apache software
Binary --> This archieve file for deployment purpose, it a already compliled and runnable software
source code --> contains all the java classes, if we want to develop somemore features we can use this and after that compile and run  

## directories in the Tomcat structure
1. bin: files like startup.sh, startup.bat are available
2. conf: server.xml, tomcat-users.xml
3. lib: jar files
4. logs: cataline.log, localhost.log, manager.log, hostmanager.log
5. webapps: by default we have 5 applications
6. work: after deployment of our application, 
7. temp:

### installation prerequestics?
java and 1gb ram
