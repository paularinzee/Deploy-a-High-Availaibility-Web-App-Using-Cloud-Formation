
# Deploy-a-High-Availaibility-Web-Service-Using-Cloud-Formation

## Prerequisites
A user account with programmatic access to AWS

## To run

#LucidCharts Infrastructure Diagram:

https://lucid.app/lucidchart/b25db5b8-2e16-4f03-a878-31926f1bf51f/edit?invitationId=inv_9ad62842-547e-4beb-aeb7-43101edc6940&page=0_0#
<img width="1438" alt="Screenshot 2022-06-17 at 14 52 03" src="https://github.com/paularinzee/Deploy-a-High-Availaibility-Web-App-Using-Cloud-Formation/blob/master/screenshots/Infrastructure%20Diagram.jpeg">

# Create network stack using the following command
aws cloudformation create-stack --stack-name myinfra --template-body file://myinfra.yml    --parameters file://myinfra-parameter.json  --region=us-east-1

# Create the server stack
aws cloudformation create-stack --stack-name myserver --template-body file://myserver.yml --parameters file://myserver-parameter.json --region=us-east-1

# Link to LoadBalancer DNS
http://myser-webap-1l0jeyx8tdmef-1094030937.us-east-1.elb.amazonaws.com/


