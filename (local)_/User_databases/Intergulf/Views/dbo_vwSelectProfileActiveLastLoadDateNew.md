#### 

[Project](../../../../index.md) > [(local)\\](../../../index.md) > [User databases](../../index.md) > [Intergulf](../index.md) > [Views](Views.md) > dbo.vwSelectProfileActiveLastLoadDateNew

# ![Views](../../../../Images/View32.png) [dbo].[vwSelectProfileActiveLastLoadDateNew]

---

## <a name="#properties"></a>Properties

| Property | Value |
|---|---|
| Collation | SQL_Latin1_General_CP1_CI_AS |
| ANSI Nulls On | YES |
| Quoted Identifier On | YES |
| Created | 7:11:05 PM Monday, January 9, 2023 |
| Last Modified | 6:31:44 PM Tuesday, January 10, 2023 |


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
| StatusChangeDate | datetime | 8 |
| CreateDateTime | datetime | 8 |
| Last Load Date | datetime | 8 |
| LoadFrequency | varchar(50) | 50 |
| StatusDescription | varchar(2000) | 2000 |


---

## <a name="#sqlscript"></a>SQL Script

```sql
CREATE VIEW [dbo].[vwSelectProfileActiveLastLoadDateNew]
AS
SELECT        TOP (100) PERCENT dbo.Profile.Id, dbo.Generator.Name AS [Generator Name], dbo.Customer.Name AS [Customer Name], dbo.Profile.ProfileNumber, dbo.Profile.WasteCode, dbo.Profile.MaterialDescription, 
                         dbo.Profile.Volume, dbo.Profile.ProfileType, dbo.Profile.Status, dbo.Profile.StatusChangeDate, dbo.Profile.CreateDateTime,
                             (SELECT        TOP (1) ScheduledDate
                               FROM            dbo.Loads
                               WHERE        (DispatchStatus = 'Complete') AND (ProfileId = dbo.Profile.Id)
                               ORDER BY ScheduledDate DESC) AS [Last Load Date], dbo.Profile.LoadFrequency, dbo.Profile.StatusDescription
FROM            dbo.Profile LEFT OUTER JOIN
                         dbo.Customer ON dbo.Profile.CustomerId = dbo.Customer.Id LEFT OUTER JOIN
                         dbo.Generator ON dbo.Profile.GeneratorId = dbo.Generator.Id
WHERE        (dbo.Profile.Status = 'Active')
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

