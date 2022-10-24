# Load Balancer
In this project, additional two servers are provided in order to configure Nginx on of the servers and set up HAproxy load balancer on the other.

# Tasks
* on the first task, we will write a bash script that configures Nginx with HTTP response header on the second server. The name of the HTTP header is X-Served-By and its value is the hostname of the server.
* Next, we will write a bash script that installs and configures HAproxy version 1.5 on the third server. Requests will be distributed using round robin algorithm.
