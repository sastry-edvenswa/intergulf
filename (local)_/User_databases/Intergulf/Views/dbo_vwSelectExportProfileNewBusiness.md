#### 

[Project](../../../../index.md) > [(local)\\](../../../index.md) > [User databases](../../index.md) > [Intergulf](../index.md) > [Views](Views.md) > dbo.vwSelectExportProfileNewBusiness

# ![Views](../../../../Images/View32.png) [dbo].[vwSelectExportProfileNewBusiness]

---

## <a name="#properties"></a>Properties

| Property | Value |
|---|---|
| Collation | SQL_Latin1_General_CP1_CI_AS |
| ANSI Nulls On | YES |
| Quoted Identifier On | YES |
| Created | 10:20:23 PM Friday, July 24, 2020 |
| Last Modified | 10:33:51 PM Friday, July 24, 2020 |


---

## <a name="#columns"></a>Columns

| Name | Data Type | Max Length (Bytes) |
|---|---|---|
| Id | bigint | 8 |
| GeneratorId | bigint | 8 |
| Name | varchar(100) | 100 |
| CustomerId | bigint | 8 |
| Expr1 | varchar(100) | 100 |
| ProfileNumber | varchar(50) | 50 |
| WasteCode | varchar(50) | 50 |
| LoadFrequency | varchar(50) | 50 |
| ProfileType | varchar(50) | 50 |
| Direction | varchar(50) | 50 |
| SalesPersonId | varchar(50) | 50 |
| Status | varchar(20) | 20 |
| BillingDepartment | varchar(100) | 100 |
| CreateDate | datetime | 8 |
| CreateDateTime | datetime | 8 |
| NoLoads | int | 4 |


---

## <a name="#sqlscript"></a>SQL Script

```sql
CREATE VIEW [dbo].[vwSelectExportProfileNewBusiness]
AS
SELECT        TOP (100) PERCENT dbo.Profile.Id, dbo.Profile.GeneratorId, dbo.Generator.Name, dbo.Profile.CustomerId, dbo.Customer.Name AS Expr1, dbo.Profile.ProfileNumber, dbo.Profile.WasteCode, 
                         dbo.Profile.LoadFrequency, dbo.Profile.ProfileType, dbo.Profile.Direction, dbo.Profile.SalesPersonId, dbo.Profile.Status, dbo.Profile.BillingDepartment, dbo.Profile.CreateDate, dbo.Profile.CreateDateTime,
                             (SELECT        COUNT(Id) AS NoLoads
                               FROM            dbo.Loads
                               WHERE        (dbo.Profile.Id = ProfileId) AND (dbo.Profile.CreateDate >= '06/24/2020') AND (DispatchStatus <> 'Canceled')) AS NoLoads
FROM            dbo.Profile LEFT OUTER JOIN
                         dbo.Customer ON dbo.Profile.CustomerId = dbo.Customer.Id LEFT OUTER JOIN
                         dbo.Generator ON dbo.Profile.GeneratorId = dbo.Generator.Id
WHERE        (dbo.Profile.CreateDate >= CONVERT(DATETIME, '2020-06-24 00:00:00', 102))
ORDER BY dbo.Generator.Name, dbo.Profile.ProfileNumber
GO

```


---

## <a name="#uses"></a>Uses

* [[dbo].[Customer]](../Tables/dbo_Customer.md)
* [[dbo].[Generator]](../Tables/dbo_Generator.md)
* [[dbo].[Loads]](../Tables/dbo_Loads.md)
* [[dbo].[Profile]](../Tables/dbo_Profile.md)


---

###### Author:  Sastry

###### Copyright 2023 - All Rights Reserved

###### Created: Thursday, October 5, 2023 9:55:17 PM

