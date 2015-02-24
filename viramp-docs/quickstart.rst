Quick Start Guide
=================

From the AWS (Amazon Web Services) dashboard navigate to “EC2”, then “AMIs”. Change the dropdown box to indicate public instances, then search for “Szpara_Viramp” and click the blue “Launch” button. 

*Note: Only AMIs found in the current Availability Zone will be displayed. Make sure that the Availability Zone found in the upper right hand corner next to your account name is pointing to "US East(N. Virginia).

Due to storage and computational requirements this AMI is not free tier eligible, and the m3.xlarge instance size is recommended. After selecting an instance size follow the prompts until the configure security group page is reached. Three custom TCP rules are required and should be added using the “add rule” button. All three are custom TCP rules and should have the source column as “anywhere” (0.0.0.0) with port ranges 1) 8080, 2) 20-21, and 3) 40000 - 50000. 

With these added, click the “review and launch” button and follow the prompts to create a key pair. 

The instance is now launched and can be accessed under the “instances” tab on the left of the dashboard. Selecting the instance and clicking the “Connect” button will display directions on how to connect to your instance using ssh. 

Once connected, run the run.sh script found in the home directory using screen (screen -> space -> space -> ./run.sh -> Ctrl-a-d). Until the system is stopped internally VirAmp will be accessible by typing the public IP address into the address bar of any internet browser.
