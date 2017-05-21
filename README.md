## Description

This is a sample TestNG based Selenium framework. This is developed just for the purpose of AOF demo.

## Pre-Requisite:

- JRE/JDK
- Selenium Server Standalone JAR
- Selenium Chrome Driver
- **Windows OS** (Tested in Windows 10 only. Not tested in any other Windows Version or Linux)
- **Chrome Browser** (Works only for Chrome browser)

## Location of Test Cases

- The Test Cases are in the following folder/package : `/src/test/java/AOF`
- Each test case file extends `BaseTest.java`

## Steps to Run:

- Clone/Download the Repo.

- Update the path for Selenium Server Standalone JAR & Chrome Driver in `Node.bat` and `Hub.bat`

- Start `Node.bat` & `Hub.bat` and verify that there are no errors in their console

- It is a maven project and test cases are run using `mvn surefire:test` command in the root path i.e where `pom.xml` is present

## mvn Command Options:

**Core command** : `mvn surefire:test`

**Test Case selection** : `-Dtest=\<list of test classes/methods\>`

**Browser Selection** : `-DmyBrowser=\<browser\>`

*To run parallel in class level. [ Note: We can use wild card as well like TestParallel\*, it will execute all the methods in the class.]*

`mvn surefire:test -Dtest=TestParallel,TestParallel2 -DmyBrowser=chrome`

*To run specific method in a specific class*

`mvn test -Dtest=TestParallel#test_01+test_02,TestParallel2#test_01 -DmyBrowser=chrome`

*If we want to run method in parallel [Class name # method name 1 + method name 2]*

`mvn test -Dtest=TestParallel#test_01+test_02 -DmyBrowser=chrome`

