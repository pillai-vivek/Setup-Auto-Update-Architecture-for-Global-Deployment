# Setup-Auto-Update-Architecture-for-Global-Deployment
A fully automated script to fetch Zabbix templates, external scripts, and Grafana dashboards from GitHub, then deploy them to your local Zabbix and Grafana environments. Supports .xml, .json, and .yaml template formats and handles automatic format detection and overwriting of existing templates.

# Prerequisite
1). Zabbix Installed on the Server.

2). Grafana Installed on the Server.

3). Edit the auto_update_config.json and Give the : 

    i. zabbix url 
       
       if zabbix is Installed with apache2 then url will be :

          http://34.130.10.46/zabbix/api_jsonrpc.php

       else with nginx : 
          
          http://34.130.10.46/api_jsonrpc.php

    ii. username and password

    iii. grafana url

    iv.  grafana api key generate (Grafana icon --> Administration --> Users and access --> Service accounts --> Add Service Account --> Create service account --> Enter the Display name and Role : Editor or Admin --> Add 
         service account token --> Expiration : No expiration --> Generate token --> Copy the Token)

    v. Repo url (Code --> HTTPS --> copy the url)


# On the Server install Git 
    sudo apt install git
# And run this Comamnd 

    git clone https://github.com/Tools-Automation-Vector-Team/Setup-Auto-Update-Architecture-for-Global-Deployment.git && cd Setup-Auto-Update-Architecture-for-Global-Deployment && chmod +x run.sh && ./run.sh


