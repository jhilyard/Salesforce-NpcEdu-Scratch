# Sample Salesforce Scratch Orgs

There is a shortage of public directions for how to setup Nonprofit Cloud and Education Cloud scratch org definitions. This project framework is meant to help other people find the patterns quickly.

There are two configurations included in this project (and really nothing else) for creating Salesforce scratch orgs that have the features for Nonprofit Cloud and Education Cloud.

To make use of these configurations you'll need setup SF cli and a Salesforce devhub. Complete [Trailhead Quick Salesforce DX](https://trailhead.salesforce.com/content/learn/projects/quick-start-salesforce-dx) if you don't have those elements in place.

## Nonprofit Cloud

Setup Command:

`sf org create scratch -d -f config/nonprofit-cloud.json -a npc-org`

For details see: `config/nonprofit-cloud.json`

### Features List:

- `AccountingSubledgerGrowthEdition` Subledger is included in this sample. You can remove this from the feature list if you aren't using it for your project.
- `IndustriesActionPlan`
- `AnalyticsQueryService`
- `PublicSectorAccess`
- `Fundraising`
- `Grantmaking` I've included fundraising and grant making. You can remove one if you aren't using it. Please not that Grant making also includes some industry settings that may need to be disabled if this is removed.
- `IndustriesSalesExcellenceAddOn`
- `IndustriesServiceExcellenceAddOn`
- `MarketingUser`
- `ProgramManagement`
- `OmniStudioDesigner`
- `OmniStudioRuntime`
- `EnableSetPasswordInApi`
- `PersonAccounts`

### Industry Settings

The following specific industry settings are included.

- `enableGrantmaking`: true – Grantmaking enablement switch
- `enableBenefitManagementPreference`: true
- `enableBenefitAndGoalSharingPref`: true
- `enableCarePlansPreference`: true

There are three more you can add, but require another feature: `IndustriesCompliantDataSharing`:

- `enableCompliantDataSharingForFundingAward`
- `enableCompliantDataSharingForBudget`
- `enableCompliantDataSharingForIndividualApplication`

## Education Cloud

Setup Command:

`sf org create scratch -d -f config/education-cloud.json -a edu-org`

For Education Cloud the Salesforce help documentation notes that you need to complete the setup manually following the [Education Cloud setup guide](https://help.salesforce.com/s/articleView?id=sfdo.EC_Enable_Education_Cloud.htm&type=5). However, there are a number industry settings that can be pre-set in the configuration to enable and disable these features.

For details see: `config/education-cloud.json`

### Features List:

- `EducationCloud:10` Note that this includes a quantity parameter. I'm unclear why it's needed in this context but appears to be required.
- `Assessments`
- `Fundraising` I've included fundraising in this sample, because you can get Edu Cloud with it. If you aren't using Fundraising in the project you're testing you can remove this one.
- `AccountingSubledgerGrowthEdition` I've included Subledger in this sample, because you can get Edu Cloud with it. If you aren't using Fundraising in the project you're testing you can remove this one.
- `IndustriesActionPlan`
- `AnalyticsQueryService`
- `PublicSectorAccess`
- `IndustriesSalesExcellenceAddOn`
- `IndustriesServiceExcellenceAddOn`
- `LightningScheduler`
- `LightningServiceConsole`
- `MarketingUser`
- `OmniStudioDesigner`
- `OmniStudioRuntime`
- `EnableSetPasswordInApi`
- `PersonAccounts`

### Industry Settings:

- `enableIndustriesAssessment:`: true
- `enableDiscoveryFrameworkMetadata`: true
- `enableEducationCloud`: true
- `enableStudentSuccess`: true
- `enableAcademicOperations`: true
- `enableAlumniRelations`: true
- `enableCarePlansPreference`: true
- `enableBenefitManagementPreference`: true
- `enableBenefitAndGoalSharingPref`: true
