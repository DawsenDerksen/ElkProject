# ElkProject
The files in this repository were used to configure the network depicted below.
​
!(/ElkProject-main/Images/diagram_filename.png)
​
These files have been tested and used to generate a live ELK deployment on Azure. They can be used to either recreate the entire deployment pictured above. Alternatively, select portions of the "Config" file may be used to install only certain pieces of it, such as Filebeat.
​
  - _filebeat-playbook.yml_
​
This document contains the following details:
- Description of the Topologu
- Access Policies
- ELK Configuration
  - Beats in Use
  - Machines Being Monitored
- How to Use the Ansible Build
​
​
### Description of the Topology
​
The main purpose of this network is to expose a load-balanced and monitored instance of DVWA, the D*mn Vulnerable Web Application.
​
Load balancing ensures that the application will be highly stable, in addition to restricting denial of service to the network.
-  Loadbalancers help protect the availablity of a network from denial of service attacks and helps make the system more stable. Advantages if a jump box include allowing safe and secure access to seperate VMs_
​
Integrating an ELK server allows users to easily monitor the vulnerable VMs for changes to the _____ and system _____.
Filebeat watches for log events and captures that data
Metricbeat records metrics from the operating system and the applicatons/services that are installed on the machine
​
The configuration details of each machine may be found below.
​
|   Name   |       Function       | IP Address | Operation System |
|:--------:|:--------------------:|:----------:|:----------------:|
| Jump Box |        Gateway       |  10.0.0.4  |       Linux      |
|   Web 1  |       Container      |  10.0.0.5  |       Linux      |
|   Web 2  |       Container      |  10.0.0.6  |       Linux      |
| DVWA-VM2 | Vulnerabilty Scanner |  10.0.0.7  |       Linux      |
|  Elk-VM  |       Database       |  10.1.0.4  |       Linux      |
​
### Access Policies
​
The machines on the internal network are not exposed to the public Internet. 
​
Only the Jump Box machine can accept connections from the Internet. Access to this machine is only allowed from the following IP addresses:
"User's home IP Address"
​
Machines within the network can only be accessed by the Jump Box.
- Web 1 was allowed access to the Elk VM. Web 1's IP address is 10.0.0.5
​
A summary of the access policies in place can be found in the table below.
​
|   Name   | Publicly Accessible | Allowed IP Addresses |
|:--------:|:-------------------:|:--------------------:|
| Jump Box |          No         |        Home IP       |
|   Web 1  |          No         |       10.0.0.4       |
|   Web 2  |          No         |       10.0.0.4       |
|  Elk VM  |          No         |   10.0.0.5/10.0.0.6  |
​
### Elk Configuration
​
Ansible was used to automate configuration of the ELK machine. No configuration was performed manually, which is advantageous because it cuts the time in half and makes it alot easier.
​
The playbook implements the following tasks:
- Install docker.io 
- Install pip3
- Install Docker python module
- Increase virtual memory
- Use more memory
- download and launch a docker elk container
​
The following screenshot displays the result of running `docker ps` after successfully configuring the ELK instance.
​
![TODO: Update the path with the name of your screenshot of docker ps output](Images/docker_ps_output.png)
​
### Target Machines & Beats
This ELK server is configured to monitor the following machines:
- _TODO: List the IP addresses of the machines you are monitoring_
​
We have installed the following Beats on these machines:
- _TODO: Specify which Beats you successfully installed_
​
These Beats allow us to collect the following information from each machine:
- _TODO: In 1-2 sentences, explain what kind of data each beat collects, and provide 1 example of what you expect to see. E.g., `Winlogbeat` collects Windows logs, which we use to track user logon events, etc._
​
### Using the Playbook
In order to use the playbook, you will need to have an Ansible control node already configured. Assuming you have such a control node provisioned: 
​
SSH into the control node and follow the steps below:
- Copy the _____ file to _____.
- Update the _____ file to include...
- Run the playbook, and navigate to ____ to check that the installation worked as expected.
​
_TODO: Answer the following questions to fill in the blanks:_
- _Which file is the playbook? Where do you copy it?_
- _Which file do you update to make Ansible run the playbook on a specific machine? How do I specify which machine to install the ELK server on versus which to install Filebeat on?_
- _Which URL do you navigate to in order to check that the ELK server is running?
​
_As a **Bonus**, provide the specific commands the user will need to run to download the playbook, update the files, etc._
