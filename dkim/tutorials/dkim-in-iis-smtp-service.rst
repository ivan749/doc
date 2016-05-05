

Deploy DKIM in IIS SMTP Service
==================================

**IIS SMTP Server** is a common Windows built-in SMTP service.
**DKIM** is a method for associating a domain name to an email message, 
thereby allowing email sender claims some responsibility for the email. 
In this tutorial, I will introduce how to add DKIM signature to 
outgoing emails in IIS SMTP server.

.. contents:: Sections:
  :local:
  :depth: 1

How DKIM works？
----------------

DKIM combines of a public key cryptography and a DNS to provide credible domain-level 
authentication for email. 

When an email claims to originate from a certain domain, DKIM provides a mechanism by 
which the recipient system can credibly determine that the email did in fact originate 
from a person or system authorized to send email for that domain. 

Therefore, to sign an email with DKIM in IIS SMTP Server, you MUST have a private key/public 
key pair for email signing. The work flow is illustrated as follows: 

.. image:: ../_static/dkim_work_intro.png

Because DKIM signer uses private key to sign the email, recipient system uses public key to 
verify the signature, therefore, if signer doesn't expose the private key to third-party, 
the DKIM signature cannot be faked. 

Install DKIM in IIS SMTP Service
--------------------------------

To enable DKIM signature in IIS SMTP server, you should download the DKIM Installer 
and install it on your machine at first. 

Double click installer file and the installation will be executed automatically. 
Installer requires IIS SMTP server to be installed. If no IIS SMTP Services detected 
in your operation system, Setup will be aborted. 
