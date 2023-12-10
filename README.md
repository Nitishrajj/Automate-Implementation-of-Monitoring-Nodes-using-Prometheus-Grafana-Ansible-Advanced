# Automate Implementation of Monitoring Nodes using Prometheus Grafana Ansible

# Ansible 
Ansible is an open-source automation tool that simplifies configuration management, application deployment, task automation, and orchestration. 

# Grafana 
 Grafana serves as the visualization and dashboarding platform, providing an intuitive and customizable interface for monitoring and analyzing data. Dashboards are crafted to offer a real-time, consolidated view of critical metrics, empowering DevOps teams to make informed decisions promptly. The monitoring solution is designed to be scalable, accommodating the growth of the infrastructure. Grafana's flexibility ensures adaptability to diverse infrastructure setups, making it suitable for both small-scale and large-scale deployments.

# Prometheus 
Prometheus acts as the core monitoring and alerting component, responsible for collecting and storing time-series data from various nodes in the infrastructure. Customizable Prometheus queries enable the extraction of relevant metrics, empowering operators to gain insights into resource utilization, system performance, and potential bottlenecks.

# Node Exporter 
Node Exporter collects a variety of metrics related to the host machine's operating system and hardware. This includes information about the CPU, memory, disk, network, and other system-level resources. Node Exporter is designed to work seamlessly with Prometheus, a popular open-source monitoring and alerting toolkit. Prometheus scrapes (pulls) metrics from Node Exporter endpoints at regular intervals. Node Exporter exposes metrics through HTTP endpoints, typically on port 9100 by default. Prometheus scrapes these endpoints to collect the metrics. The exposed metrics follow the Prometheus exposition format.

# Getting Started 
In this project we are using Ansible playbooks to do the configuration in the nodes respectively. Generally in Ansible we can use Adhoc commands or ansible playbooks (.yml file) for the configuration management and automation. 
Basically, Ansible adhoc commands are used when you want to execute small commands (like "ls", etc) but when you want to execute bigger commands for configuration management or deploymet or automation it is suggested to use Ansible playbooks. 
Since our project deals with larger commands we have used Ansible playbooks (.yml file)

Ansible (.yml file ) explanation. 
We have used Ansible roles to keep our ansible in a structured way 
In Ansible, roles are a way to organize and structure your playbooks by breaking them into smaller, reusable components. In a simpler way a role is to organize playbooks and reuse them.  Here we have 3 different things to do 1 is installing and configuring grafana (which is our role 1) 2 is configuring node exporter in our nodes (role 2 ) and 3 is configuring prometheus to scrape metrics using node exporter  (role 3). 
So, we have created 3 roles in roles folder
