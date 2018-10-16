# Launch Cloud Datalab

**Step 1**     
Open Cloud Shell. The cloud shell icon is at the top right of the Google Cloud Platform web console:  
**Step 2**  
In Cloud Shell, type:  

gcloud compute zones list     

**Step 2**    
In Cloud Shell, type:   

datalab create mydatalabvm --zone <ZONE>    
Note: Please replace <ZONE> with a zone name you picked from the previous step.    

Note: follow the prompts during this process.     

**Step 3**       
Look back at Cloud Shell, and follow any prompts. If asked for a ssh passphrase, just hit return (for no passphrase).     

**Step 4**   
If necessary, wait for Datalab to finish launching. Datalab is ready when you see a message prompting you to do a "Web Preview".   

**Step 5**           
Click on the Web Preview icon on the top-right corner of the Cloud Shell ribbon. Switch or enter the port 8081.        
Note: If the cloud shell used for running the datalab command is closed or interrupted, the connection to your Cloud Datalab VM    
will terminate. If that happens, you may be able to reconnect using the command ‘datalab connect mydatalabvm' in your new Cloud Shell.  

**Clone course repo within your Datalab instance**

**Step 1**   
In Cloud Datalab home page (browser), navigate into "notebooks" and add a new notebook using the icon  on the top left.     
**Step 2**    
Rename this notebook as ‘repocheckout'.       
**Step 3**     
In the new notebook, enter the following commands in the cell, and click on Run (on the top navigation bar) to run the commands:

%bash    
git clone https://github.com/GoogleCloudPlatform/training-data-analyst     
rm -rf training-data-analyst/.git     

**Step 4**    
Confirm that you have cloned the repo by going back to Datalab browser, and ensure you see the training-data-analyst directory. All   
the files for all labs throughout this course are available in this directory.  


