# AWS CLI 

# Installation of AWS CLI 

On Linux:
---------

1. 64-bit:

   curl "https://awscli.amazonaws.com/awscli-exe-linux-x86_64.zip" -o "awscliv2.zip"
   
   unzip awscliv2.zip
   
   sudo ./aws/install

2. Linux ARM

   curl "https://awscli.amazonaws.com/awscli-exe-linux-aarch64.zip" -o "awscliv2.zip"
   
   unzip awscliv2.zip
   
   sudo ./aws/install
   
On macOS:
---------

   curl "https://awscli.amazonaws.com/AWSCLIV2.pkg" -o "AWSCLIV2.pkg"
   
   sudo installer -pkg AWSCLIV2.pkg -target /
   
On Windows:
-----------
   
   msiexec.exe /i https://awscli.amazonaws.com/AWSCLIV2.msi


NOTE:
------

Value refers to the id of the resources in the aws 

Example: 

instance id : i-0155239af7d3f1523

Remove the value and add the instance id,Volume id, AMI id etc.., 

Configuring the aws cli in the local system
---------------------------------------------

Note:
-----

Before using all the commands first we need to configure the AWS by creating the IAM User with the required permission along with the access keys and secret access keys 

To configure the AWS CLI 
-------------------------
aws configure 

output:

AWS Access Key ID []: Enter the access key 

AWS Secret Access Key []: Enter the secret access key

Default region name []: Enter the region code 

Default output format [json]: Enter the Output format like Text,json,table,yml choose anyone




To create the Key Pair
-----------------------
aws ec2 create-key-pair --key-name name_of_the_keypair

Describe the Key pair
---------------------
aws ec2 describe-key-pairs

Delete the Key Pair
-----------------
aws ec2 delete-key-pair --key-name name_of_the_keypair

Creating the Instances
-----------------------------
aws ec2 run-instances --image-id ami-09ba48996007c8b50 --count 1 --instance-type t2.micro --key-name wdde17

Describe the Instances
-------------------------
aws ec2 describe-instances

To start the Instances
-------------------------
aws ec2 start-instances --instance-ids value

To Stop the Instances
------------------------
aws ec2 stop-instances --instance-ids value

To terminate the Instances 
----------------------------
aws ec2 terminate-instances --dry-run --instance-ids value

To reboot the Instances
--------------------------
aws ec2 reboot-instances --instance-ids value

To create AMI
------------------
aws ec2 create-image --instance-id value --name "Image_name" --description "AMI_for_development_server"

Describe the Images
---------------------
aws ec2 describe-images

De-register AMI
------------------
aws ec2 deregister-image --image value

To create the IAM Groups
-------------------------
aws iam create-group --group-name name_of_the_group

To create the IAM Users
-----------------------
aws iam create-user --user-name name_of_the_user

To add the users to the group
------------------------------
aws iam add-user-to-group --user-name name_of_the_user --group-name name_of_the_group

To see the complete information of group
-----------------------------------------
aws iam get-group --group-name name_of_the_group

Creating the volume 
---------------------
aws ec2 create-volume --size Value --availability-zone Value

Describe the Volume
----------------------
aws ec2 describe-volumes

To attach the volume to the instance
--------------------------------------
aws ec2 attach-volume  --volume-id value --instance-id value --device /dev/sdh

To detach the volume to the instance
-------------------------------
aws ec2 detach-volume --volume-id value

 



