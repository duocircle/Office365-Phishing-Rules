# Office365 Phishing Transport Rules

Example transport rules that can be implemented without using ATP to block some common types of Phishing on Office 365.

**ATP is an excellent option if you have an E5 license and above.** If not, please feel free to browse these rules and adapt them for your environment. 

Your environment should have at least one of the rules from each of the sections to help protect against Office 365 phishing. 

*These rules are accurate at the time of posting but Microsoft is constantly updating their interface and some steps may be different.*


## Sender Spoofing

[Friendly FROM: Address](/friendly-from/README.md)

## Display Banners

[External Message Banner](/external-sender/README.md)

## Security Controls

- [Enabling 2FA in Office 365](/security/office365-enable-2fa.md)
- [Enabling FIDO2 in Office 365](/security/office365-enable-FIDO2.md)

## Domain Spoofing


## DKIM / DMARC

- [Setup DKIM/DMARC in O365](https://github.com/duocircle/Office365-Setup-DKIM-DMARC-SPF)
- [Enforce DMARC Policies Transport Rule](/security/dmarc-reject-transport.md)



## Microsoft OFFICIAL

[Mail flow rules (transport rules) in Exchange Online](https://docs.microsoft.com/en-us/exchange/security-and-compliance/mail-flow-rules/mail-flow-rules)

[Mail flow rule conditions and exceptions (predicates) in Exchange Online](https://docs.microsoft.com/en-us/exchange/security-and-compliance/mail-flow-rules/conditions-and-exceptions)

## Setup Message Reporting

[Enable the report Message Add-in](https://docs.microsoft.com/en-us/microsoft-365/security/office-365-security/enable-the-report-message-add-in?view=o365-worldwide)

[See what your users are reporting using a transport rule](https://docs.microsoft.com/en-us/microsoft-365/security/office-365-security/use-mail-flow-rules-to-see-what-your-users-are-reporting-to-microsoft?view=o365-worldwide)


## Third Party Rules

[Blocking email spam with the Office 365 spam filter (for administrators)](https://www.clouddirect.net/knowledge-base/KB0011008/blocking-email-spam-with-the-office-365-spam-filter-for-administrators)


## Outlook 365 Dark Mode

Dark mode (black background rather than a white reading pane) makes it easy to spot fake attachments, and hidden text links. 
You would be amazed at the amount deception that can be uncovered in the dark. 

[Enable dark mode in Outlook](https://support.office.com/en-us/article/dark-mode-in-outlook-3e2446e0-9a7b-4189-9af9-57fb94d02ae3)