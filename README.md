# AWS CLI COMMANDS

Value refers to the id of the resources in the aws 

Example: 

instance id : i-0155239af7d3f1523

Remove the value and add the instance id 

1.Creating the Instances:
-----------------------------
aws ec2 run-instances --image-id ami-09ba48996007c8b50 --count 1 --instance-type t2.micro --key-name wdde17

2.Describe the Instances
-------------------------
aws ec2 describe-instances

3.To start the Instances
-------------------------
aws ec2 start-instances --instance-ids value

4.To Stop the Instances
------------------------
aws ec2 stop-instances --instance-ids value

5.To terminate the Instances 
----------------------------
aws ec2 terminate-instances --dry-run --instance-ids value

6.To reboot the Instances
--------------------------
aws ec2 reboot-instances --instance-ids value

7.To create AMI
------------------
aws ec2 create-image --instance-id value --name "Image_name" --description "AMI_for_development_server"

8.Creating the volume 
---------------------
aws ec2 create-volume --size Value --availability-zone Value

9.Describe the Volume
----------------------
aws ec2 describe-volumes

10.To attach the volume to the instance
--------------------------------------
aws ec2 attach-volume  --volume-id value --instance-id value --device /dev/sdh

11. 



