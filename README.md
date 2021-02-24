start the configuration server: 

./configserver.sh

start the demo client with spring-profile=test4: 

./demo.sh

check which value for message is served by /config-repo/application.yml or /config-repo/demo.yml

http://localhost:8080/message

expected: test4 (from application.yml), served: test2 (from demo.yml)

-------------

Stop or don't start the configserver and run this Test:
mvn -pl demo -Dtest=DemoApplicationTests test

--> wrong result. Profiles are not taken into account
src/main/resources/application.yml
--> if you change optional:configserver:http://localhost:8888/ to configserver:http://localhost:8888/
the Tests fails because the config server is not available

The Property "spring.cloud.config.enabled=false" has no effect in the TestClass.
