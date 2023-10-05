#### 

[Project](../../../../index.md) > [(local)\\](../../../index.md) > [User databases](../../index.md) > [Intergulf](../index.md) > [Views](Views.md) > dbo.vwSelectLabTest

# ![Views](../../../../Images/View32.png) [dbo].[vwSelectLabTest]

---

## <a name="#properties"></a>Properties

| Property | Value |
|---|---|
| Collation | SQL_Latin1_General_CP1_CI_AS |
| ANSI Nulls On | YES |
| Quoted Identifier On | YES |
| Created | 9:43:02 PM Tuesday, February 12, 2013 |
| Last Modified | 2:05:38 PM Sunday, January 25, 2015 |


---

## <a name="#columns"></a>Columns

| Name | Data Type | Max Length (Bytes) |
|---|---|---|
| Id | bigint | 8 |
| TestDate | datetime | 8 |
| LoadId | decimal(18,0) | 9 |
| Customer Name | varchar(50) | 50 |
| Generator Name | varchar(100) | 100 |
| Profile Number | varchar(50) | 50 |
| DocumentNumber | varchar(50) | 50 |
| DocumentType | varchar(50) | 50 |
| TruckNumber | varchar(50) | 50 |
| Location | varchar(50) | 50 |
| Status | varchar(50) | 50 |
| Notes | varchar(5000) | 5000 |
| SalesPerson | varchar(101) | 101 |


---

## <a name="#sqlscript"></a>SQL Script

```sql

CREATE VIEW [dbo].[vwSelectLabTest]
AS
SELECT     TOP 100 PERCENT dbo.LabTest.Id, dbo.LabTest.TestDate, dbo.LabTest.LoadId, dbo.Customer.Name AS [Customer Name], 
                      dbo.Generator.Name AS [Generator Name], dbo.Profile.ProfileNumber AS [Profile Number], dbo.LabTest.DocumentNumber, dbo.LabTest.DocumentType, 
                      dbo.LabTest.TruckNumber, dbo.LabTest.Location, dbo.LabTest.Status, dbo.LabTest.Notes, 
                      dbo.UserMaster.FirstName + ' ' + dbo.UserMaster.LastName AS SalesPerson
FROM         dbo.UserMaster INNER JOIN
                      dbo.Profile ON dbo.UserMaster.UserName = dbo.Profile.SalesPersonId RIGHT OUTER JOIN
                      dbo.LabTest ON dbo.Profile.Id = dbo.LabTest.ProfileId LEFT OUTER JOIN
                      dbo.Generator ON dbo.LabTest.GeneratorId = dbo.Generator.Id LEFT OUTER JOIN
                      dbo.Customer ON dbo.LabTest.CustomerId = dbo.Customer.Id
ORDER BY dbo.LabTest.TestDate DESC, dbo.Generator.Name

GO

```


---

## <a name="#uses"></a>Uses

* [[dbo].[Customer]](../Tables/dbo_Customer.md)
* [[dbo].[Generator]](../Tables/dbo_Generator.md)
* [[dbo].[LabTest]](../Tables/dbo_LabTest.md)
* [[dbo].[Profile]](../Tables/dbo_Profile.md)
* [[dbo].[UserMaster]](../Tables/dbo_UserMaster.md)


---

###### Author:  Sastry

###### Copyright 2023 - All Rights Reserved

###### Created: Thursday, October 5, 2023 9:55:17 PM

