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
    - Default: ssoclient
- region
    - Description: Your AWS region.
    - Type: String
    - Default: us-east-1

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
import aws_ssooidc.aws_ssooidc as sso
response = sso.gettoken('<start_url>')
access_token = response['accessToken']

```

In BASH:

```bash
python3 -c "
    import aws_ssooidc.aws_ssooidc as sso
    response = sso.gettoken('<start_url>')
    access_token = response['accessToken']
"

```

Changelog
---------

2021.1.0.2

- Updated README.

2021.1.0.1

- Added verification URI printout for devices which cannot launch browsers automatically.

2021.1.0.0

- Initial release.

*Current version: 2021.1.0.2*
