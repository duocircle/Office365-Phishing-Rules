# Office365 Phishing Transport Rules

These are some example transport rules that can be implemented without using ATP to block some common types of Phishing on Office 365.

**ATP is an excellent option if you have an E5 license and above.** If not, please feel free to browse these rules and adapt them for your environment. 

Your environment should have at least one of the rules from each of the sections to help protect against Office 365 phishing. 

*These rules are accurate at the time of posting but Microsoft is constantly updating their interface and some steps may be different.*

## Sender Spoofing

[Friendly FROM: Address](/friendly-from/README.md)

## Display Banners

[External Message Banner](/external-sender/README.md)

## Domain Spoofing


## DKIM / DMARC


## Microsoft OFFICIAL

[Mail flow rules (transport rules) in Exchange Online](https://docs.microsoft.com/en-us/exchange/security-and-compliance/mail-flow-rules/mail-flow-rules)

[Mail flow rule conditions and exceptions (predicates) in Exchange Online](https://docs.microsoft.com/en-us/exchange/security-and-compliance/mail-flow-rules/conditions-and-exceptions)

## Third Party Rules

[Blocking email spam with the Office 365 spam filter (for administrators)](https://www.clouddirect.net/knowledge-base/KB0011008/blocking-email-spam-with-the-office-365-spam-filter-for-administrators)