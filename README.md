# Project1
Cybersecurity wk 13 project1
## Automated ELK Stack Deployment

The files in this repository were used to configure the network depicted below.

![ELK Red Team](https://user-images.githubusercontent.com/69772235/100253746-7b06f300-2f0f-11eb-8f5c-4bb16f96bd2f.png)

These files have been tested and used to generate a live ELK deployment on Azure. They can be used to either recreate the entire deployment pictured above. Alternatively, select portions of the Playbook YML file may be used to install only certain pieces of it, such as Filebeat.

![Elkyml](https://user-images.githubusercontent.com/69772235/100255825-07b2b080-2f12-11eb-9597-38ef95e70761.PNG)

This document contains the following details:
- Description of the Topology
- Access Policies
- ELK Configuration
  - Beats in Use
  - Machines Being Monitored
- How to Use the Ansible Build


### Description of the Topology

The main purpose of this network is to expose a load-balanced and monitored instance of DVWA, the D*mn Vulnerable Web Application.

Load balancing ensures that the application will be highly available, in addition to restricting unauthorized access to the network.
Load Balancing can be a security defense against Distributed Denial-of-Service (DDoS) attacks.
Using a Jump Box controls access to the network by only allowing connection from specific IP addresses, protecting the respective virtual machines within the network.

Integrating an ELK server allows users to easily monitor the vulnerable VMs for changes to the log files and system traffic.
Filebeat watches for changes in a system by collecting data from the various logs generated by the machine.
Metricbeat monitors the performance and metrics of the machine.

The configuration details of each machine may be found below.

| Name     | Function | IP Address      | Operating System |
|----------|----------|-----------------|------------------|
| Jump Box | Gateway  | 20.51.230.227   | Linux            |
| Web1     |Web Server| 10.0.0.5        | Linux            |
| Web2     |Web Server| 10.0.0.6        | Linux            |
|Elk Server| ELK      | 40.83.183.119   | Linux            |
|RedTeam_LB|Balancing | 52.249.196.23   |                  |

### Access Policies

The machines on the internal network are not exposed to the public Internet. 

Only the Jump-Box machine can accept connections from the Internet. Access to this machine is only allowed from the following IP addresses:
71.225.xx.xxx/32

Machines within the network can only be accessed by SSH.
The Jump Box Provisioner is allowed access to the ELK machine.  The Jump Box IP is 20.51.230.227

A summary of the access policies in place can be found in the table below.

| Name     | Publicly Accessible | Allowed IP Addresses |
|----------|---------------------|----------------------|
| Jump Box | Yes                 |70.225.xx.xxx         |
| Web1     | No                  |10.0.0.4              |
| Web2     | No                  |10.0.0.4              |
| ELK      | No                  |10.0.0.4              |

### Elk Configuration

Ansible was used to automate configuration of the ELK machine. No configuration was performed manually, which is advantageous because...
- _TODO: What is the main advantage of automating configuration with Ansible?_

The playbook implements the following tasks:
- _TODO: In 3-5 bullets, explain the steps of the ELK installation play. E.g., install Docker; download image; etc._
- ...
- ...

The following screenshot displays the result of running `docker ps` after successfully configuring the ELK instance.

![TODO: Update the path with the name of your screenshot of docker ps output](Images/docker_ps_output.png)

### Target Machines & Beats
This ELK server is configured to monitor the following machines:
10.0.0.5 (Web1) & 10.0.0.6 (Web2)

We have installed the following Beats on these machines:
FileBeat & MetricBeat

These Beats allow us to collect the following information from each machine:
- _TODO: In 1-2 sentences, explain what kind of data each beat collects, and provide 1 example of what you expect to see. E.g., `Winlogbeat` collects Windows logs, which we use to track user logon events, etc._

### Using the Playbook
In order to use the playbook, you will need to have an Ansible control node already configured. Assuming you have such a control node provisioned: 

SSH into the control node and follow the steps below:
- Copy the _____ file to _____.
- Update the _____ file to include...
- Run the playbook, and navigate to ____ to check that the installation worked as expected.

_TODO: Answer the following questions to fill in the blanks:_
- _Which file is the playbook? Where do you copy it?_
- _Which file do you update to make Ansible run the playbook on a specific machine? How do I specify which machine to install the ELK server on versus which to install Filebeat on?_
- _Which URL do you navigate to in order to check that the ELK server is running?

_As a **Bonus**, provide the specific commands the user will need to run to download the playbook, update the files, etc._
