#### 

[Project](../../../../index.md) > [(local)\\](../../../index.md) > [User databases](../../index.md) > [Intergulf](../index.md) > [Views](Views.md) > dbo.vwSelectLoadsInactive

# ![Views](../../../../Images/View32.png) [dbo].[vwSelectLoadsInactive]

---

## <a name="#properties"></a>Properties

| Property | Value |
|---|---|
| Collation | SQL_Latin1_General_CP1_CI_AS |
| ANSI Nulls On | YES |
| Quoted Identifier On | YES |
| Created | 10:35:05 PM Sunday, November 6, 2011 |
| Last Modified | 2:05:38 PM Sunday, January 25, 2015 |


---

## <a name="#columns"></a>Columns

| Name | Data Type | Max Length (Bytes) |
|---|---|---|
| Id | bigint | 8 |
| Generator Name | varchar(100) | 100 |
| Customer Name | varchar(50) | 50 |
| Profile Number | varchar(50) | 50 |
| Waste Code | varchar(50) | 50 |
| MaterialCode | nvarchar(50) | 100 |
| Description | nvarchar(50) | 100 |
| ScheduledDate | datetime | 8 |
| LoadCount | int | 4 |
| ProfileId | bigint | 8 |
| Status | varchar(20) | 20 |
| SalesPersonId | varchar(50) | 50 |
| ProfileType | varchar(50) | 50 |
| InactiveExclude | bit | 1 |
| InactiveReviewed | bit | 1 |


---

## <a name="#sqlscript"></a>SQL Script

```sql

CREATE VIEW [dbo].[vwSelectLoadsInactive]
AS
SELECT     TOP 100 PERCENT dbo.Profile.Id, dbo.Generator.Name AS [Generator Name], dbo.Customer.Name AS [Customer Name], 
                      dbo.Profile.ProfileNumber AS [Profile Number], dbo.Profile.WasteCode AS [Waste Code], dbo.MaterialCode.MaterialCode, 
                      dbo.MaterialCode.Description, dbo.Loads.ScheduledDate, COUNT(dbo.Loads.ScheduledDate) AS LoadCount, dbo.Loads.ProfileId, dbo.Profile.Status, 
                      dbo.Profile.SalesPersonId, dbo.Profile.ProfileType, dbo.Profile.InactiveExclude, dbo.Profile.InactiveReviewed
FROM         dbo.Loads INNER JOIN
                      dbo.Profile ON dbo.Loads.ProfileId = dbo.Profile.Id INNER JOIN
                      dbo.Generator ON dbo.Profile.GeneratorId = dbo.Generator.Id INNER JOIN
                      dbo.MaterialCode ON dbo.Profile.MaterialCodeId = dbo.MaterialCode.ID INNER JOIN
                      dbo.Customer ON dbo.Profile.CustomerId = dbo.Customer.Id
GROUP BY dbo.Loads.ScheduledDate, dbo.Loads.ProfileId, dbo.Generator.Name, dbo.Profile.ProfileNumber, dbo.Profile.WasteCode, 
                      dbo.MaterialCode.MaterialCode, dbo.MaterialCode.Description, dbo.Customer.Name, dbo.Profile.Status, dbo.Profile.SalesPersonId, 
                      dbo.Profile.ProfileType, dbo.Profile.Id, dbo.Profile.InactiveExclude, dbo.Profile.InactiveReviewed
ORDER BY dbo.Generator.Name, dbo.Loads.ProfileId, dbo.Loads.ScheduledDate

GO

```


---

## <a name="#uses"></a>Uses

* [[dbo].[Customer]](../Tables/dbo_Customer.md)
* [[dbo].[Generator]](../Tables/dbo_Generator.md)
* [[dbo].[Loads]](../Tables/dbo_Loads.md)
* [[dbo].[MaterialCode]](../Tables/dbo_MaterialCode.md)
* [[dbo].[Profile]](../Tables/dbo_Profile.md)


---

###### Author:  Sastry

###### Copyright 2023 - All Rights Reserved

###### Created: Thursday, October 5, 2023 9:55:17 PM

