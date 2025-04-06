# Change Log

## v1.1.4
    * Updated publish.zsh to support dual-remote publishing to CloudSecOps-Org repositories.

## v1.1.3
    * Removed superfluous condition.

## v1.1.2
    * AWS Chatbot policy clause now uses wildcard matching instead of assuming the service role always exists.

## v1.1.1
    * Updated comment regarding scope.

## v1.1.0
    * Restricted the SNS topic for the use of the Org account only, as well as for AWS ChatBot.
      Before deploying, add the line `OrgAccountId     = '{admin-account}'` to the 
      Foundation-limit-log-group-retention section of `Delegat-Install/apps/foundation/parameters.toml`. 
      See `Delegat-Install/apps.example/parameters.toml` for an example.

## v1.0.5
    * Upgraded to Python 3.12.
    * Added `.python-version` file for pyenv.

## v1.0.4
  * Refreshed deployment scripts.

## v1.0.3
    * Open-source credits and URLs
    * Fixed installer initial stackset creation.

## v1.0.2
    * `--dry-run` and `--verbose` added to `deploy`.

## v1.0.1
  * Role bug fixed.

## v1.0.0
  * First release.
