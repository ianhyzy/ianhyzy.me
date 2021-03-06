---
title: "Prevent Google Docs phishing with one filter"
excerpt_separator: "<!--more-->"
categories:
  - Tutorial
tags:
  - technology
  - Google
  - Ragtag
classes: wide
comments: true
---

<p><b>TL;DR</b>  Don't click links in email messages, especially not requests to share a Drive file</p>{: .notice--primary}

### What's the phishing risk of Docs?
If you use Google Docs and Gmail, you may have seen an email like this before:

![screenshot of request for access email](/assets/images/request-for-access-email.png)

This is a very dangerous email for a few reasons:

* You only see the name of the person requesting - if you want to see their email, you need to hover over their name (or long-press their name if you're on mobile). This allows a bad actor to make a Google account with the same name as someone you may know but with a different email. The sharing interface in Google Drive will show the name of the person and not their email by default. If you aren't careful, you may click the link and approve access for the bad actor. 
* Emails like this can be easily copied by bad actors and sent with phishing links - you may think you're clicking a link to be taken to Google Drive but in reality you would be taken to a malicious webpage.
* It's an immediate call to action that you can complete in a few seconds - even if the request in from a legitimate person you know who thinks they should have access, you only need to slip up and provide someone the wrong access once to create a huge problem. In environments with sensitive data, such as political campaigns, any access request should take more than a few seconds to complete.

So, how do you prevent this type of phishing? The best way is to simply **delete all sharing request emails automatically**. 

The best way to help prevent phiishing attacks is to make sure that you have folders or Shared Drives set up such that you don't need to frequently share individual items. If someone requests access to a doc or folder you control, have them reach out using Hangouts Chat, Slack, Signal, or other sources where you can better identify the person requesting access.

I've created a filter that can filter out all sharing request access messages from Gmail so you aren't provided the opportunity to share in a way that could compromise your organization's data.

To use it, click the gear icon and select `Settings > Filters and Blocked Addresses`. Then, press `Import Filters` on that screen and upload <a href="/assets/mailFilters.xml" download>this file</a>. This will import the filter and any Request for Access emails will be automatically deleted.

If you'd like to set up the filter yourself or customize it to do something other than delete, follow these steps when on Gmail in your browser:

1. Paste this into your Gmail search bar:

`from:(drive-shares-noreply@google.com) subject:("Request for access")`

1. Then click the small down arrow on the right side of the search bar.
2. Then click `Create Filter`
3. Then select what you want to happen to "Request for Access" emails.
4. Then click `Create Filter`

No matter what method you choose, you should see something like this in `Settings > Filters and Blocked Addresses`:
![filter as it appears in settings](/assets/images/drive-sharing-filter.png)

Now that you're no longer seeing request emails, make sure people who may need to legitimately request access know where to contact you to ask. Also note that this won't prevent phishing emails faking the "Request for Access" message from appearing (You could modify a search query to try to find similar messages by keyword, but the false positive rate is high) - but now that you know you won't see any real requests for access you can assume any others you see are fake.

If you need to keep seeing these emails and acting on them - for example, if you're in a political campaign and many of your contributors won't have a way to contact you outside of email - I would still recommend using the filter to label messages and separating them from your regular inbox via a label. You can take the time when you're at a computer to go through your requests and verify they're legitimate before approving them - don't approve anything when you're feeling tired or overwhelmed.