# Change Log

## v1.2.8
    * Converted to OpenSecOps supply-chain framework (libraryless variant). This component ships a single CloudFormation template with no Python library dependencies, so the release pipeline emits a deterministic source archive (`git archive HEAD`) + SLSA Build L1 in-toto provenance attesting to it, both Sigstore-signed (`.bundle` files alongside each artefact). The customer-side `scripts/deploy.py` (Installer v3.0.11+) verifies the signatures against the maintainer identity (`peter@peterbengtson.com` via `https://github.com/login/oauth`) before any `cfn deploy`. Adds daily CVE scan and OpenSSF Scorecard workflows (both trivially pass — no library deps to scan). See `SECURITY.md`.

## v1.2.7
    * Enable auto-close workflow for external pull requests, enforcing the cathedral governance policy uniformly across all OpenSecOps repositories. Pull requests from non-team authors are closed automatically with a redirect comment pointing to the bug-report template, the GitHub Security Advisory flow, and the fork-under-MPL-2.0 path.

## v1.2.6
    * Updated GitHub remote references in publish.zsh script to use only OpenSecOps-Org, removed Delegat-AB

## v1.2.5
    * Updated GitHub organization name from CloudSecOps-Org to OpenSecOps-Org.
    * Updated references to CloudSecOps-Installer to Installer.

## v1.2.4
    * File paths corrected for the new name of the installer.

## v1.2.3
    * Updated LICENSE file to MPL 2.0.

## v1.2.2
    * Third time: Updated publish.zsh to support dual-remote publishing to CloudSecOps-Org repositories.

## v1.2.1
    * Again: Updated publish.zsh to support dual-remote publishing to CloudSecOps-Org repositories.

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
      Foundation-limit-log-group-retention section of `CloudSecOps-Installer/apps/foundation/parameters.toml`. 
      See `CloudSecOps-Installer/apps.example/parameters.toml` for an example.

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
