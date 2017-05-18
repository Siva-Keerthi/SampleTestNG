Step to Run:

Download the Repo.

Navigate to the folder with pom.xml

Open the command prompt

Run with below Maven command to run the script 

mvn surefire:test -Dtest=TestParallel,TestParallel2 -DmyBrowser=chrome - To run parallel in class level. [ Note: We can use wild card as well like TestParallel*, it will execute all the methods in the class.

If we want to run method in parallel,
Class name # method name 1 + method name 2
mvn test -Dtest=TestParallel#test_01+test_02 -DmyBrowser=chrome

If we want to run specific method in the class
mvn test -Dtest=TestParallel#test_01+test_02,TestParallel2#test_01 -DmyBrowser=chrome
