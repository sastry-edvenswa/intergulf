#### 

[Project](../../../../index.md) > [(local)\\](../../../index.md) > [User databases](../../index.md) > [Intergulf](../index.md) > [Views](Views.md) > dbo.vwRptProspectByName

# ![Views](../../../../Images/View32.png) [dbo].[vwRptProspectByName]

---

## <a name="#properties"></a>Properties

| Property | Value |
|---|---|
| Collation | SQL_Latin1_General_CP1_CI_AS |
| ANSI Nulls On | YES |
| Quoted Identifier On | YES |
| Created | 7:19:04 PM Monday, January 29, 2007 |
| Last Modified | 2:05:38 PM Sunday, January 25, 2015 |


---

## <a name="#columns"></a>Columns

| Name | Data Type | Max Length (Bytes) |
|---|---|---|
| Id | numeric(18,0) | 9 |
| Name | varchar(50) | 50 |
| Address | varchar(50) | 50 |
| City | varchar(50) | 50 |
| State | varchar(50) | 50 |
| Zip | varchar(50) | 50 |
| URL | varchar(255) | 255 |
| Refinery | varchar(255) | 255 |
| Capacity | varchar(1024) | 1024 |
| Location | varchar(1024) | 1024 |
| Processes | varchar(1024) | 1024 |
| Products | varchar(5000) | 5000 |
| FeedStocks | varchar(5000) | 5000 |
| ByProducts | varchar(5000) | 5000 |
| RawMaterial | varchar(5000) | 5000 |
| Waste | varchar(5000) | 5000 |
| Notes | varchar(1024) | 1024 |
| SalesPersonId | varchar(50) | 50 |
| FirstName | varchar(50) | 50 |
| LastName | varchar(50) | 50 |
| LastUpdateUser | varchar(50) | 50 |
| LastUpdateDate | datetime | 8 |


---

## <a name="#sqlscript"></a>SQL Script

```sql
CREATE VIEW [dbo].[vwRptProspectByName]
AS
SELECT     TOP 100 PERCENT dbo.Prospect.Id, dbo.Prospect.Name, dbo.Prospect.Address, dbo.Prospect.City, dbo.Prospect.State, dbo.Prospect.Zip, 
                      dbo.Prospect.URL, dbo.Prospect.Refinery, dbo.Prospect.Capacity, dbo.Prospect.Location, dbo.Prospect.Processes, dbo.Prospect.Products, 
                      dbo.Prospect.FeedStocks, dbo.Prospect.ByProducts, dbo.Prospect.RawMaterial, dbo.Prospect.Waste, dbo.Prospect.Notes, 
                      dbo.Prospect.SalesPersonId, dbo.UserMaster.FirstName, dbo.UserMaster.LastName, dbo.Prospect.LastUpdateUser, 
                      dbo.Prospect.LastUpdateDate
FROM         dbo.Prospect LEFT OUTER JOIN
                      dbo.UserMaster ON dbo.Prospect.SalesPersonId = dbo.UserMaster.UserName
ORDER BY dbo.Prospect.Name
GO

```


---

## <a name="#uses"></a>Uses

* [[dbo].[Prospect]](../Tables/dbo_Prospect.md)
* [[dbo].[UserMaster]](../Tables/dbo_UserMaster.md)


---

###### Author:  Sastry

###### Copyright 2023 - All Rights Reserved

###### Created: Thursday, October 5, 2023 9:55:17 PM

