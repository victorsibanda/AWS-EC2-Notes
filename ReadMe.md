# AWS :cloud:


### What is an EC2?
An EC2 is Elastic Compute Cloud which allows you to develop applications in the cloud using an amazon server. You can change how much computing power you want depending on the applications.

#### To set up an EC2
Using AWS go on to their website and create an instance.
- Choose an Operating System - Ubuntu Server 18.04 LTS
- Decide on an instance - t2.micro
- Network Configurations - DevOpsStudent - DevOpsStudentSubnet
- Add Storage (You may add additional storage we skipped this step)
- Add Tags - This is to identify your EC2 - We used a 'Name' tag and a 'Cohort' tag.
- Set up a Security Group - A security group allows you to add restrictions to who can access the EC2 and on what ports they can use.  
 - For our setup we used ports 80,22,8080,443 and 3000 to access our personal IP's.
- The final step is creating a key, which has to be saved in ~/.ssh or other secure folder, away from your code, that way only you can access your server and vulnerability is removed.

### SSH into EC2
```
ssh -i <Location of Key/Keyname> ubuntu@ <ip>

```
`-i`  is the identity file, which should be the key.
`Location of Key/Keyname` is where the key is located and the name of the key.
`ip` is the IPv4 IP on the AWS Machine

### Transfer Files into EC2

To Transfer a file onto the AWS machine use SCP, use:

```
scp -i path/to/key file/to/copy user@ec2-xx-xx-xxx-xxx.compute-1.amazonaws.com:path/to/file

```

To transfer a whole directory use:

```
scp -i path/to/key -r directory/to/copy user@ec2-xx-xx-xxx-xxx.compute-1.amazonaws.com:path/to/directory

```
