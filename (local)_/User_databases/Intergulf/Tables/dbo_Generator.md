#### 

[Project](../../../../index.md) > [(local)\\](../../../index.md) > [User databases](../../index.md) > [Intergulf](../index.md) > [Tables](Tables.md) > dbo.Generator

# ![Tables](../../../../Images/Table32.png) [dbo].[Generator]

---

## <a name="#properties"></a>Properties

| Property | Value |
|---|---|
| Collation | SQL_Latin1_General_CP1_CI_AS |
| Row Count (~) | 6942 |
| Created | 6:47:33 PM Monday, January 29, 2007 |
| Last Modified | 11:44:41 AM Tuesday, August 28, 2018 |


---

## <a name="#columns"></a>Columns

| Key | Name | Data Type | Max Length (Bytes) | Nullability | Identity |
|---|---|---|---|---|---|
| [![Cluster Primary Key PK_Generator: Id](../../../../Images/pkcluster.png)](#indexes)[![Indexes hind_2105058535_1A_2A, _dta_stat_2105058535_1_2_15, hind_2105058535_2A_1A](../../../../Images/Index.png)](#indexes)(3) | Id | numeric(18,0) | 9 | NOT NULL | 1 - 1 |
| [![Indexes hind_2105058535_1A_2A, _dta_stat_2105058535_1_2_15, _dta_stat_2105058535_2_15, hind_2105058535_2A_1A](../../../../Images/Index.png)](#indexes)(4) | Name | varchar(100) | 100 | NULL allowed |  |
|  | Address | varchar(3000) | 3000 | NULL allowed |  |
|  | City | varchar(50) | 50 | NULL allowed |  |
|  | State | varchar(50) | 50 | NULL allowed |  |
|  | Zip | varchar(50) | 50 | NULL allowed |  |
|  | BillingName | varchar(100) | 100 | NULL allowed |  |
|  | BillingAddress | varchar(3000) | 3000 | NULL allowed |  |
|  | BillingCity | varchar(50) | 50 | NULL allowed |  |
|  | BillingState | varchar(50) | 50 | NULL allowed |  |
|  | BillingZip | varchar(50) | 50 | NULL allowed |  |
|  | Contact | varchar(50) | 50 | NULL allowed |  |
|  | Phone | varchar(50) | 50 | NULL allowed |  |
|  | Fax | varchar(50) | 50 | NULL allowed |  |
| [![Indexes _dta_stat_2105058535_1_2_15, _dta_stat_2105058535_2_15](../../../../Images/Index.png)](#indexes)(2) | Email | varchar(50) | 50 | NULL allowed |  |
|  | RegistrationNo | varchar(50) | 50 | NULL allowed |  |
|  | EpaIdNo | varchar(50) | 50 | NULL allowed |  |
|  | Type | varchar(50) | 50 | NULL allowed |  |
|  | Classification | varchar(50) | 50 | NULL allowed |  |
|  | UpdateDateTime | datetime | 8 | NULL allowed |  |
|  | UpdateUser | varchar(50) | 50 | NULL allowed |  |
|  | UpdateComputer | varchar(50) | 50 | NULL allowed |  |
|  | MaxTCPeriod | varchar(50) | 50 | NULL allowed |  |
|  | MaxTCCount | numeric(18,0) | 9 | NULL allowed |  |
|  | MinTCPeriod | varchar(50) | 50 | NULL allowed |  |
|  | MinTCCount | numeric(18,0) | 9 | NULL allowed |  |
|  | Facility | varchar(50) | 50 | NULL allowed |  |
|  | CompanyId | varchar(25) | 25 | NULL allowed |  |


---

## <a name="#indexes"></a>Indexes

| Key | Name | Key Columns | Unique |
|---|---|---|---|
| [![Cluster Primary Key PK_Generator: Id](../../../../Images/pkcluster.png)](#indexes) | PK_Generator | Id | YES |


---

## <a name="#statistics"></a>Statistics

| Name | Key Columns |
|---|---|
| _dta_stat_2105058535_1_2_15 | Id, Name, Email |
| _dta_stat_2105058535_2_15 | Name, Email |
| hind_2105058535_1A_2A | Id, Name |
| hind_2105058535_2A_1A | Name, Id |


---

## <a name="#sqlscript"></a>SQL Script

```sql
CREATE TABLE [dbo].[Generator]
(
[Id] [numeric] (18, 0) NOT NULL IDENTITY(1, 1),
[Name] [varchar] (100) COLLATE SQL_Latin1_General_CP1_CI_AS NULL,
[Address] [varchar] (3000) COLLATE SQL_Latin1_General_CP1_CI_AS NULL,
[City] [varchar] (50) COLLATE SQL_Latin1_General_CP1_CI_AS NULL,
[State] [varchar] (50) COLLATE SQL_Latin1_General_CP1_CI_AS NULL,
[Zip] [varchar] (50) COLLATE SQL_Latin1_General_CP1_CI_AS NULL,
[BillingName] [varchar] (100) COLLATE SQL_Latin1_General_CP1_CI_AS NULL,
[BillingAddress] [varchar] (3000) COLLATE SQL_Latin1_General_CP1_CI_AS NULL,
[BillingCity] [varchar] (50) COLLATE SQL_Latin1_General_CP1_CI_AS NULL,
[BillingState] [varchar] (50) COLLATE SQL_Latin1_General_CP1_CI_AS NULL,
[BillingZip] [varchar] (50) COLLATE SQL_Latin1_General_CP1_CI_AS NULL,
[Contact] [varchar] (50) COLLATE SQL_Latin1_General_CP1_CI_AS NULL,
[Phone] [varchar] (50) COLLATE SQL_Latin1_General_CP1_CI_AS NULL,
[Fax] [varchar] (50) COLLATE SQL_Latin1_General_CP1_CI_AS NULL,
[Email] [varchar] (50) COLLATE SQL_Latin1_General_CP1_CI_AS NULL,
[RegistrationNo] [varchar] (50) COLLATE SQL_Latin1_General_CP1_CI_AS NULL,
[EpaIdNo] [varchar] (50) COLLATE SQL_Latin1_General_CP1_CI_AS NULL,
[Type] [varchar] (50) COLLATE SQL_Latin1_General_CP1_CI_AS NULL,
[Classification] [varchar] (50) COLLATE SQL_Latin1_General_CP1_CI_AS NULL,
[UpdateDateTime] [datetime] NULL,
[UpdateUser] [varchar] (50) COLLATE SQL_Latin1_General_CP1_CI_AS NULL,
[UpdateComputer] [varchar] (50) COLLATE SQL_Latin1_General_CP1_CI_AS NULL,
[MaxTCPeriod] [varchar] (50) COLLATE SQL_Latin1_General_CP1_CI_AS NULL,
[MaxTCCount] [numeric] (18, 0) NULL,
[MinTCPeriod] [varchar] (50) COLLATE SQL_Latin1_General_CP1_CI_AS NULL,
[MinTCCount] [numeric] (18, 0) NULL,
[Facility] [varchar] (50) COLLATE SQL_Latin1_General_CP1_CI_AS NULL,
[CompanyId] [varchar] (25) COLLATE SQL_Latin1_General_CP1_CI_AS NULL
) ON [PRIMARY]
GO
ALTER TABLE [dbo].[Generator] ADD CONSTRAINT [PK_Generator] PRIMARY KEY CLUSTERED ([Id]) ON [PRIMARY]
GO
CREATE STATISTICS [hind_2105058535_1A_2A] ON [dbo].[Generator] ([Id], [Name])
GO
CREATE STATISTICS [_dta_stat_2105058535_1_2_15] ON [dbo].[Generator] ([Id], [Name], [Email])
GO
CREATE STATISTICS [_dta_stat_2105058535_2_15] ON [dbo].[Generator] ([Name], [Email])
GO
CREATE STATISTICS [hind_2105058535_2A_1A] ON [dbo].[Generator] ([Name], [Id])
GO

```


---

## <a name="#usedby"></a>Used By

* [[dbo].[vwChooseProfile]](../Views/dbo_vwChooseProfile.md)
* [[dbo].[vwCustomerGeneratorProfileReport]](../Views/dbo_vwCustomerGeneratorProfileReport.md)
* [[dbo].[vwCustomerGeneratorSort]](../Views/dbo_vwCustomerGeneratorSort.md)
* [[dbo].[vwExportLoadLabVolume]](../Views/dbo_vwExportLoadLabVolume.md)
* [[dbo].[vwExportLoadVolume]](../Views/dbo_vwExportLoadVolume.md)
* [[dbo].[vwGeneratorProfileSort]](../Views/dbo_vwGeneratorProfileSort.md)
* [[dbo].[vwProfilesActiveNoMSDS]](../Views/dbo_vwProfilesActiveNoMSDS.md)
* [[dbo].[vwRptLabTestForm]](../Views/dbo_vwRptLabTestForm.md)
* [[dbo].[vwRptLoadBillingAccounting]](../Views/dbo_vwRptLoadBillingAccounting.md)
* [[dbo].[vwRptLoadBillingAccountingNew]](../Views/dbo_vwRptLoadBillingAccountingNew.md)
* [[dbo].[vwRptLoadBillingDetail]](../Views/dbo_vwRptLoadBillingDetail.md)
* [[dbo].[vwRptLoadBOL]](../Views/dbo_vwRptLoadBOL.md)
* [[dbo].[vwRptLoadDriverTimeLog]](../Views/dbo_vwRptLoadDriverTimeLog.md)
* [[dbo].[vwRptLoadInternalTruck]](../Views/dbo_vwRptLoadInternalTruck.md)
* [[dbo].[vwRptLoadInternalTruckNew]](../Views/dbo_vwRptLoadInternalTruckNew.md)
* [[dbo].[vwRptLoadInventoryDetails]](../Views/dbo_vwRptLoadInventoryDetails.md)
* [[dbo].[vwRptLoadLabPadTimes]](../Views/dbo_vwRptLoadLabPadTimes.md)
* [[dbo].[vwRptLoadManifest]](../Views/dbo_vwRptLoadManifest.md)
* [[dbo].[vwRptLoadMaterialDestination]](../Views/dbo_vwRptLoadMaterialDestination.md)
* [[dbo].[vwRptLoadMaterialGenerator]](../Views/dbo_vwRptLoadMaterialGenerator.md)
* [[dbo].[vwRptLoadMaterialGeneratorKStarks]](../Views/dbo_vwRptLoadMaterialGeneratorKStarks.md)
* [[dbo].[vwRptLoadMaterialGeneratorKStarksProfileNo]](../Views/dbo_vwRptLoadMaterialGeneratorKStarksProfileNo.md)
* [[dbo].[vwRptLoadRequest]](../Views/dbo_vwRptLoadRequest.md)
* [[dbo].[vwRptLoadSchedule]](../Views/dbo_vwRptLoadSchedule.md)
* [[dbo].[vwRptLoadScheduleByPump]](../Views/dbo_vwRptLoadScheduleByPump.md)
* [[dbo].[vwRptLoadScheduleNew]](../Views/dbo_vwRptLoadScheduleNew.md)
* [[dbo].[vwRptLoadsTrailerStorage]](../Views/dbo_vwRptLoadsTrailerStorage.md)
* [[dbo].[vwRptLoadTCEQ]](../Views/dbo_vwRptLoadTCEQ.md)
* [[dbo].[vwRptProfileBol]](../Views/dbo_vwRptProfileBol.md)
* [[dbo].[vwRptProfileForm]](../Views/dbo_vwRptProfileForm.md)
* [[dbo].[vwRptProfileFormProduct]](../Views/dbo_vwRptProfileFormProduct.md)
* [[dbo].[vwRptProfileManifest]](../Views/dbo_vwRptProfileManifest.md)
* [[dbo].[vwRptProfileTCEQ]](../Views/dbo_vwRptProfileTCEQ.md)
* [[dbo].[vwRptSelectSchedulePumpTimes]](../Views/dbo_vwRptSelectSchedulePumpTimes.md)
* [[dbo].[vwRptSelectScheduleTimes]](../Views/dbo_vwRptSelectScheduleTimes.md)
* [[dbo].[vwRptWasteLoads]](../Views/dbo_vwRptWasteLoads.md)
* [[dbo].[vwSelectAvailableForScheduledLoadsAll]](../Views/dbo_vwSelectAvailableForScheduledLoadsAll.md)
* [[dbo].[vwSelectAvailableForScheduledLoadsPending]](../Views/dbo_vwSelectAvailableForScheduledLoadsPending.md)
* [[dbo].[vwSelectAvailableForScheduledLoadsScheduled]](../Views/dbo_vwSelectAvailableForScheduledLoadsScheduled.md)
* [[dbo].[vwSelectEManifest]](../Views/dbo_vwSelectEManifest.md)
* [[dbo].[vwSelectEmergencyContactNumber]](../Views/dbo_vwSelectEmergencyContactNumber.md)
* [[dbo].[vwSelectExportBayportTimes]](../Views/dbo_vwSelectExportBayportTimes.md)
* [[dbo].[vwSelectExportIntergulfDriversOnSiteTime]](../Views/dbo_vwSelectExportIntergulfDriversOnSiteTime.md)
* [[dbo].[vwSelectExportLoadLabVolume]](../Views/dbo_vwSelectExportLoadLabVolume.md)
* [[dbo].[vwSelectExportLoadLabVolumeNew]](../Views/dbo_vwSelectExportLoadLabVolumeNew.md)
* [[dbo].[vwSelectExportLoadsForEBE]](../Views/dbo_vwSelectExportLoadsForEBE.md)
* [[dbo].[vwSelectExportLoadsForEBETemp]](../Views/dbo_vwSelectExportLoadsForEBETemp.md)
* [[dbo].[vwSelectExportLoadsForSchedule]](../Views/dbo_vwSelectExportLoadsForSchedule.md)
* [[dbo].[vwSelectExportLoadsForSteers]](../Views/dbo_vwSelectExportLoadsForSteers.md)
* [[dbo].[vwSelectExportProfileNewBusiness]](../Views/dbo_vwSelectExportProfileNewBusiness.md)
* [[dbo].[vwSelectExportProfiles]](../Views/dbo_vwSelectExportProfiles.md)
* [[dbo].[vwSelectExportProfilesApprovalDays]](../Views/dbo_vwSelectExportProfilesApprovalDays.md)
* [[dbo].[vwSelectExportProfilesNew]](../Views/dbo_vwSelectExportProfilesNew.md)
* [[dbo].[vwSelectExportProfileVolume]](../Views/dbo_vwSelectExportProfileVolume.md)
* [[dbo].[vwSelectExportStrangTimes]](../Views/dbo_vwSelectExportStrangTimes.md)
* [[dbo].[vwSelectExportToSage]](../Views/dbo_vwSelectExportToSage.md)
* [[dbo].[vwSelectExportToSageAccrual]](../Views/dbo_vwSelectExportToSageAccrual.md)
* [[dbo].[vwSelectExportToSageTest]](../Views/dbo_vwSelectExportToSageTest.md)
* [[dbo].[vwSelectGeneratorForSaturn]](../Views/dbo_vwSelectGeneratorForSaturn.md)
* [[dbo].[vwSelectGeneratorProfilePricing]](../Views/dbo_vwSelectGeneratorProfilePricing.md)
* [[dbo].[vwSelectLabTest]](../Views/dbo_vwSelectLabTest.md)
* [[dbo].[vwSelectLoadForSchedule]](../Views/dbo_vwSelectLoadForSchedule.md)
* [[dbo].[vwSelectLoadPadTimesForExport]](../Views/dbo_vwSelectLoadPadTimesForExport.md)
* [[dbo].[vwSelectLoadRequest]](../Views/dbo_vwSelectLoadRequest.md)
* [[dbo].[vwSelectLoadRequestForOverage]](../Views/dbo_vwSelectLoadRequestForOverage.md)
* [[dbo].[vwSelectLoadRequestForSchedule]](../Views/dbo_vwSelectLoadRequestForSchedule.md)
* [[dbo].[vwSelectLoadRequestsLeadTimes]](../Views/dbo_vwSelectLoadRequestsLeadTimes.md)
* [[dbo].[vwSelectLoads]](../Views/dbo_vwSelectLoads.md)
* [[dbo].[vwSelectLoads4thQtrBayportLoadTimes]](../Views/dbo_vwSelectLoads4thQtrBayportLoadTimes.md)
* [[dbo].[vwSelectLoadsByProfileCreateDate]](../Views/dbo_vwSelectLoadsByProfileCreateDate.md)
* [[dbo].[vwSelectLoadsCount]](../Views/dbo_vwSelectLoadsCount.md)
* [[dbo].[vwSelectLoadsFor225ByMonth]](../Views/dbo_vwSelectLoadsFor225ByMonth.md)
* [[dbo].[vwSelectLoadsForBayportCWaste]](../Views/dbo_vwSelectLoadsForBayportCWaste.md)
* [[dbo].[vwSelectLoadsForBayportTurnTimes]](../Views/dbo_vwSelectLoadsForBayportTurnTimes.md)
* [[dbo].[vwSelectLoadsForSaturn]](../Views/dbo_vwSelectLoadsForSaturn.md)
* [[dbo].[vwSelectLoadsInactive]](../Views/dbo_vwSelectLoadsInactive.md)
* [[dbo].[vwSelectLoadsMotiva20121001]](../Views/dbo_vwSelectLoadsMotiva20121001.md)
* [[dbo].[vwSelectLoadsScheduledForChart]](../Views/dbo_vwSelectLoadsScheduledForChart.md)
* [[dbo].[vwSelectLoadsScheduleForExport]](../Views/dbo_vwSelectLoadsScheduleForExport.md)
* [[dbo].[vwSelectMonthlyDischarge]](../Views/dbo_vwSelectMonthlyDischarge.md)
* [[dbo].[vwSelectPendingLoads]](../Views/dbo_vwSelectPendingLoads.md)
* [[dbo].[vwSelectProfileActiveLastLoadDate]](../Views/dbo_vwSelectProfileActiveLastLoadDate.md)
* [[dbo].[vwSelectProfileActiveLastLoadDateNew]](../Views/dbo_vwSelectProfileActiveLastLoadDateNew.md)
* [[dbo].[vwSelectProfileBlinds]](../Views/dbo_vwSelectProfileBlinds.md)
* [[dbo].[vwSelectProfileBlindsBothSides]](../Views/dbo_vwSelectProfileBlindsBothSides.md)
* [[dbo].[vwSelectProfileFixExpirationDate]](../Views/dbo_vwSelectProfileFixExpirationDate.md)
* [[dbo].[vwSelectProfileForSales]](../Views/dbo_vwSelectProfileForSales.md)
* [[dbo].[vwSelectProfileInformation]](../Views/dbo_vwSelectProfileInformation.md)
* [[dbo].[vwSelectProfilePrePrint]](../Views/dbo_vwSelectProfilePrePrint.md)
* [[dbo].[vwSelectProfileReviewForMarc]](../Views/dbo_vwSelectProfileReviewForMarc.md)
* [[dbo].[vwSelectProfilesInactive]](../Views/dbo_vwSelectProfilesInactive.md)
* [[dbo].[vwSelectProfilesInReviewNextReviewUser]](../Views/dbo_vwSelectProfilesInReviewNextReviewUser.md)
* [[dbo].[vwSelectProfilesInReviewNextUser]](../Views/dbo_vwSelectProfilesInReviewNextUser.md)
* [[dbo].[vwSelectProfileVolumeTest]](../Views/dbo_vwSelectProfileVolumeTest.md)
* [[dbo].[vwSelectRequestedLoads]](../Views/dbo_vwSelectRequestedLoads.md)
* [[dbo].[vwSelectScheduledLoads]](../Views/dbo_vwSelectScheduledLoads.md)
* [[dbo].[vwSelectTrailerLastLoad]](../Views/dbo_vwSelectTrailerLastLoad.md)
* [[dbo].[vwSelectTrailerScheduledLoads]](../Views/dbo_vwSelectTrailerScheduledLoads.md)
* [[dbo].[fnSelectGenerator]](../Programmability/Functions/Table-valued_Functions/dbo_fnSelectGenerator.md)
* [[dbo].[fnSelectOneGenerator]](../Programmability/Functions/Table-valued_Functions/dbo_fnSelectOneGenerator.md)
* [[dbo].[fnSelectOneLabTest]](../Programmability/Functions/Table-valued_Functions/dbo_fnSelectOneLabTest.md)
* [[dbo].[fnSelectScheduledLoads]](../Programmability/Functions/Table-valued_Functions/dbo_fnSelectScheduledLoads.md)


---

###### Author:  Sastry

###### Copyright 2023 - All Rights Reserved

###### Created: Thursday, October 5, 2023 9:55:17 PM

