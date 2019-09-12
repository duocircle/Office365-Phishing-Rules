## External Message Banner

As a security precaution, it’s a good idea to remind your staff not to open attachments from unknown senders. One easy way to implement this in Office 365 is by setting up a mail flow rule in the Exchange admin center. If you have ever set up a Disclaimer mail flow rule, the setup is almost identical. In this tutorial, we’ll cover how to setup your own warning message for all external email sent to users inside your organization.
Steps to Configure Attachment Security in Office365

1. Log in to your Office 365 Admin account at: https://portal.office.com
2. Select Admin from your list of Apps
3. Select Admin centers > Exchange (located on the left-side menu)
4. Select mail flow (left side menu)
5. Select the  + icon > Create a new rule…
6. Create a name (Ex: External message warning)
7. For *Apply this rule if…  Select “The sender is located…”, then choose “Outside the organization”.
8. Select “More options…” at the bottom of the new rule window
9. Select “Add condition” > “The recipient is..” > “External/Internal” > then choose “Inside the Organization”.
10. For *Do the following… , select “Apply a disclaimer to the message…” , “prepend a disclaimer”.
11. Select *Enter text…
12. Enter the message you want to prepend to inbound external emails. We recommend keeping it short. If you make it too long, you will get complaints because the users cannot see the preview. Feel free to copy and paste the HTML below for a formatted message like this:

```<p style="border:1px; border-style:solid; border-color: #FFCACA; background-color: #FFCACA; padding: 1em;">
<span style=font-size:12.0pt;color:black;><b>[EXTERNAL EMAIL]</span></b>
<span style=font-size:10.0pt;color:black> DO NOT CLICK links or attachments unless you recognize the sender and know the content is safe.</span></p>```

![External Email Banner Example](https://github.com/duocircle/Office365-Phishing-Rules/blob/master/assets/img/external-message-banner.png)

13. After entering the Text, you’ll need to specify the fall back action. (by clicking “*Select one…”). Choose Wrap, then “OK”.
14. Scroll down and set the Priority level according to any other rules you have configured. If this is the only rule, you can set this to “0”.
15. Click Save

Credit: https://www.securit360.com/blog/configure-warning-messages-office-365-emails-external-senders/