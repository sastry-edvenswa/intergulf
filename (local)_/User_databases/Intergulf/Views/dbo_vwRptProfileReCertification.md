#### 

[Project](../../../../index.md) > [(local)\\](../../../index.md) > [User databases](../../index.md) > [Intergulf](../index.md) > [Views](Views.md) > dbo.vwRptProfileReCertification

# ![Views](../../../../Images/View32.png) [dbo].[vwRptProfileReCertification]

---

## <a name="#properties"></a>Properties

| Property | Value |
|---|---|
| Collation | SQL_Latin1_General_CP1_CI_AS |
| ANSI Nulls On | YES |
| Quoted Identifier On | YES |
| Created | 1:14:00 PM Thursday, January 16, 2014 |
| Last Modified | 7:47:57 PM Wednesday, April 29, 2020 |


---

## <a name="#columns"></a>Columns

| Name | Data Type | Max Length (Bytes) |
|---|---|---|
| Id | bigint | 8 |
| UserName | varchar(50) | 50 |
| ProfileId | varchar(50) | 50 |
| GeneratorName | varchar(100) | 100 |
| CustomerName | varchar(100) | 100 |
| ProfileType | varchar(50) | 50 |
| ProfileNo | varchar(50) | 50 |
| WasteCode | varchar(50) | 50 |
| Description | varchar(1000) | 1000 |
| Status | varchar(50) | 50 |
| LastName | varchar(50) | 50 |
| FirstName | varchar(50) | 50 |
| TreatmentCode | varchar(50) | 50 |
| GCApprovalDate | datetime | 8 |
| LastLoadDate | datetime | 8 |
| ExpirationDate | datetime | 8 |
| SalesPersonId | varchar(50) | 50 |
| CSRPersonId | varchar(50) | 50 |


---

## <a name="#sqlscript"></a>SQL Script

```sql
CREATE VIEW [dbo].[vwRptProfileReCertification]
AS
SELECT        TOP (100) PERCENT dbo.ReCertificationProfileReport.Id, dbo.ReCertificationProfileReport.UserName, dbo.ReCertificationProfileReport.ProfileId, dbo.ReCertificationProfileReport.GeneratorName, 
                         dbo.ReCertificationProfileReport.CustomerName, dbo.ReCertificationProfileReport.ProfileType, dbo.ReCertificationProfileReport.ProfileNo, dbo.ReCertificationProfileReport.WasteCode, 
                         dbo.ReCertificationProfileReport.Description, dbo.ReCertificationProfileReport.Status, dbo.UserMaster.LastName, dbo.UserMaster.FirstName, dbo.ReCertificationProfileReport.TreatmentCode, 
                         dbo.ReCertificationProfileReport.GCApprovalDate, dbo.ReCertificationProfileReport.LastLoadDate, dbo.ReCertificationProfileReport.ExpirationDate, dbo.ReCertificationProfileReport.SalesPersonId, 
                         dbo.ReCertificationProfileReport.CSRPersonId
FROM            dbo.ReCertificationProfileReport LEFT OUTER JOIN
                         dbo.UserMaster ON dbo.ReCertificationProfileReport.UserName = dbo.UserMaster.UserName
ORDER BY dbo.ReCertificationProfileReport.GeneratorName
GO

```


---

## <a name="#uses"></a>Uses

* [[dbo].[ReCertificationProfileReport]](../Tables/dbo_ReCertificationProfileReport.md)
* [[dbo].[UserMaster]](../Tables/dbo_UserMaster.md)


---

###### Author:  Sastry

###### Copyright 2023 - All Rights Reserved

###### Created: Thursday, October 5, 2023 9:55:17 PM

