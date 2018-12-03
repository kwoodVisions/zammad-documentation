Email
*****

Basic
=====

If you want to fetch emails via POP3 or IMAP, you have to create a mail channel in system settings "#channels/email".

**If you're using an Office365 Mailbox, please ensure that it's a real usermailbox and not a shared mailbox!**

Just follow these steps:

* Click "New"
* Enter "Organization & Department Name"
* Enter "Email address"
* Enter "Password"
* Enter "Destination Group"

Zammad tries to detect the POP3, IMAP and SMTP server settings automatically.
This should work most of the time. If it doesn't, use the "Experts" button to configure it by yourself.

For Office 365 Users
********************

If you are going to use an Office 365 account, it must be an active account that can be logged into, not a shared account, as the current authentication protocols for Office 365 are better suited towards an active account.  If you have multiple departments that may be receiving tickets, it would be best to have one central email address that is used for incoming tickets, and then within the system, assign those tickets to a particular group.

Since Zammad will most likely not be able to detect the settings, below are the recommended settings for an Office 365 email configuration to send and receive:

Email Inbound Settings:

* Type = IMAP
* Host = outlook.office365.com
* User = helpdeskemail@yourdomain.com
* Password = emailAccountPassword
* SSL/STARTTLS = yes
* Port = 993
* Keep Messages On Server = Yes (this is important for testing so you can ensure messages are coming and going)

Email Outbound Settings:

* Send Mails Via = SMTP
* Host = outlook.office365.com
* User = helpdeskemail@yourdomain.com
* Password = emailAccountPassword
* Port = 25

Email Notification Settings:

* Send Mails Via = SMTP
* Host = smtp.office365.com
* User = helpdeskemail@yourdomain.com
* Password = emailAccountPassword
* Port = 25

Advanced
========

.. toctree::
   :maxdepth: 1

   channel-email/fetchmail
   channel-email/sendmail
