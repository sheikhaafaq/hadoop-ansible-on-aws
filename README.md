Hadoop Ansible Playbook 
=======================

Hadoop HDFS & MapReduce Multi Node Cluster Setup on AWS EC2 Instances using Ansible Automation.

## Statement :

- Create Ansible [EC2](https://github.com/sheikhaafaq/hadoop-ansible-on-aws/tree/master/workspace/roles/ec2)  Role to launch Nine instances on AWS EC2 Instances.
- Fetch the IPs of EC2 instances dynamically & create the Inventory to run the Ansible Roles on those hosts.
- Create Roles for configuration of  [Hadoop Master Node](https://github.com/sheikhaafaq/hadoop-ansible-on-aws/tree/master/workspace/roles/namenode), [Slave Node](https://github.com/sheikhaafaq/hadoop-ansible-on-aws/tree/master/workspace/roles/datanode) , [Job Tracker Node](https://github.com/sheikhaafaq/hadoop-ansible-on-aws/tree/master/workspace/roles/jobtracker), [Task Tracker Node](https://github.com/sheikhaafaq/hadoop-ansible-on-aws/tree/master/workspace/roles/tasktracker) & [Client Node](https://github.com/sheikhaafaq/hadoop-ansible-on-aws/tree/master/workspace/roles/client).
- Finally configure 1st Instance as Name Node, 2nd & 3rd as Data Nodes, 4th Client Node, 5th as Job Tracker  6th & 7th as Task Trackers.


#### Requirements/Procedure:

- **Ansible v 2.10** should be installed on your local linux system.
- Should have AWS account.
- Clone this [repository](https://github.com/sheikhaafaq/hadoop-ansible-on-aws.git) & go inside the directory **"workspace"**.
- In this workspace copy - **awskey.pem** file & write the values of  AWS access key & secret key in **credentials.yml** file.
- Give permissions to key run `chmod 400 awskey.pem` to secure your AWS key pair from other user on your linux system.

##### Now deploy the setup using setup.yml playbook:

```
$ansible-playbook -v main.yml
```
                              
#### Video Demo: https://ajna.com/ 


