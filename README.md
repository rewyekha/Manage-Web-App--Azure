# Manage-Web-App--Azure
I will deploy a line of business web application. I will provision a web app, configure autoscale for the web app, and deploy a web job to support the web app.
--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------

## A. Deploy a Web App via the Azure portal

1. Sign in to the Azure portal. 
2. Use the region associated with the WebAppslod* resource group for all resources that you provision.
3. Create an App Service Plan named ASP-Portal by using the S1 performance tier in the WebAppslod* resource group.
4. Create a Windows code-based Web App named mms3* in the ASP-Portal App Service Plan.
5. Deploy code from https://lodschallenges.blob.core.windows.net/mms/deploy.zip to the Web App.
6. Add an application settings named challengeNumber with a value of 4.
7. Add a custom connection string named storageConnection to the mms3* with the connection string for the sa3* Storage Account.
8. Verify that the mms3* loads and operates properly.

--- Check your work ---

Hint
https://docs.microsoft.com/en-us/azure/app-service/deploy-zip

-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------

## B. Configure autoscale

1. Create a queue named process in the sa33* Storage Account.
2. Enable autoscale for the mms3* Web App.
3. Set the default scale condition to scale between 1 and 5 instances based on the process queue in the sa3* Storage Account. Scale out if the queue length exceeds 3 messages, and scale in if the queue length is 3 or less.
4. Add a second scale condition named Friday to the mms3* Web App that scales to 2 instances from 6:00PM to 11:59 PM on Fridays.
5. Add another scale condition named Weekend to the mms3* Web App that scales to 2 instances all day Saturday and Sunday.
6. Use the Generate Messages button on the home page of the mms3* to generate queue messages and test autoscale.
NOW!

--- Check your work ---


hint
https://docs.microsoft.com/en-us/azure/azure-monitor/platform/autoscale-get-started

-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------

## C. Provision a Web Job

1. Configure the mms3* Web App to host a continuous Web Job.
2. Add a custom connection string named AzureWebJobsDashboard with the connection string for the sa3* Storage Account to the mms3* Web App.
3. Add a custom connection string named AzureWebJobsStorage with the connection string for the sa3* Storage Account to the mms3* Web App.
4. Note that both connection strings have very similar names and the same value.

5. Add a Continuous Web Job named QueueProcessor to the mms34504887 Web App by using the portal. Use the deployment package from https://lodschallenges.blob.core.windows.net/mms/MMSWebjob.zip.
6. Use the Generate Messages button on the home page of the mms34504887 Web App to generate queue messages.
7. Select the Validate Web Job button to verify that the Web Job processed the queue items.

Finally!!!
--- Check your work --- ALL Running ?


Hint
https://docs.microsoft.com/en-us/azure/app-service/webjobs-create

-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------

## Summary
Congratulations, you have completed the Can You Manage a Web App? 

You have accomplished the following:

Provisioned a Web App.
Configured autoscale for a Web App.
Deployed a Web Job.

------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------
If any doubt, reach out to me on Linkdin!
