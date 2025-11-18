
---
# Alert to Mattermost with Logic app



This template allows you to create a Logic app that has a webhook to be used from an Azure Alert. When the Alert is triggered, it will post a message to a Mattermost channel that you specify. You need to have a Mattermost account to use this template.

## Linking with Mattermost

After the template deployment has completed, there is a manual step that you must complete before the messages can be posted to the channel. You need to setup an inbound connection in the Mattermost console for this to work. 

## Call from your Alerts

To call this whenever your Alert fires, you need to paste in the webhook URI into the alert:

1. Once the template has completed, navigate to the resource group you deployed it to.
2. Under **Settings**, click on **Deployments**
3. Select the top deployment.
4. Click on **Outputs**. Copy the output called **WebHookURI**.
5. Navigate to the alert you want to trigger the Logic app and select **Edit**.
6. Scroll to the bottom and paste in the **WebHook**.
7. Click save.

`Tags: Microsoft.Web/connections, Microsoft.Logic/workflows, request, object, string, Http, ApiConnection, Mattermost`