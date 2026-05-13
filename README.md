# Foundation-new-account-created-sns-topic

[![Daily CVE scan](https://github.com/OpenSecOps-Org/Foundation-new-account-created-sns-topic/actions/workflows/daily-scan.yml/badge.svg)](https://github.com/OpenSecOps-Org/Foundation-new-account-created-sns-topic/actions/workflows/daily-scan.yml) [![OpenSSF Scorecard](https://github.com/OpenSecOps-Org/Foundation-new-account-created-sns-topic/actions/workflows/scorecard.yml/badge.svg)](https://github.com/OpenSecOps-Org/Foundation-new-account-created-sns-topic/actions/workflows/scorecard.yml) [![OpenSSF Best Practices](https://www.bestpractices.dev/projects/12827/badge)](https://www.bestpractices.dev/projects/12827)

This stack creates an SNS Topic which receives events signalling the successful creation of an account
via AWS Organizations or AWS Control Tower. The topic is intended to be used for post-creation account 
configuration. It can be accessed by any principal.


## Deployment

First make sure that your SSO setup is configured with a default profile giving you AWSAdministratorAccess
to your AWS Organizations administrative account. This is necessary as the AWS cross-account role used 
during deployment only can be assumed from that account.

```console
aws sso login
```

Then type:

```console
./deploy
```
