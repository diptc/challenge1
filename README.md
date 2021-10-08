# challenge1

I have deployed attached 3 tier achitecture.

Network Tier, Webtier-Apptier, DB Tier CFT are seperated.

I have not added WAF in Load Balancer and not enabled SSM for server which I could do.

Step 1: Run VPC Stack. Get Outputs.

Step 2: Run ELB-EC2 Stack. Take input from VPC Stack.

Step 3: Run MySQL-Stack. Take input from VPC Stack.

VPC Stack below resources will be deployed:

1 VPC
2 Web Subnet
2 App Subnet
2 DB Subnet
1 IGW
2 Nat Gateway in App Subnet
Corresponding Routes of Subnet

ELB-EC2 stack below resources will be deployed

1 Application load balancer (Listener, traget group)
2 2 EC2 in each AZ along with tomcat

MySQL stack below resources will be deployed

1 Multi AZ MySQL RDS
