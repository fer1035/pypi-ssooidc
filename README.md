**aws_ssooidc**
===============

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
    - Default: 'ssoclient'
- region
    - Description: Your AWS region.
    - Type: String
    - Default: 'us-east-1'
- timeout
    - Description: Number of tries before giving up.
    - Type: Integer
    - Default: 30

Usage
-----

Installation:

```bash
pip3 install aws-ssooidc
# or
python3 -m pip install aws-ssooidc

```

In Python3:

```python
import aws_ssooidc as sso
response = sso.gettoken('<start_url>')

# To get Access Token:
access_token = response['accessToken']

```

In BASH:

```bash
python3 -c "
    import aws_ssooidc as sso
    response = sso.gettoken('<start_url>')

    # To get Access Token:
    access_token = response['accessToken']
"

```

Changelog
---------

2021.1.1.1

- Bugfix: Added type hint to **timeout** parameter in *gettoken*.
- Added feedbacks to *gettoken*.
- Added type and value check to **timeout** parameter.

2021.1.1.0

- Bugfix: Added **region** as keyword in *gettoken* function call.
- Added **timeout** as keyword in *gettoken* function call.
- Added message into JSON cache file error handling.
- Restructured module for easier usage.
- Updated README.

2021.1.0.2

- Updated README.

2021.1.0.1

- Added verification URI printout for devices which cannot launch browsers automatically.

2021.1.0.0

- Initial release.

*Current version: 2021.1.1.1*
