#### 

[Project](../../../../index.md) > [(local)\\](../../../index.md) > [User databases](../../index.md) > [Intergulf](../index.md) > [Views](Views.md) > dbo.vwSelectProfileActiveLastLoadDate

# ![Views](../../../../Images/View32.png) [dbo].[vwSelectProfileActiveLastLoadDate]

---

## <a name="#properties"></a>Properties

| Property | Value |
|---|---|
| Collation | SQL_Latin1_General_CP1_CI_AS |
| ANSI Nulls On | YES |
| Quoted Identifier On | YES |
| Created | 7:43:30 PM Tuesday, April 21, 2020 |
| Last Modified | 5:24:02 PM Tuesday, April 28, 2020 |


---

## <a name="#columns"></a>Columns

| Name | Data Type | Max Length (Bytes) |
|---|---|---|
| Id | bigint | 8 |
| Generator Name | varchar(100) | 100 |
| Customer Name | varchar(100) | 100 |
| ProfileNumber | varchar(50) | 50 |
| WasteCode | varchar(50) | 50 |
| MaterialDescription | varchar(3000) | 3000 |
| Volume | varchar(50) | 50 |
| ProfileType | varchar(50) | 50 |
| Status | varchar(20) | 20 |
| Last Load Date | datetime | 8 |
| LoadFrequency | varchar(50) | 50 |


---

## <a name="#sqlscript"></a>SQL Script

```sql
/*[Generator Name]*/
CREATE VIEW [dbo].[vwSelectProfileActiveLastLoadDate]
AS
SELECT        TOP (100) PERCENT dbo.Profile.Id, dbo.Generator.Name AS [Generator Name], dbo.Customer.Name AS [Customer Name], dbo.Profile.ProfileNumber, dbo.Profile.WasteCode, dbo.Profile.MaterialDescription, 
                         dbo.Profile.Volume, dbo.Profile.ProfileType, dbo.Profile.Status,
                             (SELECT        TOP (1) ScheduledDate
                               FROM            dbo.Loads
                               WHERE        (DispatchStatus = 'complete') AND (ProfileId = dbo.Profile.Id)) AS [Last Load Date], dbo.Profile.LoadFrequency
FROM            dbo.Profile LEFT OUTER JOIN
                         dbo.Customer ON dbo.Profile.CustomerId = dbo.Customer.Id LEFT OUTER JOIN
                         dbo.Generator ON dbo.Profile.GeneratorId = dbo.Generator.Id
WHERE        (dbo.Profile.ProfileType = 'Waste') AND (dbo.Profile.Status = 'Active') AND (dbo.Profile.LoadFrequency <> 'One Time')
ORDER BY [Generator Name]
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

