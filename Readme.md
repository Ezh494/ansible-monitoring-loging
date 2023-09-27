# Playbook for installation Monitoring and loging systems
## Roles information
0. static-ip (optional)
* Preparation servers - install statis IP address

1. prometheus
* prometheus
* alertmanager
* grafana

2. ES-kibana
* elasticsearch
* kibana

3. node_exporter
* node_exporter

4. fluent-bit
* fluent-bit

## Installation
### Add servers and identity in the inventory - local
* .\inventories\local\hosts

### Change defaults values and templates for all enabled systems:
1. prometheus, alertmanager, grafana
* roles\prometheus\defaults - Installation values and updates configs
* roles\prometheus\templates - Nginx configs and grafana provisioners

2. elasticsearch, kibana
* roles\ES-kibana\defaults - Installation values 
* roles\ES-kibana\templates - Nginx configs and more options configs ES and kibana

3. node_expoter
* roles\node_expoter\defaults - Installation values

4. fluent-bit
* roles\fluent-bit\defaults - Installation values
* roles\fluent-bit\templates - Configuration fluent-bit

## Start playbook
* ansible-playbook playbook.yml