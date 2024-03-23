# The-From_Mind_Posts-Medium
Medium : : Scripts of My Project in posting my idea and support.

<a href="https://medium.com/@sams0ngultek/step-by-step-guide-on-how-to-set-up-the-environment-for-java-web-application-on-intellij-idea-ide-6f2cc588b12e"
  id = "PostFirst"> 
     Post-First-Medium
</a>


<div>
  Hey medium👋, I am very thrilled for this post. The motivation behind this blog-post is that I was very obsessed with the clean 😎UI and UX of Intellij-Idea IDE of jetbrain that makes me stick with it in every moment of developing any java application. My project was a java web application that can be implemented for cargo shipping company that enables the client of the company to track their properties😜. Apparently, my project need to be submitted with in 24-hrs 🤷‍♂️but my development environment was not set-up. At that moment of urgency the deal is about finishing the project not about choosing IDE to IDE with regard to the beauty and the coolness of the UI. Matter-fact, I choose favorite and promising IDE (Intellij Idea of jet-brain) for java application development. So then the struggle begins here, Which is that, In jet-brain software product policy there are different Editions on a certain software product like Intellij Idea IDE Community Edition(Free) and Intellij Idea IDE Ultimate Edition(Payed) based-on your development option.

```
source: https://blog.jetbrains.com/idea/2021/01/creating-a-new-project-in-intellij-idea/
For more Information you can check this: https://blog.jetbrains.com/
```
Step One:

At that moment I was using the Community Edition that I won’t be able to develop my java application on so I have to download the Ultimate Edition and I downloaded it:
```
Download IntelliJ IDEA - The Leading Java and Kotlin IDE
Download the latest version of IntelliJ IDEA for Windows, macOS or Linux.
www.jetbrains.com
```
Step Two:

Make sure that you just download and set-up the required Software(s) for your java web application:

Downloading the JDK:
```
Download the Latest Java LTS Free
Download the Java including the latest version 17 LTS on the Java SE Platform. These downloads can be used for any…
www.oracle.com
```
then setting-up the path in the system environment variable on your local machine:

How to set the environment variables for Java in Windows
```
How to set the environment variables for Java in Windows (the classpath)?
stackoverflow.com
```
You have to check whether the installation and the path is correctly set-up using the following command:
```shell
C:\>javac --version
javac 14.0.1
C:\>
```
If the version of your java, in my case the java version is 14.0.1, is not appeared after typing the javac version command may be it is incorrect on the set-up of environment variable, try by making the path and the naming directly as it is in the tutorial above.

After Installing the JDK and setting-up the path that powerful jet-brain’s IDE automatically detects the Java Development Kit(JDK).

Downloading Apache Tomcat, I recommend downloading the latest version:
```
welcome to Apache tomcat downaload
```

Step Three:

Let us download our database management system software, In my project I use MySQL:
```
MySQL :: MySQL Downloads
MySQL and HeatWave Summit is where developers, DBAs, experts, and users come to learn about the latest innovations…
www.mysql.com
```
Download the community version which say ```“MySQL Community (GPL) Downloads »”``` you can find it in the last option.

Step Four:

Downloading a java ```.jar file``` for establishing the connectivity between the database and Java program. Since we are using MySQL we are going to download the MySQL java connector that we can find in:
```
MySQL :: Download Connector/J
MySQL Connector/J is the official JDBC driver for MySQL. MySQL Connector/J 8.0 and higher is compatible with all MySQL…
dev.mysql.com
```
Now let us open IntelliJ Idea IDE and create our first java web application.

Creating a new Java Enterprise project
IntelliJ IDEA includes a dedicated wizard for creating Java Enterprise projects based on various Java EE and Jakarta EE implementations. In this tutorial, we will create a simple web application.

In the main menu, go to ```File | New | Project.```
In the New Project dialog, select Jakarta EE.
Enter a name for your project: ```JavaEEHelloWorld.``` You can enter any name you want
Select the Web application template, Maven as a build tool, and use Oracle OpenJDK 17 as the project SDK. Don’t select or add an application server, we will do it later.
Click Next to continue.

In the Version field, select ```Jakarta EE 10 ```because that’s what Tomcat 10.1 used in this tutorial is compatible with.

For ```Tomcat 9```, select ```Java EE 8.``` For ```Tomcat 10```, select ```Jakarta EE 9.1```.

In the Dependencies list, you can see that the web application template includes only the Servlet framework under Specifications.


Finally, Click Create.

In the IntelliJ Idea ``` Setting Build, Execution, Deployment | Application Servers``` panel we can check that our configuration is full set, our IDE will automatically detects and set everything for us.

You can check for more on:
```
Enable Web application support | IntelliJ IDEA
When you enable Web Application support in IntelliJ IDEA, it can do the following: Create a web resource directory web…
www.jetbrains.com
```
The final part on our set-up is, In in project folder which we named it as ```JavaEEHelloWorld.```

we can find a folder named ```WEB-INF``` in that folder we will copy and paste the MySQL java connector.

The java code for the database connectivity establishment is as follows:
```java
import java.io.*;
import java.sql.*;

class samsonTesting {
 public static void main(String[] args) throws Exception
 {
  String url = "jdbc:mysql://localhost:3306/table_name"; // connection url details
  String username = "Yourusername"; // MySQL credentials
  String password = "Yourpassword";
 
  Class.forName(
   "com.mysql.cj.jdbc.Driver"); // here it is the Driver name of MySQL
  Connection con = DriverManager.getConnection(
   url, username, password);
  System.out.println(
   "Connection Established successfully");
// It is a good practice to close a connection after we are done with our database program
  con.close(); // close connection
  System.out.println("Connection Closed....");
 }
}
```
Vola, we are done!!!

For the story to be end, I just remain with my obsession and set-up my java web application project using IntelliJ IDEA, it was fantastic at the end.

Thankyou for reading, I hope you learn a lot from this post. See you later.

    Topics:
        Java Web Application
        Intellij Idea
        Tomcat
        MySQL
        Jdbc
</div>
