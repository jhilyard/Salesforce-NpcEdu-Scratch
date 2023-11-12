# Sample Salesforce Scratch Orgs

There is a shortage of public directions for how to setup Nonprofit Cloud and Education Cloud scratch org definitions. This project framework is meant to help other people find the patterns quickly.

There are two configurations included in this project (and really nothing else) for creating Salesforce scratch orgs that have the features for Nonprofit Cloud and Education Cloud.

To make use of these configurations you'll need setup SF cli and a Salesforce devhub. Complete [Trailhead Quick Salesforce DX](https://trailhead.salesforce.com/content/learn/projects/quick-start-salesforce-dx) if you don't have those elements in place.

## Nonprofit Cloud

Setup Command:

`sf org create scratch -d -f config/project-scratch-def.json -a npc-org`

For details see: `config/nonprofit-cloud.json`

Features List:

```
  "features": [
    "AccountingSubledgerGrowthEdition",
    "IndustriesActionPlan",
    "AnalyticsQueryService",
    "PublicSectorAccess",
    "Fundraising",
    "Grantmaking",
    "IndustriesSalesExcellenceAddOn",
    "IndustriesServiceExcellenceAddOn",
    "MarketingUser",
    "ProgramManagement",
    "OmniStudioDesigner",
    "OmniStudioRuntime",
    "EnableSetPasswordInApi",
    "PersonAccounts"
  ],
```

## Education Cloud

Setup Command:

`sf org create scratch -d -f config/education-cloud.json -a edu-org`

For details see: `config/education-cloud.json`

Features List:

```
"features": [
    "EducationCloud:10",
    "Assessments",
    "Fundraising",
    "AccountingSubledgerGrowthEdition",
    "IndustriesActionPlan",
    "AnalyticsQueryService",
    "PublicSectorAccess",
    "IndustriesSalesExcellenceAddOn",
    "IndustriesServiceExcellenceAddOn",
    "LightningScheduler",
    "LightningServiceConsole",
    "MarketingUser",
    "OmniStudioDesigner",
    "OmniStudioRuntime",
    "EnableSetPasswordInApi",
    "PersonAccounts"
  ],
```
