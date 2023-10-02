### GCP Setup Process

First, I navigated to "SQL" on the sidebar of the Google Cloud Console. Then, I clicked on "Create an instance", prompting a selection of "MySQL". Afterwards, I configured the instance, filling out necessary info. For this specific instance, I choose the Enterprise, Sandbox, Shared core, 1vCPU/.614gb RAM, and configured the network that allowed any IP (0.0.0.0/0). Then, I deployed it and it took Google Cloud almost 15 minutes. When setting up the MySQL Connection on MySQL Workbench, the username remained as root and hostname was the Public IP address.
Browse more instructions for [Creating a MySQL instance on GCP](https://cloud.google.com/sql/docs/mysql/create-instance)

### Azure Setup Process

First, I navigated to "Azure Database for MySQL" through the Azure Portal and selected Flexible server. Then, I configured the basics and networking with "Burstable" tier and "B1S" compute. I also allowed public access and initially I did not set any firewall rules. The deployment time was quicker than GCP. When connecting with MySQL Connection on MySQL Workbench, the username was the server admin name from Azure and hostname was the server name from Azure. Browse more instructions for [Creating a MySQL instance on Azure](https://learn.microsoft.com/en-us/azure/mysql/flexible-server/quickstart-create-server-portal)

### My MySQL Workbench Experience

Overall, I had a good experience. It was easy to navigate and I did not experience any difficulties creating the ERD and I liked that it was simple to change the relationships of the tables. Also, I preferred that when the syntax of a certain command would result in an error, there would be a red "X" on the left side to let you know. I had to keep in mind of SQL syntax when running commands, which took some time to get used to. ERD pic is uploaded to "MySQL Workbench" folder. I used the same data for Azure and GCP connection so diagram was the same.

### Errors

1) Running the Insert Into SQL Command

I successfully ran the "CREATE TABLE", "CREATE DATABASE" and "SELECT" SQL commands. But I had issues running the "INSERT INTO" command. I wanted to insert a into a specific column, but it  returned error codes of 1136, 1064, 1364, after resolving one after another. Error code: 1364 showed the field doesn't have a default value (not the field I wanted to insert value into). Pic is also uploaded in "MySQL Workbench" folder.

2) Connecting Azure MySQL Connection and MySQL Workbench

Initially I received a Failed to Connect error of "Unable to connect to localhost". Then I searched and to resolve it, I set a Firewall rule of Start IP address 0.0.0.0 and End IP address 255.255.255.255. I was able to successfully connect after that. Pic is uploaded to "MySQL set up documentation" folder and under the "Azure" folder.
