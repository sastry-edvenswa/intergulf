#### 

[Project](../../../../index.md) > [(local)\\](../../../index.md) > [User databases](../../index.md) > [Intergulf](../index.md) > [Views](Views.md) > dbo.vwSelectProfilesInactive

# ![Views](../../../../Images/View32.png) [dbo].[vwSelectProfilesInactive]

---

## <a name="#properties"></a>Properties

| Property | Value |
|---|---|
| Collation | SQL_Latin1_General_CP1_CI_AS |
| ANSI Nulls On | YES |
| Quoted Identifier On | YES |
| Created | 9:23:05 PM Monday, August 19, 2013 |
| Last Modified | 2:05:38 PM Sunday, January 25, 2015 |


---

## <a name="#columns"></a>Columns

| Name | Data Type | Max Length (Bytes) |
|---|---|---|
| ProfileId | bigint | 8 |
| Generator Name | varchar(100) | 100 |
| Customer Name | varchar(50) | 50 |
| Profile Number | varchar(50) | 50 |
| Waste Code | varchar(50) | 50 |
| MaterialCode | nvarchar(50) | 100 |
| Description | nvarchar(50) | 100 |
| Status | varchar(20) | 20 |
| SalesPersonId | varchar(50) | 50 |
| InactiveReviewed | bit | 1 |
| InactiveExclude | bit | 1 |
| ProfileType | varchar(50) | 50 |


---

## <a name="#sqlscript"></a>SQL Script

```sql

CREATE VIEW [dbo].[vwSelectProfilesInactive]
AS
SELECT     TOP 100 PERCENT dbo.Profile.Id AS ProfileId, dbo.Generator.Name AS [Generator Name], dbo.Customer.Name AS [Customer Name], 
                      dbo.Profile.ProfileNumber AS [Profile Number], dbo.Profile.WasteCode AS [Waste Code], dbo.MaterialCode.MaterialCode, 
                      dbo.MaterialCode.Description, dbo.Profile.Status, dbo.Profile.SalesPersonId, dbo.Profile.InactiveReviewed, dbo.Profile.InactiveExclude, 
                      dbo.Profile.ProfileType
FROM         dbo.Profile LEFT OUTER JOIN
                      dbo.MaterialCode ON dbo.Profile.MaterialCodeId = dbo.MaterialCode.ID LEFT OUTER JOIN
                      dbo.Customer ON dbo.Profile.CustomerId = dbo.Customer.Id LEFT OUTER JOIN
                      dbo.Generator ON dbo.Profile.GeneratorId = dbo.Generator.Id
ORDER BY dbo.Generator.Name, dbo.Profile.ProfileNumber

GO

```


---

## <a name="#uses"></a>Uses

* [[dbo].[Customer]](../Tables/dbo_Customer.md)
* [[dbo].[Generator]](../Tables/dbo_Generator.md)
* [[dbo].[MaterialCode]](../Tables/dbo_MaterialCode.md)
* [[dbo].[Profile]](../Tables/dbo_Profile.md)


---

###### Author:  Sastry

###### Copyright 2023 - All Rights Reserved

###### Created: Thursday, October 5, 2023 9:55:17 PM

