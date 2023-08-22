# SOAR-detect-log-buckets

This stack creates an SNS Topic which receives events signalling the successful creation of an account
via AWS Organizations or AWS Control Tower. The topic is intended to be used for post-creation account 
configuration. It can be accessed by any principal.


## Deployment

First log in to your AWS organisation using SSO and a profile that gives you
AWSAdministratorAccess to the AWS Organizations admin account.

```console
aws sso login --profile <profile-name>
```

Then type:

```console
./deploy
```
