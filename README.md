# Springboot Command Run

1. Basic command
* gradlew
* gradlew test      //test
* gradlew bootRun   //run for environment
* gradlew bootJar   //run for deploy 

2. Fix errors
* gradlew clean
* set java_home=<location java>jdk folder>
* gradlew test 
* wait ...
or
* build.gradle
* edit line 9 sourceCompatibility ='8'

3. Set java path
* echo %java_home%
* set path=.;%java_home%\bin;%path%