start the configuration server: 

./configserver.sh

start the demo client with spring-profile=test4: 

./demo.sh

check which value for message is served by /config-repo/application.yml or /config-repo/demo.yml

http://localhost:8080/message

expected: test4 (from application.yml), served: test2 (from demo.yml)
