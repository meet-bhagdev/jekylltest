---
layout: page-steps
language: Java
title: Windows
permalink: /java/windows/
redirect_from:
  - /java/
  - /java/windows/step/
  - /java/windows/step/1
---

> In this section, you will get SQL Server 2017 running on Windows. After that you will install the necessary dependencies to create Java apps with SQL Server.

## Step 1.1 Install SQL Server
{% include partials/install_sql_server_windows.md %}

## Step 1.2 Install Java
If you already have Java installed on your machine, skip the next three steps. 

Install the **Java Runtime Environment (JRE)** by following the steps below. 
1. Click "Accept License Agreement" on the [**JRE download page**](http://www.oracle.com/technetwork/java/javase/downloads/jre8-downloads-2133155.html)

    ![downloads](https://sqlchoice.blob.core.windows.net/sqlchoice/static/images/jre_windows_license.JPG "downloads")

2. Download the appropriate JRE installer for Windows based on your operating system requirements (32 or 64-bit) 
3. Run the installer and follow the installation prompts to complete the JRE installation

Next, install the **Java Development Kit (JDK)** using the following command. 
1. Click "Accept License Agreement" on the [JDK download page](http://www.oracle.com/technetwork/java/javase/downloads/jdk8-downloads-2133151.html)

    ![downloadjdk](https://sqlchoice.blob.core.windows.net/sqlchoice/static/images/jdk_windows_license.JPG "downloadjdk")

2. Download the appropriate JDK installer for Windows based on your operating system requirements (32 or 64-bit) 
3. Run the installer and follow the installation prompts to complete the JDK installation

Add the JDK to your PATH environment variable 
1. Press start 
2. Search for "Advanced System Settings" 
3. Click on the "Environment Variables" button 
4. Add the location of the bin folder of the JDK installation to the PATH variable in **System Variables**. The following is a typical value for the PATH variable C:\WINDOWS\system32;C:\WINDOWS;C:\Program Files\Java\jdk1.8.0\bin

## 1.2 Install Maven

Maven can be used to help manage dependencies, build, test and run your Java project. Follow the instructions below to install Maven. 
1. Download the [Maven binary](http://www-eu.apache.org/dist/maven/maven-3/3.3.9/binaries/apache-maven-3.3.9-bin.zip)
2. Unzip the installer to a file location on your computer

Add the Maven bin directory to your PATH environment variable and add the JRE to the JAVA_HOME environment variable 
1. Press start 
2. Search for "Advanced System Settings" 
3. Click on the "Environment Variables" button 
4. Add the location of the bin folder of the Maven installation to the PATH variable 
5. Create a new System Variable for "JAVA_HOME" and point it to the location of the JRE in the JDK folder (ex. C:\Program Files\Java\jdk1.8.0_102\jre) 
6. Check that Maven was installed properly by running the following command.

```terminal
  mvn -v
```
```results
Apache Maven 3.3.9 (bb52d8502b132ec0a5a3f4c09453c07478323dc5; 2015-11-10T08:41:47-08:00)
Maven home: C:\apache-maven-3.3.9\bin\..
Java version: 1.8.0_102, vendor: Oracle Corporation
Java home: C:\Program Files\Java\jdk1.8.0_102\jre
Default locale: en_US, platform encoding: Cp1252
OS name: "windows 10", version: "10.0", arch: "amd64", family: "dos"
```
> You have successfully installed Java and Maven on Windows. You now have everything you need to start writing your Java apps with SQL Server!
