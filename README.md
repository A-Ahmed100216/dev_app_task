# Task
Provision the app

## Pre-requisites
1. Starter code


## Steps
1. Clone the starter code.
2. Create a bash script to run commands to install relevant files. This will be titled provision.sh
3. Within the provision.sh file, write out the commands which will install the required files.
`#!/bin/bash

sudo apt-get update
sudo apt-get upgrade
sudo apt-get install nginx -y
sudo apt-get install nodejs -y
sudo apt-get install npm -y
sudo npm install pm2
`
