# Playbook for installation Monitoring and loging systems
**This playbook has been tested only on Ubuntu 20+ system!!!**
## Roles information
static-ip (optional)
* Preparation servers - install statis IP address 

prometheus
* prometheus
* alertmanager
* grafana

ES-kibana
* elasticsearch
* kibana

node_exporter
* node_exporter

fluent-bit
* fluent-bit

## Installation
### Add servers and identity in the inventory - local
.\inventories\local\hosts

### Change defaults values and templates for all enabled systems:
prometheus, alertmanager, grafana
* roles\prometheus\defaults - Installation values and updates configs
* roles\prometheus\templates - Nginx configs and grafana provisioners

elasticsearch, kibana
* roles\ES-kibana\defaults - Installation values 
* roles\ES-kibana\templates - Nginx configs and more options configs ES and kibana

node_expoter
* roles\node_expoter\defaults - Installation values

fluent-bit
* roles\fluent-bit\defaults - Installation values
* roles\fluent-bit\templates - Configuration fluent-bit

## Start playbook
ansible-playbook playbook.yml