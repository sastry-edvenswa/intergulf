#### 

[Project](../../../../index.md) > [(local)\\](../../../index.md) > [User databases](../../index.md) > [Intergulf](../index.md) > [Views](Views.md) > dbo.vwCustomerGeneratorProfileReport

# ![Views](../../../../Images/View32.png) [dbo].[vwCustomerGeneratorProfileReport]

---

## <a name="#properties"></a>Properties

| Property | Value |
|---|---|
| Collation | SQL_Latin1_General_CP1_CI_AS |
| ANSI Nulls On | YES |
| Quoted Identifier On | YES |
| Created | 7:09:15 PM Monday, January 29, 2007 |
| Last Modified | 2:05:38 PM Sunday, January 25, 2015 |


---

## <a name="#columns"></a>Columns

| Name | Data Type | Max Length (Bytes) |
|---|---|---|
| Id | bigint | 8 |
| Generator Id | bigint | 8 |
| Generator Name | varchar(100) | 100 |
| Generator Address | varchar(50) | 50 |
| Profile Number | varchar(50) | 50 |
| Customer Id | bigint | 8 |
| Customer Name | varchar(50) | 50 |
| Vendor Id | bigint | 8 |
| Vendor Name | varchar(50) | 50 |
| MaterialDescription | varchar(3000) | 3000 |
| Direction | varchar(50) | 50 |
| ProfileType | varchar(50) | 50 |
| WasteCode | varchar(50) | 50 |
| MaterialClassification | varchar(200) | 200 |
| MaterialCodeId | int | 4 |
| ProductCategory | varchar(50) | 50 |
| SalesPersonId | varchar(50) | 50 |
| ProcessDescription | varchar(3000) | 3000 |
| DocumentType | varchar(50) | 50 |
| ContactName | varchar(50) | 50 |
| ContactEmail | varchar(50) | 50 |
| ContactPhone | varchar(50) | 50 |
| ContactFax | varchar(50) | 50 |
| DeepWell | char(10) | 10 |
| DispatchNotes | varchar(3000) | 3000 |


---

## <a name="#sqlscript"></a>SQL Script

```sql
CREATE VIEW [dbo].[vwCustomerGeneratorProfileReport]
AS
SELECT     TOP 100 PERCENT dbo.Profile.Id, dbo.Profile.GeneratorId AS [Generator Id], dbo.Generator.Name AS [Generator Name], 
                      dbo.Generator.Address AS [Generator Address], dbo.Profile.ProfileNumber AS [Profile Number], dbo.Profile.CustomerId AS [Customer Id], 
                      dbo.Customer.Name AS [Customer Name], dbo.Profile.VendorId AS [Vendor Id], dbo.Vendor.Name AS [Vendor Name], dbo.Profile.MaterialDescription, 
                      dbo.Profile.Direction, dbo.Profile.ProfileType, dbo.Profile.WasteCode, dbo.Profile.MaterialClassification, dbo.Profile.MaterialCodeId, 
                      dbo.Profile.ProductCategory, dbo.Profile.SalesPersonId, dbo.Profile.ProcessDescription, dbo.Profile.DocumentType, dbo.Profile.ContactName, 
                      dbo.Profile.ContactEmail, dbo.Profile.ContactPhone, dbo.Profile.ContactFax, dbo.Profile.DeepWell, dbo.Profile.DispatchNotes
FROM         dbo.Profile LEFT OUTER JOIN
                      dbo.Customer ON dbo.Profile.CustomerId = dbo.Customer.Id LEFT OUTER JOIN
                      dbo.Vendor ON dbo.Profile.VendorId = dbo.Vendor.Id LEFT OUTER JOIN
                      dbo.Generator ON dbo.Profile.GeneratorId = dbo.Generator.Id
ORDER BY dbo.Generator.Name
GO

```


---

## <a name="#uses"></a>Uses

* [[dbo].[Customer]](../Tables/dbo_Customer.md)
* [[dbo].[Generator]](../Tables/dbo_Generator.md)
* [[dbo].[Profile]](../Tables/dbo_Profile.md)
* [[dbo].[Vendor]](../Tables/dbo_Vendor.md)


---

###### Author:  Sastry

###### Copyright 2023 - All Rights Reserved

###### Created: Thursday, October 5, 2023 9:55:17 PM

