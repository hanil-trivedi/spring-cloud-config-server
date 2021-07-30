# spring-cloud-config-server
The MS which connects with the local git repo(git-localconfig-repo) having all MS config files and connects with other MS and provides them the config files

Its a centalized config server ...
starters added -
1. Config Server 
2. SB Dev tools

in app.properties file,

#give the application a good name as below
spring.application.name=spring-cloud-config-server

#configure the local folder(git initiated) where the prop files are present
spring.cloud.config.server.git.uri=file:///C:/Learning/Full-courses/in28minutes/courses/Master_Microservices_with_Spring_Boot_and_Spring_Cloud/workspaces/spring-microservices-v2-writtenByHanil/git-localconfig-repo

-> now we can use this microservice to pick the properties/configs from local git folder/repo(git-localconfig-repo) and then the MSs where this application (spring-cloud-config-server) is configiured as a config-server will be able to use those properties .

now once the this application is up and running on port 8888 ,local host , we can hit below URL to get the default properties file present in out local git folder/repo(git-localconfig-repo)

http://localhost:8888/limits-service/default
