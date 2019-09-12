# Friendly From Spoofing

You’ve secured your email system to prevent domain spoofing with DMARC, DKIM, and SPF. 
Now your users are getting email pretending to be from your CEO, with their name and 
signature from some email address not on your domain. Let’s block those!

Our CEO for this example will be Bruce Wayne and your users are getting emails like this:

=======================================

From: Bruce Wayne <theceo125451@aol.com>
To:  Alfred Pennyworth <alfred@wayneenterprises.com>
Subject: Urgent!

Hey Alfred,

I’m out of the office right now and I lost my cell phone but I really need to you pick me up some iTunes Gift Cards real fast so I can hand them out at this event. Respond to this email and I’ll give you the details

Bruce Wayne
CEO
Wayne Enterprises

=======================================

Looks legit enough to pass by spam filters, which have no way of knowing if “theceo125451@aol.com” is Bruce Wayne’s personal email or not. 
And if you block that address, the spammers will just send from another one.

So, lets make a rule to block ALL emails that have “Bruce Wayne’s” name in the sender header, but come from outside the organization. 
Then, let your CEO know that this will block his personal email address from sending to employees or tweak the rule to allow it 
from his personal OR work.

## HERE IS HOW TO SET UP THE RULE:

- Log into your Admin Portal and the Exchange admin center
- Click on “Mail Flow” and then “Rules”
- Create a new rule, and click on “more options…” at the bottom to get all the fields
- Name the rule whatever you want
- Set *Apply this rule if… to
- The sender is internal/external
- then pick Outside the organization
- then click add a condition
- and add The sender…
- and pick address matches any of these text patterns
- then plug in the variations of your CEO, accountant, etc… names that you’d like to prevent people from spoofing
- Under *do the following…, select the action you’d like to occur when a match is found. You can have Office forward the emails to you to monitor the activity. Check the audit box if you’d like Office to track the rule activity too.
- Hit save

![Friendly From Spoofing](https://github.com/duocircle/Office365-Phishing-Rules/blob/master/assets/img/block-office-365-email-spoofing-friendly-name.jpg)



Credit - https://www.itjon.com/blocking-those-obnoxious-phishing-emails-with-spoofed-friendly-display-name-on-office-365/
