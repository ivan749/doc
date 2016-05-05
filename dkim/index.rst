.. DKIM Plugin documentation master file, created by
   sphinx-quickstart on Thu May  5 11:35:26 2016.
   You can adapt this file completely to your liking, but it should at least
   contain the root `toctree` directive.

DKIM for Exchange Server and IIS SMTP Service documentation
============================================================

Platform: Windows 2000 or later version (Windows x86/x64)
with Exchange Server 2000/2003/2007/2013/2016 or IIS SMTP Service installed

.. attention:: Exchange 2007 requires SP1 rollup 9 or SP2 installed.

With this tool, your Exchange Server or IIS SMTP Service will be enabled to add DomainKeys 
and DKIM signature to outgoing emails from specified domain(s), which verify the DNS domain of 
an email sender and the message integrity, and in turn preventing the emails from your domain from 
being flagged as spam or junk mail by email servers which have Domainkeys/DKIM implemented 
(such as Hotmail, Yahoo mail and Gmail).

Topics
------
.. toctree::
   :maxdepth: 2
   
   tutorials/index

Indices and tables
==================

* :ref:`genindex`
* :ref:`search`

