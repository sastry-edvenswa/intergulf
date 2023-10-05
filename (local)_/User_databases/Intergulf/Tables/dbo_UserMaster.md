#### 

[Project](../../../../index.md) > [(local)\\](../../../index.md) > [User databases](../../index.md) > [Intergulf](../index.md) > [Tables](Tables.md) > dbo.UserMaster

# ![Tables](../../../../Images/Table32.png) [dbo].[UserMaster]

---

## <a name="#properties"></a>Properties

| Property | Value |
|---|---|
| Collation | SQL_Latin1_General_CP1_CI_AS |
| Row Count (~) | 328 |
| Created | 6:47:37 PM Monday, January 29, 2007 |
| Last Modified | 4:31:31 PM Wednesday, September 22, 2021 |


---

## <a name="#columns"></a>Columns

| Key | Name | Data Type | Max Length (Bytes) | Nullability |
|---|---|---|---|---|
| [![Cluster Primary Key PK_UserMaster: UserName](../../../../Images/pkcluster.png)](#indexes) | UserName | varchar(50) | 50 | NOT NULL |
|  | UserPassword | varchar(50) | 50 | NULL allowed |
|  | UserType | varchar(50) | 50 | NULL allowed |
|  | SalesPerson | varchar(2) | 2 | NULL allowed |
|  | FirstName | varchar(50) | 50 | NULL allowed |
|  | LastName | varchar(50) | 50 | NULL allowed |
|  | WebUser | varchar(2) | 2 | NULL allowed |
|  | ProspectReport | varchar(2) | 2 | NULL allowed |
|  | Email | varchar(50) | 50 | NULL allowed |
|  | UpdateDateTime | datetime | 8 | NULL allowed |
|  | UpdateUser | varchar(50) | 50 | NULL allowed |
|  | UpdateComputer | varchar(50) | 50 | NULL allowed |
|  | MaterialCodeReviewer | varchar(2) | 2 | NULL allowed |
|  | Status | varchar(10) | 10 | NULL allowed |
|  | ProfileReviewer | varchar(2) | 2 | NULL allowed |
|  | BackupProfileReviewerUserName | varchar(50) | 50 | NULL allowed |
|  | BackupProfileReviewer | varchar(2) | 2 | NULL allowed |
|  | UseBackupReviewer | varchar(2) | 2 | NULL allowed |
|  | OverrideProfileReviewer | varchar(2) | 2 | NULL allowed |
|  | ProspectEmail | varchar(2) | 2 | NULL allowed |
|  | AllowResourceChanges | varchar(2) | 2 | NULL allowed |
|  | ReceiveProfileOverrideEmail | varchar(2) | 2 | NULL allowed |
|  | ReceiveCustomerStopEmail | varchar(2) | 2 | NULL allowed |
|  | ReceiveCustomerStopOverrideEmail | varchar(2) | 2 | NULL allowed |
|  | ReceiveScheduleOverrideEmail | varchar(2) | 2 | NULL allowed |
|  | ReceiveProspectCWReversalEmail | varchar(2) | 2 | NULL allowed |
|  | AllowScheduleUnlock | varchar(2) | 2 | NULL allowed |
|  | CustomerServiceRep | varchar(2) | 2 | NULL allowed |
|  | SageSalespersonCode | varchar(2) | 2 | NULL allowed |
|  | CSRPersonId | varchar(50) | 50 | NULL allowed |
|  | EManifestUser | varchar(2) | 2 | NULL allowed |


---

## <a name="#indexes"></a>Indexes

| Key | Name | Key Columns | Unique |
|---|---|---|---|
| [![Cluster Primary Key PK_UserMaster: UserName](../../../../Images/pkcluster.png)](#indexes) | PK_UserMaster | UserName | YES |


---

## <a name="#sqlscript"></a>SQL Script

```sql
CREATE TABLE [dbo].[UserMaster]
(
[UserName] [varchar] (50) COLLATE SQL_Latin1_General_CP1_CI_AS NOT NULL,
[UserPassword] [varchar] (50) COLLATE SQL_Latin1_General_CP1_CI_AS NULL,
[UserType] [varchar] (50) COLLATE SQL_Latin1_General_CP1_CI_AS NULL,
[SalesPerson] [varchar] (2) COLLATE SQL_Latin1_General_CP1_CI_AS NULL,
[FirstName] [varchar] (50) COLLATE SQL_Latin1_General_CP1_CI_AS NULL,
[LastName] [varchar] (50) COLLATE SQL_Latin1_General_CP1_CI_AS NULL,
[WebUser] [varchar] (2) COLLATE SQL_Latin1_General_CP1_CI_AS NULL,
[ProspectReport] [varchar] (2) COLLATE SQL_Latin1_General_CP1_CI_AS NULL,
[Email] [varchar] (50) COLLATE SQL_Latin1_General_CP1_CI_AS NULL,
[UpdateDateTime] [datetime] NULL,
[UpdateUser] [varchar] (50) COLLATE SQL_Latin1_General_CP1_CI_AS NULL,
[UpdateComputer] [varchar] (50) COLLATE SQL_Latin1_General_CP1_CI_AS NULL,
[MaterialCodeReviewer] [varchar] (2) COLLATE SQL_Latin1_General_CP1_CI_AS NULL,
[Status] [varchar] (10) COLLATE SQL_Latin1_General_CP1_CI_AS NULL,
[ProfileReviewer] [varchar] (2) COLLATE SQL_Latin1_General_CP1_CI_AS NULL,
[BackupProfileReviewerUserName] [varchar] (50) COLLATE SQL_Latin1_General_CP1_CI_AS NULL,
[BackupProfileReviewer] [varchar] (2) COLLATE SQL_Latin1_General_CP1_CI_AS NULL,
[UseBackupReviewer] [varchar] (2) COLLATE SQL_Latin1_General_CP1_CI_AS NULL,
[OverrideProfileReviewer] [varchar] (2) COLLATE SQL_Latin1_General_CP1_CI_AS NULL,
[ProspectEmail] [varchar] (2) COLLATE SQL_Latin1_General_CP1_CI_AS NULL,
[AllowResourceChanges] [varchar] (2) COLLATE SQL_Latin1_General_CP1_CI_AS NULL,
[ReceiveProfileOverrideEmail] [varchar] (2) COLLATE SQL_Latin1_General_CP1_CI_AS NULL,
[ReceiveCustomerStopEmail] [varchar] (2) COLLATE SQL_Latin1_General_CP1_CI_AS NULL,
[ReceiveCustomerStopOverrideEmail] [varchar] (2) COLLATE SQL_Latin1_General_CP1_CI_AS NULL,
[ReceiveScheduleOverrideEmail] [varchar] (2) COLLATE SQL_Latin1_General_CP1_CI_AS NULL,
[ReceiveProspectCWReversalEmail] [varchar] (2) COLLATE SQL_Latin1_General_CP1_CI_AS NULL,
[AllowScheduleUnlock] [varchar] (2) COLLATE SQL_Latin1_General_CP1_CI_AS NULL,
[CustomerServiceRep] [varchar] (2) COLLATE SQL_Latin1_General_CP1_CI_AS NULL,
[SageSalespersonCode] [varchar] (2) COLLATE SQL_Latin1_General_CP1_CI_AS NULL,
[CSRPersonId] [varchar] (50) COLLATE SQL_Latin1_General_CP1_CI_AS NULL,
[EManifestUser] [varchar] (2) COLLATE SQL_Latin1_General_CP1_CI_AS NULL
) ON [PRIMARY]
GO
ALTER TABLE [dbo].[UserMaster] ADD CONSTRAINT [PK_UserMaster] PRIMARY KEY CLUSTERED ([UserName]) ON [PRIMARY]
GO

```


---

## <a name="#usedby"></a>Used By

* [[dbo].[vwExportLoadLabVolume]](../Views/dbo_vwExportLoadLabVolume.md)
* [[dbo].[vwExportLoadVolume]](../Views/dbo_vwExportLoadVolume.md)
* [[dbo].[vwInventoryContracts]](../Views/dbo_vwInventoryContracts.md)
* [[dbo].[vwProfilesActiveNoMSDS]](../Views/dbo_vwProfilesActiveNoMSDS.md)
* [[dbo].[vwRptLabTestForm]](../Views/dbo_vwRptLabTestForm.md)
* [[dbo].[vwRptLabTestSampleForm]](../Views/dbo_vwRptLabTestSampleForm.md)
* [[dbo].[vwRptLoadAccounting]](../Views/dbo_vwRptLoadAccounting.md)
* [[dbo].[vwRptLoadBillingAccounting]](../Views/dbo_vwRptLoadBillingAccounting.md)
* [[dbo].[vwRptLoadBillingAccountingNew]](../Views/dbo_vwRptLoadBillingAccountingNew.md)
* [[dbo].[vwRptLoadBOL]](../Views/dbo_vwRptLoadBOL.md)
* [[dbo].[vwRptLoadInternalTruck]](../Views/dbo_vwRptLoadInternalTruck.md)
* [[dbo].[vwRptLoadInternalTruckNew]](../Views/dbo_vwRptLoadInternalTruckNew.md)
* [[dbo].[vwRptLoadManifest]](../Views/dbo_vwRptLoadManifest.md)
* [[dbo].[vwRptLoadRequest]](../Views/dbo_vwRptLoadRequest.md)
* [[dbo].[vwRptLoadTCEQ]](../Views/dbo_vwRptLoadTCEQ.md)
* [[dbo].[vwRptProfileForm]](../Views/dbo_vwRptProfileForm.md)
* [[dbo].[vwRptProfileFormProduct]](../Views/dbo_vwRptProfileFormProduct.md)
* [[dbo].[vwRptProfileInactive]](../Views/dbo_vwRptProfileInactive.md)
* [[dbo].[vwRptProfileReCertification]](../Views/dbo_vwRptProfileReCertification.md)
* [[dbo].[vwRptProspectAllOpportunities]](../Views/dbo_vwRptProspectAllOpportunities.md)
* [[dbo].[vwRptProspectByName]](../Views/dbo_vwRptProspectByName.md)
* [[dbo].[vwRptProspectContactByName]](../Views/dbo_vwRptProspectContactByName.md)
* [[dbo].[vwRptTankTurnLabTest]](../Views/dbo_vwRptTankTurnLabTest.md)
* [[dbo].[vwSelectCustomerStopInformation]](../Views/dbo_vwSelectCustomerStopInformation.md)
* [[dbo].[vwSelectCustomerStopInformationLoadRequest]](../Views/dbo_vwSelectCustomerStopInformationLoadRequest.md)
* [[dbo].[vwSelectEManifest]](../Views/dbo_vwSelectEManifest.md)
* [[dbo].[vwSelectExportLoadLabVolume]](../Views/dbo_vwSelectExportLoadLabVolume.md)
* [[dbo].[vwSelectExportProfilesApprovalDays]](../Views/dbo_vwSelectExportProfilesApprovalDays.md)
* [[dbo].[vwSelectExportToSage]](../Views/dbo_vwSelectExportToSage.md)
* [[dbo].[vwSelectExportToSageAccrual]](../Views/dbo_vwSelectExportToSageAccrual.md)
* [[dbo].[vwSelectExportToSageTest]](../Views/dbo_vwSelectExportToSageTest.md)
* [[dbo].[vwSelectInventoryFixedCostContracts]](../Views/dbo_vwSelectInventoryFixedCostContracts.md)
* [[dbo].[vwSelectInventoryRailCarContracts]](../Views/dbo_vwSelectInventoryRailCarContracts.md)
* [[dbo].[vwSelectLabTest]](../Views/dbo_vwSelectLabTest.md)
* [[dbo].[vwSelectLabTestSample]](../Views/dbo_vwSelectLabTestSample.md)
* [[dbo].[vwSelectLoadProfileMaterialCode]](../Views/dbo_vwSelectLoadProfileMaterialCode.md)
* [[dbo].[vwSelectLoadRequestProfileMaterialCode]](../Views/dbo_vwSelectLoadRequestProfileMaterialCode.md)
* [[dbo].[vwSelectLoadsByProfileCreateDate]](../Views/dbo_vwSelectLoadsByProfileCreateDate.md)
* [[dbo].[vwSelectLoadsReadyForAccountingNew]](../Views/dbo_vwSelectLoadsReadyForAccountingNew.md)
* [[dbo].[vwSelectProfileForSales]](../Views/dbo_vwSelectProfileForSales.md)
* [[dbo].[vwSelectProfileReviewForMarc]](../Views/dbo_vwSelectProfileReviewForMarc.md)
* [[dbo].[vwSelectProfileReviewUsers]](../Views/dbo_vwSelectProfileReviewUsers.md)
* [[dbo].[vwSelectProfilesInReviewNextReviewUser]](../Views/dbo_vwSelectProfilesInReviewNextReviewUser.md)
* [[dbo].[vwSelectProfilesInReviewNextUser]](../Views/dbo_vwSelectProfilesInReviewNextUser.md)
* [[dbo].[vwSelectProspectActivity]](../Views/dbo_vwSelectProspectActivity.md)
* [[dbo].[vwSelectProspectContact]](../Views/dbo_vwSelectProspectContact.md)
* [[dbo].[vwSelectProspectLabTestSample]](../Views/dbo_vwSelectProspectLabTestSample.md)
* [[dbo].[vwSelectProspectOpportunity]](../Views/dbo_vwSelectProspectOpportunity.md)
* [[dbo].[vwSelectProspectOpportunityForDavid]](../Views/dbo_vwSelectProspectOpportunityForDavid.md)
* [[dbo].[vwSelectProspects]](../Views/dbo_vwSelectProspects.md)
* [[dbo].[vwSelectRequestedLoads]](../Views/dbo_vwSelectRequestedLoads.md)
* [[dbo].[vwSelectUserMaster]](../Views/dbo_vwSelectUserMaster.md)
* [[dbo].[fnSelectOneLabTest]](../Programmability/Functions/Table-valued_Functions/dbo_fnSelectOneLabTest.md)
* [[dbo].[fnSelectUserMaster]](../Programmability/Functions/Table-valued_Functions/dbo_fnSelectUserMaster.md)
* [[dbo].[fnSelectUserMasterActive]](../Programmability/Functions/Table-valued_Functions/dbo_fnSelectUserMasterActive.md)


---

###### Author:  Sastry

###### Copyright 2023 - All Rights Reserved

###### Created: Thursday, October 5, 2023 9:55:17 PM

