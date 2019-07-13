StreamIO project for Certificate Transparency monitoring with Faust
===================================

This repo contains a sample Faust project to stream Certificate Transparancy data. It includes advanced features of AI in the Cloud utilizing Smart BlockChain with advanced Machine Learning models to detect Phishing Campaigns targetting your organisation.

Just kidding. The project contains a API+WebUI to manage plain and simple keyword monitoring. You have the ability to add regular expressions and fuzzy terms and monitor newly requested certificates. The application makes use of Faust tables to persist transparency offsets. In the case of a crash, the application will still fetch all the missed certificitates during downtime. You'll never miss a certificate :)

Details on how the agents/flows are structured can be found @ https://www.d3vzer0.com/streamio-domain-cert-monitoring/


## 1 Getting started
- **Clone the quickstart repo to your system:** `git clone https://github.com/d3vzer0/streamio --recurse`
- **Navigate to the Ansible  directory:** `cd streamio/ansible`
- **Install pip dependencies:** `pip3 install ansible==2.7.8`

## 2 Install
Be sure to change all the configuration options inside the 'inventories' directory. Set the server IP in the host_vars/phish-dev-01 file and the environment parameters in the group_vars/phishyme file. Make sure you have authenticated to the destination server at least ones over SSH. Then run the following playbooks:

- **Randomly generate DB passwords and API tokens:** `ansible-playbook secrets.yml`
- **Run playbook to build + install components on target server (example)** `ansible-playbook -i inventories/development/hosts.ini phishyme.yml --ask-become-pass --ask-vault-pass`

Running the playbook can be done in various ways. The above example assumes you have your private key cached in the ssh-agent and use sudo for extra privileges. 

The first install/build can take a while depending on your download speeds. When the playbook is finished, you can access the UI via https://<your_server_ip>:8443/#/install to create your first user. You will be redirected to the login window afterwards.

PS. The install API (ie. first user creation) only works when no admin user is present in the DB.

## Example Screenshots (Dummy data)

<img width="1645" alt="match" src="https://user-images.githubusercontent.com/34250156/61177492-22afa980-a5d7-11e9-8260-5889b9bdd776.png">


<img width="1655" alt="screenshots" src="https://user-images.githubusercontent.com/34250156/61177484-fe53cd00-a5d6-11e9-9ec6-2fe681259d30.png">


