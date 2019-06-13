StreamIO project for Certificate Transparency monitoring with Faust
===================================

This repo contains a sample Faust project to stream Certificate Transparancy data. It includes advanced features of AI in the Cloud utilizing Smart BlockChain with advanced Machine Learning models to detect Phishing Campaigns targetting your organisation.

Just kidding. The project contains a API+WebUI to manage plain and simple keyword monitoring. You have the ability to add regular expressions and fuzzy terms and monitor newly requested certificates. The application makes use of Faust tables to persist transparency offsets. In the case of a crash, the application will still fetch all the missed certificitates during downtime. You'll never miss a certificate :)


## 1 Getting started
- **Clone the quickstart repo to your system:** `git clone https://github.com/d3vzer0/streamio --recurse`
- **Navigate to the Ansible  directory:** `cd streamio/ansible`
- **Install pip dependencies:** `pip3 install ansible==2.7.8`

## 2 Install
Todo