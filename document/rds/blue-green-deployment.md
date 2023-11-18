**Blue/green deployment** is a technique for releasing applications by shifting traffic between two identical environments running different versions of the application:
 * "Blue" is the currently running version 
 * "Green" is the new version. 
 
 This type of deployment allows you to test features in the green environment without impacting the currently running version of your application. 
 
 When you’re satisfied that the green version is working properly, you can gradually reroute the traffic from the old blue environment to the new green environment. 
 
 Blue/green deployments can mitigate common risks associated with deploying software, such as downtime and rollback capability.