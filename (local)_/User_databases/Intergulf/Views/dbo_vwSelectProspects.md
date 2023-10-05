#### 

[Project](../../../../index.md) > [(local)\\](../../../index.md) > [User databases](../../index.md) > [Intergulf](../index.md) > [Views](Views.md) > dbo.vwSelectProspects

# ![Views](../../../../Images/View32.png) [dbo].[vwSelectProspects]

---

## <a name="#properties"></a>Properties

| Property | Value |
|---|---|
| Collation | SQL_Latin1_General_CP1_CI_AS |
| ANSI Nulls On | YES |
| Quoted Identifier On | YES |
| Created | 10:54:05 AM Tuesday, May 19, 2015 |
| Last Modified | 10:54:05 AM Tuesday, May 19, 2015 |


---

## <a name="#columns"></a>Columns

| Name | Data Type | Max Length (Bytes) | Identity |
|---|---|---|---|
| Id | numeric(18,0) | 9 | 0 - 0 |
| Name | varchar(200) | 200 |  |
| Address | varchar(200) | 200 |  |
| City | varchar(200) | 200 |  |
| State | varchar(50) | 50 |  |
| Zip | varchar(50) | 50 |  |
| County | varchar(50) | 50 |  |
| MailName | varchar(200) | 200 |  |
| MailAddress | varchar(200) | 200 |  |
| MailCity | varchar(200) | 200 |  |
| MailState | varchar(50) | 50 |  |
| MailZip | varchar(50) | 50 |  |
| Phone | varchar(50) | 50 |  |
| Fax | varchar(50) | 50 |  |
| ParentName | varchar(200) | 200 |  |
| ParentAddress | varchar(200) | 200 |  |
| ParentCity | varchar(200) | 200 |  |
| ParentState | varchar(50) | 50 |  |
| ParentZip | varchar(50) | 50 |  |
| ParentPhone | varchar(50) | 50 |  |
| ParentFax | varchar(50) | 50 |  |
| TollFree | varchar(50) | 50 |  |
| WebSite | varchar(255) | 255 |  |
| Email | varchar(50) | 50 |  |
| YearEstablished | varchar(50) | 50 |  |
| NoEmployees | varchar(50) | 50 |  |
| AnnualSales | varchar(50) | 50 |  |
| SIC | varchar(10) | 10 |  |
| SICDescription | varchar(2000) | 2000 |  |
| NAICS | varchar(10) | 10 |  |
| NAICSDescription | varchar(2000) | 2000 |  |
| Refinery | varchar(255) | 255 |  |
| Capacity | varchar(1024) | 1024 |  |
| Location | varchar(1024) | 1024 |  |
| Processes | varchar(1024) | 1024 |  |
| Products | varchar(5000) | 5000 |  |
| FeedStocks | varchar(5000) | 5000 |  |
| ByProducts | varchar(5000) | 5000 |  |
| RawMaterial | varchar(5000) | 5000 |  |
| Waste | varchar(5000) | 5000 |  |
| Notes | varchar(1024) | 1024 |  |
| PlantManager | varchar(50) | 50 |  |
| PlantManagerPhone | varchar(50) | 50 |  |
| PurchasingManager | varchar(50) | 50 |  |
| PurchasingManagerPhone | varchar(50) | 50 |  |
| EngineeringManager | varchar(50) | 50 |  |
| EngineeringManagerPhone | varchar(50) | 50 |  |
| EnvironmentalManager | varchar(50) | 50 |  |
| EnvironmentalManagerPhone | varchar(50) | 50 |  |
| SalesPersonId | varchar(50) | 50 |  |
| MarkForDeletion | varchar(1) | 1 |  |
| AccessId | bigint | 8 |  |
| UpdateDateTime | datetime | 8 |  |
| UpdateUser | varchar(50) | 50 |  |
| UpdateComputer | varchar(50) | 50 |  |
| CreateUser | varchar(50) | 50 |  |
| CreateDateTime | datetime | 8 |  |
| CreateComputer | varchar(50) | 50 |  |
| SalesPersonFirstName | varchar(50) | 50 |  |
| SalesPersonLastName | varchar(50) | 50 |  |


---

## <a name="#sqlscript"></a>SQL Script

```sql

CREATE VIEW [dbo].[vwSelectProspects]
AS
SELECT     dbo.Prospect.Id, dbo.Prospect.Name, dbo.Prospect.Address, dbo.Prospect.City, dbo.Prospect.State, dbo.Prospect.Zip, dbo.Prospect.County, dbo.Prospect.MailName, 
                      dbo.Prospect.MailAddress, dbo.Prospect.MailCity, dbo.Prospect.MailState, dbo.Prospect.MailZip, dbo.Prospect.Phone, dbo.Prospect.Fax, dbo.Prospect.ParentName, 
                      dbo.Prospect.ParentAddress, dbo.Prospect.ParentCity, dbo.Prospect.ParentState, dbo.Prospect.ParentZip, dbo.Prospect.ParentPhone, dbo.Prospect.ParentFax, 
                      dbo.Prospect.TollFree, dbo.Prospect.WebSite, dbo.Prospect.Email, dbo.Prospect.YearEstablished, dbo.Prospect.NoEmployees, dbo.Prospect.AnnualSales, 
                      dbo.Prospect.SIC, dbo.Prospect.SICDescription, dbo.Prospect.NAICS, dbo.Prospect.NAICSDescription, dbo.Prospect.Refinery, dbo.Prospect.Capacity, 
                      dbo.Prospect.Location, dbo.Prospect.Processes, dbo.Prospect.Products, dbo.Prospect.FeedStocks, dbo.Prospect.ByProducts, dbo.Prospect.RawMaterial, 
                      dbo.Prospect.Waste, dbo.Prospect.Notes, dbo.Prospect.PlantManager, dbo.Prospect.PlantManagerPhone, dbo.Prospect.PurchasingManager, 
                      dbo.Prospect.PurchasingManagerPhone, dbo.Prospect.EngineeringManager, dbo.Prospect.EngineeringManagerPhone, dbo.Prospect.EnvironmentalManager, 
                      dbo.Prospect.EnvironmentalManagerPhone, dbo.Prospect.SalesPersonId, dbo.Prospect.MarkForDeletion, dbo.Prospect.AccessId, dbo.Prospect.UpdateDateTime, 
                      dbo.Prospect.UpdateUser, dbo.Prospect.UpdateComputer, dbo.Prospect.CreateUser, dbo.Prospect.CreateDateTime, dbo.Prospect.CreateComputer, 
                      dbo.UserMaster.LastName AS SalesPersonFirstName, dbo.UserMaster.FirstName AS SalesPersonLastName
FROM         dbo.Prospect LEFT OUTER JOIN
                      dbo.UserMaster ON dbo.Prospect.SalesPersonId = dbo.UserMaster.UserName

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

