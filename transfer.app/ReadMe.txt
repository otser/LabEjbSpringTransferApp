In order to build this application:

Go to com.softexploration.lab.ejbspring.transfer.build artifact location on a command line and execute: mvn clean install
Under location of com.softexploration.lab.ejbspring.transfer.app in the target folder will be created  a ready to deploy application: com.softexploration.lab.ejbspring.transfer.app-0.0.1-SNAPSHOT.ear
Deployment:

Deploy the com.softexploration.lab.ejbspring.transfer.app-0.0.1-SNAPSHOT.ear on a JEE 6+ compliant application server. The artifact does not declare external dependencies.

Accessing deployed application:

The MoneyTransferServlet takes two GET parameters:

amount � amount of money to transfer; expressed in java.lang.Double
facade � name of a fa�ade to perform a transfer
There are following fa�ade names:

ejb-spring � EJB fa�ade which refers to Spring Service
spring-singletonejb � Spring fa�ade which refers to Singleton Session Bean Service
spring-slejb � Spring fa�ade which refers to SLSB Service
spring-sfejb � Spring fa�ade which refers to SFSB Service
Generic URL:

http://<host>:<port>/webapp/MoneyTransferServlet?facade=<facade-name>&amount=<amount-value>

<host> � host on which application server is running
<port> � port of application server
<facade-name> � fa�ade name
<amount-value> � amount to transfer
------------------------------------------------------------------------------------------------------------------------------------------
Example URLs:
http://localhost:8080/webapp/MoneyTransferServlet?facade=ejb-spring&amount=100.5
------------------------------------------------------------------------------------------------------------------------------------------

------------------------------------------------------------------------------------------------------------------------------------------

------------------------------------------------------------------------------------------------------------------------------------------

------------------------------------------------------------------------------------------------------------------------------------------

