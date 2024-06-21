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
|Directory|usage|
|:---:|:---:|
 bin: | files like startup.sh, startup.bat are available
 conf | server.xml, tomcat-users.xml
 lib |jar files
 logs | cataline.log, localhost.log, manager.log, hostmanager.log
 webapps | by default we have 5 applications
 work | after deployment of our application, 
 temp |

### installation prerequestics?
java and 1gb ram
### configuration of the apache tomcat in linux
|command|usage|
|:---:|:---:|
sudo su - | first Login as a root user, we can only install the softwares using the root user 
cd /opt | we create all the additional softwares in the *OPT* folder in linux
wget https://dlcdn.apache.org/tomcat/tomcat-9/v9.0.86/bin/apache-tomcat-9.0.86.zip | downloading the required version of the tomacat ZIP from the apache tomcat website to the linux server we use the *wget* command  
yum install wget unzip -y | to unzip the file we install the unzip to the linux server 
unzip apache-tomcat-9.0.86.zip | unzipping the downloaded apache tomcat zip file 
chmod u+x *.sh | give the executable permissions to all the .sh files in the bin/ directory as we have all the necessary files to start the tomcat server in the bin/ folder
ln -s /opt/apache-tomcat-9.0.86/bin/startup.sh /usr/bin/startTomcat ***and*** ln -s /opt/apache-tomcat-9.0.86/bin/shutdown.sh /usr/bin/stopTomcat | creating the soft links for the *startup and Stoptomcat* sh files to access it easily every time
login to the tomcat with manager app | comment the <value> tag in the /opt/apache-tomcat-9.0.90/webapps/manager/META-INF. why should we comment the value tag refer to the link: https://stackoverflow.com/a/36773669 
`<user username="admin" password="password" roles="manager-gui,admin-gui"/>` | add the username, password, roles in the /opt/apache-tomcat-9.0.90/conf file to login to the manger app and see our deployed applications
 
