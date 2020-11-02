# Configure Exchange Online to reject emails that fail DMARC validation with organizations having policy of reject

By default Office 365 DMARC validation for internet emails that fails for policy P=Reject will make the email to land in junk folder of the recipient mailbox. Microsoft 365 will treat DMARC policies of quarantine and reject in the same way, which means that if the sender’s DMARC policy is set to reject or quarantine, the emails that fail DMARC will be sent to the junk folder of the recipient mailbox which is by design as of now and can be found in the [Microsoft Article](https://docs.microsoft.com/en-us/microsoft-365/security/office-365-security/use-dmarc-to-validate-email?view=o365-worldwide#how-microsoft-365-handles-outbound-email-that-fails-dmarc).

For a successful email from a legitimate sender where it has passed spf, dkim & dmarc we see the below value for DMARC.

`dmarc=pass action=none`

### WorkAround:

A workaround can be accomplished by creating a Transport Rule to reject the emails that fails with the DMARC validation.

### Create a Transport Rule:

Include the below value `oreject` or `action=oreject` or `dmarc=fail` in the message header include option.

Reject the message with the custom status code.

![Transport Rule](https://github.com/duocircle/Office365-Phishing-Rules/blob/master/assets/img/reject2.png)