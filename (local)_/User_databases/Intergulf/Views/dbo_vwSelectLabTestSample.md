#### 

[Project](../../../../index.md) > [(local)\\](../../../index.md) > [User databases](../../index.md) > [Intergulf](../index.md) > [Views](Views.md) > dbo.vwSelectLabTestSample

# ![Views](../../../../Images/View32.png) [dbo].[vwSelectLabTestSample]

---

## <a name="#properties"></a>Properties

| Property | Value |
|---|---|
| Collation | SQL_Latin1_General_CP1_CI_AS |
| ANSI Nulls On | YES |
| Quoted Identifier On | YES |
| Created | 7:24:35 PM Monday, January 29, 2007 |
| Last Modified | 2:05:38 PM Sunday, January 25, 2015 |


---

## <a name="#columns"></a>Columns

| Name | Data Type | Max Length (Bytes) |
|---|---|---|
| FirstName | varchar(50) | 50 |
| LastName | varchar(50) | 50 |
| Id | bigint | 8 |
| DueDate | datetime | 8 |
| Customer | varchar(50) | 50 |
| Facility | varchar(50) | 50 |
| MaterialDescription | varchar(50) | 50 |
| Status | varchar(50) | 50 |


---

## <a name="#sqlscript"></a>SQL Script

```sql
CREATE VIEW [dbo].[vwSelectLabTestSample]
AS
SELECT     TOP 100 PERCENT dbo.UserMaster.FirstName, dbo.UserMaster.LastName, fnSelectLabTestSample.Id, fnSelectLabTestSample.DueDate, 
                      fnSelectLabTestSample.Customer, fnSelectLabTestSample.Facility, fnSelectLabTestSample.MaterialDescription, fnSelectLabTestSample.Status
FROM         dbo.fnSelectLabTestSample() fnSelectLabTestSample LEFT OUTER JOIN
                      dbo.UserMaster ON fnSelectLabTestSample.SalesPersonId = dbo.UserMaster.UserName
ORDER BY dbo.UserMaster.LastName, fnSelectLabTestSample.DueDate DESC
GO

```


---

## <a name="#uses"></a>Uses

* [[dbo].[UserMaster]](../Tables/dbo_UserMaster.md)
* [[dbo].[fnSelectLabTestSample]](../Programmability/Functions/Table-valued_Functions/dbo_fnSelectLabTestSample.md)


---

###### Author:  Sastry

###### Copyright 2023 - All Rights Reserved

###### Created: Thursday, October 5, 2023 9:55:17 PM

