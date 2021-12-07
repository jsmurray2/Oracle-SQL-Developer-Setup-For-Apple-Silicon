# Oracle-SQL-Developer-Setup-For-Apple-Silicon
This short tutorial is designed to to get Oracle SQL Developer up and running on devices using Apple Silicon processors such as the Apple M1.

## Java
Oracle now officially supplies an version of **Java JDK 17** for Apple Silicon [here](https://www.oracle.com/java/technologies/downloads/#jdk17-mac). Download and install the **Arm 64 DMG Installer**.

## SQL Developer
Download the latest version of SQL Developer [here](https://www.oracle.com/tools/downloads/sqldev-downloads.html) (version 21.2.1 as of writing). Download the MacOSX version, extract the .zip file and copy SQLDeveloper.app to your Applications folder. In finder, right click on SQLDeveloper.app and choose "Show Package Contents". Then, move to "/Contents/MacOS/" and open sqldeveloper.sh with your text editor of choice. On line 21, change 11 to 17 such that the line reads as:
```
APP_JAVA_HOME=`/usr/libexec/java_home -F -v 17`
```
Save and close sqldeveloper.sh and you may now launch SQLDeveloper.app. It may throw some warnings, but the application works as expected.