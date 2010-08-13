
===================
What is this?
===================


This is patched version of django-openid-auth (http://pypi.python.org/pypi/django-openid-auth)

========================
Why did I patch it?
========================

As of 2010-08-13, django-openid-auth v0.3 has 2 problems:

 1. Installation throws this error

    BLOB/TEXT column 'claimed_id' used in key specification without a key length

    Fix is simple. But still, manual work.


 2. We use Google Apps for Education as our OpenID provider. Google will provide only user email-id in their response. But django-openid-auth uses nickname while creating Django user accounts and falls back to 'openiduser' if nickname is empty.


    Not good for us. We want to use email id as Django username.


========================
Installation
========================

Read README.txt
