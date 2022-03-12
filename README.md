# LearnModernDataStack
Learning to use tools and technologies in the modern data stack to create end to end data solutions

In this effort we will be exploring the below mentioned tools and Technologies

# Data Stack #

- Google Cloud ( VM )
- Docker ( For containerization)
- Python ( For general data manipulation and extract/ load process)
- Postgres DB ( Reporting Database)
- SQL ( most important skills to build data pipelines)
- Airbyte ( Data Ingestion)
- Snowflake ( Cloud Data Warehouse )
- DBT ( Transformations)

# High Level Project Plan (Retail Management)

* Setup Google Cloud VM
* Containerization with Docker
  * Miniconda
  * Postgres
  * pgadmin
  * Python
  * metabase
  * snowflake connector
  * Airbyte
  * DBT 
* Setup Snowflake
* Data Ingestion using Airbyte and Python
* Tranformation with DBT
* Answer business question with Metabase

## Setting up Google Cloud

- Go to https://cloud.google.com/ and create a new account with the free trial
- Once you are in the console, follow the the steps below to create a new VM for our project
  - Navigate to console , click on drop down besides Google Cloud Platform banner
    - Click on "New project"
    - Give it a short name as per your liking
    - Keep the organization as default 
    - Navigate to the compute engine section on the left side panel
        - Go to Virtual Machines section and click on VM Instances
        - Enable the Compute Engine API when prompted
        - On the next screen , select the create instance 
          - Choose the appropriate options( I chose the below for our project)
          - E2-standard - 32 GB memory
          - Ubuntu 20.04 LTS
          - 30 GB balanced persistent disk
          - Leave other options ad default
        - Now create SSH keys to enable SSH access from your laptop to the this remote machine
          - Use the link : https://cloud.google.com/compute/docs/connect/create-ssh-keys to generate SSH keys
          - Add SSH keys to google cloud by navigating to Compute Engine ---> metadata --> add SSH keys
          - Copy the public key from the .ssh/key_file.pub and paste it . Click Save 
          - Generate a config file under .ssh folder in your home directory on your local machine
              `Host $Instancename on google cloud
                HostName External IP Address for the VM
                User $localuser on your laptop
                IdentityFile pathname to private key under .ssh`
        
