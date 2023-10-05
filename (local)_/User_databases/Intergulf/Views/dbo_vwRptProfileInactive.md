#### 

[Project](../../../../index.md) > [(local)\\](../../../index.md) > [User databases](../../index.md) > [Intergulf](../index.md) > [Views](Views.md) > dbo.vwRptProfileInactive

# ![Views](../../../../Images/View32.png) [dbo].[vwRptProfileInactive]

---

## <a name="#properties"></a>Properties

| Property | Value |
|---|---|
| Collation | SQL_Latin1_General_CP1_CI_AS |
| ANSI Nulls On | YES |
| Quoted Identifier On | YES |
| Created | 9:35:30 PM Tuesday, November 8, 2011 |
| Last Modified | 2:05:38 PM Sunday, January 25, 2015 |


---

## <a name="#columns"></a>Columns

| Name | Data Type | Max Length (Bytes) |
|---|---|---|
| LastName | varchar(50) | 50 |
| FirstName | varchar(50) | 50 |
| Id | bigint | 8 |
| ProfileId | varchar(50) | 50 |
| GeneratorName | varchar(300) | 300 |
| CustomerName | varchar(300) | 300 |
| ProfileNo | varchar(50) | 50 |
| WasteCode | varchar(50) | 50 |
| MaterialCode | varchar(50) | 50 |
| Description | varchar(500) | 500 |
| LastDate | datetime | 8 |
| LoadCount | bigint | 8 |
| Status | varchar(50) | 50 |
| UserName | varchar(50) | 50 |


---

## <a name="#sqlscript"></a>SQL Script

```sql

CREATE VIEW [dbo].[vwRptProfileInactive]
AS
SELECT     TOP 100 PERCENT dbo.UserMaster.LastName, dbo.UserMaster.FirstName, dbo.InactiveProfileReport.Id, dbo.InactiveProfileReport.ProfileId, 
                      dbo.InactiveProfileReport.GeneratorName, dbo.InactiveProfileReport.CustomerName, dbo.InactiveProfileReport.ProfileNo, 
                      dbo.InactiveProfileReport.WasteCode, dbo.InactiveProfileReport.MaterialCode, dbo.InactiveProfileReport.Description, 
                      dbo.InactiveProfileReport.LastDate, dbo.InactiveProfileReport.LoadCount, dbo.InactiveProfileReport.Status, dbo.InactiveProfileReport.UserName
FROM         dbo.InactiveProfileReport LEFT OUTER JOIN
                      dbo.UserMaster ON dbo.InactiveProfileReport.SalesPersonId = dbo.UserMaster.UserName
ORDER BY dbo.UserMaster.LastName, dbo.UserMaster.FirstName, dbo.InactiveProfileReport.GeneratorName

GO

```


---

## <a name="#uses"></a>Uses

* [[dbo].[InactiveProfileReport]](../Tables/dbo_InactiveProfileReport.md)
* [[dbo].[UserMaster]](../Tables/dbo_UserMaster.md)


---

###### Author:  Sastry

###### Copyright 2023 - All Rights Reserved

###### Created: Thursday, October 5, 2023 9:55:17 PM

