# AWS CLI COMMANDS

Value refers to the id of the resources in the aws 

Example: 

instance id : i-0155239af7d3f1523

Remove the value and add the instance id 

1.Creating the ionstances:
-----------------------------
aws opsworks --region ap-south-1 create-instance --stack-id value --layer-ids value --hostname name_of_the_instance --instance-type Type_of_Instance --ssh-key-name Key pair name --os "Amazon Linux" 

2.Describe the Instances
-------------------------
aws ec2 describe-instances

3.To start the Instances
-------------------------
aws ec2 start-instances --instance-ids value

4.To Stop the Instances
------------------------
aws ec2 stop-instances --instance-ids value

5.To terminate the instance 
----------------------------
aws ec2 terminate-instances --dry-run --instance-ids value

6.Creating the volume 
---------------------
aws ec2 create-volume --size Value --availability-zone <Value>

7.Describe the Volume
----------------------
aws ec2 describe-volumes

8.To attach the volume to the instance
--------------------------------------
aws ec2 attach-volume  --volume-id value --instance-id value --device /dev/sdh

