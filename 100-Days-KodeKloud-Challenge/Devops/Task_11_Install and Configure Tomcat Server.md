[Medium-Link](https://medium.com/@janemils/kodekloud-engineer-day-11-install-and-configure-tomcat-server-f2170aedcd45)

Commands I executed to get the result are : 
1) Install Tomcat :
   sudo dnf install -y tomcat
3) Change the port to given port in the task
   cd /etc/tomcat/server.xml
   <img width="588" height="122" alt="image" src="https://github.com/user-attachments/assets/5548f269-c69f-45eb-8337-814006fbcd31" />
4) Copy the ROOT.war from Jumphost to App-server using cmd :
  scp /tmp/ROOT.war steve@stapp02:/var/lib/tomcat/webapps/
  ROOT will be automatically extracted and deployed in Tomcat server. A directory /ROOT will be created which contains the content.
6)  Check the URL to check if the app is deployed.
   curl http://stapp02:6200
