# Dynatrace-Weekly-License-Usage-Update-Workflow
This is a workflow leveraging the Account Management API to pull in data about Dynatrace license utilisation for DPS 

The first step will be to upload the workflow json, the Dynatrace documentation here provides the steps on how to do so https://docs.dynatrace.com/docs/analyze-explore-automate/workflows/manage-workflows/workflows-upload

Once it has been uploaded this is what the workflow will look like
![image](https://github.com/user-attachments/assets/110d4889-beff-4cd0-8dd3-5a13bdd5c19f)

In the Javascript action called collect_license_usage you will need to insert your client id, client secret, and account uuid. 

This documentation here will assist you with how to procure an OAuth2 client as this is required for the Account Manage API that is leveraged https://docs.dynatrace.com/docs/manage/identity-access-management/access-tokens-and-oauth-clients/oauth-clients

Further more you will also be required to provide your subscription ID for the relevant subscription that you are wanting weekly updates on.

This API here will provide all the subscriptions on your account and you will need to choose the subscription ID for the subscription to be updated on weekly https://docs.dynatrace.com/docs/discover-dynatrace/references/dynatrace-api/account-management-api/dynatrace-platform-subscription-api/subscriptions/get-all

![image](https://github.com/user-attachments/assets/762a79f6-743b-4b64-9816-272355f32e8b)

After you have provided the relevant items to the variables in the Javascript, all that is remaining is for you to add in the recipients as well as customise the email content.

![image](https://github.com/user-attachments/assets/4f5ba449-c243-4fd9-a76e-7b2e7d0dc84c)

After you have added your client id, client secret, account uuid, subscription uuid, and the email recipients you are ready to recieve usage updates, be sure to modify the schedule in accordance with your desired timing and update frequency requirements
<img width="1132" alt="image" src="https://github.com/user-attachments/assets/5c706c9f-fe07-4efb-afe6-ed11547fc818" />
