Web Infrastructure Design with a LAMP stack.  where we are required to use a web server, application server, codebase and database where 
the https requested will be searched and a https response given back to user for www.foobar.com. why HTTPS? we use HTTPS to keep track of the traffic between client and the server
we used firewalls, load balancer to distribute traffic between the servers and a monitoring tool of your choice to monitor the designed infrastructure for instance triggering an alert
if something unusual happens. And to make it secure we addeda SSL certificate. where encryption is required to avoid granting unauthorized access.
reason for clustering the load balancer in task 3 is so that incase of a SPOF the other can take over.
Having servers with all the same components (database, web server and application server) might be a problem because when there is maintenance performed on a server for a specific component, it will affect other components that are on it
Terminating SSL at the load balancer level is an issue because the traffic between the load balancer and the web servers is unencrypted
Having only one MySQL server capable of accepting writes is an issue because if the master goes down, the application cannot write to the database anymore
