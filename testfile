[[_TOC_]]

This procedure describes process for release of projects in DCC - DCP, Web Shop and PMS.

# Roles
- Release manager
- Project manager
- DCP developer
- Web Shop developer
- PMS developer
- QA engineer
- DevOps engineer

# Projects
Projects that are included in release.

## DCP
Components:
- email-templates
- svc-utility
- svc-notification
- svc-fraud-detection
- svc-content
- svc-payment-adyen
- svc-payment
- svc-voucher
- svc-product
- svc-shop
- svc-edge

## Web Shop
Components:
- i18n
- provider-logos
- product-texts
- webshop

## PMS
Components:
- pms

# Steps
## Define release scope
Release Manager, Project Manager and Development lists every component for every project that needs to be released.

## Log Release Task
Release Manager creates Release Task for each of the projects and for particular versions that is going to be released.

Release Manager publishes Release Task to `#release - ICP Slack` channel.

Release Tasks serves as central point of communication between PM,  Development, QA and DevOps teams about release.
 
It should list details about release scope, QA validation, any change of component configuration, deployment details, etc.

It should be assigned to all persons that participates in the release.

Link to Release Task template is [here](https://peak.myjetbrains.com/youtrack/newIssue?project=ICPDCP&description=%23%23%23%20Release%20version%0A%0A%3E%20What%20project%20version%20should%20be%20released.%0A%0A%0A%23%23%23%20Release%20components%0A%0A%3E%20List%20all%20components%20that%20should%20be%20released.%0A%0A%0A%23%23%23%20QA%20report%0A%0A%3E%20Attach%20QA%20report%20for%20this%20release.%0A%0A%0A%23%23%23%20Configuration%20update%0A%0A%3E%20List%20all%20configuration%20changes%20for%20all%20components.%0A%0A%0A%23%23%23%20Deployment%20details%0A%0A%3E%20List%20all%20deployment%20details,%20notes,%20warnings,%20etc.&c=visible%20to%20ICP-DCP%20Team&c=Type%20Task&draftId=2-601).

## Validate Development environment
QA publishes validation start to `#release - ICP Slack` channel

> Code on Development environment must not be updated during validation.

QA validates Development environment by executing automated and manual test cases. Attach QA report to Release Task after successful validation.

QA publishes validation result to `#release - ICP Slack` channel

## Create Production branches
Release Manager creates production branches for all components that are being released.

Release Manager publishes creation of branches to `#release - ICP Slack` channel.

> Branch names should be in form `production-v0.0`.

## Deploy Staging environment
DevOps asks for Staging upgrade timeframe from `#release - Digital Reload Slack` channel.

DevOps publishes agreed timeframe to `#release - ICP Slack` channel.

DevOps publishes start of Staging upgrade to `#release - ICP Slack` channel.

DevOps upgrades Staging environment. While upgrade is in progress, QA executes test cases in order to find problems that user can encounter in production upgrade.

DevOps publishes end of Staging upgrade to `#release - ICP Slack` channel.

> Web Shop and PMS components should be deployed ***after*** all other components.

## Validate Staging environment
QA publishes Staging validation start to `#release - ICP Slack` channel

QA validates Staging environment by executing Staging specific test cases and procedures.

QA publishes Staging validation result to `#release - ICP Slack` channel.

DevOps publishes end of Staging upgrade to `#release - Digital Reload Slack` channel.

## Create Production tags
Release Manager creates tags for all components that are being released.

Release Manager publishes creation of tags to `#release - ICP Slack` channel.

> Tag names should be in form `v0.0`.

## Deploy Production environment
DevOps asks for Production upgrade timeframe from `#release - Digital Reload Slack` channel.

DevOps publishes agreed timeframe to `#release - ICP Slack` channel.

DevOps publishes start of Production upgrade to `#release - ICP Slack` channel.

DevOps upgrades Production environment.

DevOps publishes end of Production upgrade to `#release - ICP Slack` channel.

> Web Shop and PMS components should be deployed ***after*** all other components.

## Validate Production environment
QA publishes Production validation start to `#release - ICP Slack` channel

QA validates Production environment by executing Production specific test cases and procedures.

QA publishes Production validation result to `#release - ICP Slack` channel.

DevOps publishes end of Production upgrade to `#release - Digital Reload Slack` channel.

## Send release notes
Project Manager sends release notes `release@peaksoftware.be`
