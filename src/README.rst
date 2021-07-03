==============
**AWS-SSOOIDC**
==============

Overview
--------

Create temporary credentials for AWS SSO-OIDC.

Prerequisites
-------------

- *Python >= 3.6*
- *boto3 >= 1.17.78* (installed as a dependency)

Required (Positional) Arguments
-------------------------------

- Position 1: start_url (the start URL for your AWS SSO login)

Optional (Keyword) Arguments
----------------------------

- client_name
    - Description: Arbitrary name of the SSO client to create.
    - Type: String
    - Default: ssoclient
- region
    - Description: Your AWS region.
    - Type: String
    - Default: us-east-1

Usage
-----

Installation:

.. code-block:: BASH

   pip3 install aws-ssooidc
   # or
   python3 -m pip install aws-ssooidc

In Python3:

.. code-block:: BASH

   import aws-ssooidc
   response = aws-ssooidc.gettoken('<start_url>')
   access_token = response['accessToken']

In BASH:

.. code-block:: BASH

   python3 -c "
       import aws-ssooidc;
       response = aws-ssooidc.gettoken('<start_url>');
       access_token = response['accessToken']
   "

Changelog
---------

2021.1.0.0

- Initial release.

*Current version: 2021.1.0.0*
