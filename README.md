# Alluvio_Aternity_User_Report

Prerequisites

For the script to get information on your customers, we'll need to add customer information to a file called “account_info.csv” and insure its in the same folder as the script.  

The “account_info.csv”, will need to contain the Account Name and is corresponding Aternity System URL.

To get this information, go to https://access.aternity.com/#/status, copy all Account Names with their corresponding System URL, that you have access to.
Example:-
AccountName,URL
ACB Company,https://us3.aternity.com/
Fake Company,https://us5.aternity.com/
	
Your also need to get a oData password from "https://access.aternity.com/#/status". In the right hand corner, to the right of your aternity username, click the down arrow and click “Generate new data password” or “Generate data password”. A prompt will appear with your odata password, which is required to access and authenticate to the Aternity Rest API.

For MacOS and Linux machines, your first need to confirm that python version 3 is installed. (Open terminal on your machine and type “python3 —version”, if you get “command not found:” then your need to install Python version 3 on your machine.)
	
Run The Script
+++++++++++++++

In a terminal, in the directory of the script, Type “python3 aternity_customer_dashboard_audit.py -u username@company.com", replacing username@company.com with your Aternity Username.
Your then be prompted to enter you odata password.
The script will then run. 
The first time the script runs, it will attempt to install any none standard python libraries that are required, which aren’t already installed on your machine.
The results of the script can be found in a folder called “data” located in the same folder as the script.
The results will be,  raw data from the Rest API call in a json file, plus a spreadsheet of the data parsed. Each customer will have their own raw json and excel spreadsheet file.


N.B. each time the script runs, it creates a new log file “logs.log” and over writes the previous log file. If for some reason the script fails, please check this log file.
