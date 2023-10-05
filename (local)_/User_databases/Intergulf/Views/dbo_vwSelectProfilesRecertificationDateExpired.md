#### 

[Project](../../../../index.md) > [(local)\\](../../../index.md) > [User databases](../../index.md) > [Intergulf](../index.md) > [Views](Views.md) > dbo.vwSelectProfilesRecertificationDateExpired

# ![Views](../../../../Images/View32.png) [dbo].[vwSelectProfilesRecertificationDateExpired]

---

## <a name="#properties"></a>Properties

| Property | Value |
|---|---|
| Collation | SQL_Latin1_General_CP1_CI_AS |
| ANSI Nulls On | YES |
| Quoted Identifier On | YES |
| Created | 7:48:56 PM Wednesday, November 15, 2017 |
| Last Modified | 7:48:56 PM Wednesday, November 15, 2017 |


---

## <a name="#columns"></a>Columns

| Name | Data Type | Max Length (Bytes) |
|---|---|---|
| Id | bigint | 8 |
| Generator Id | bigint | 8 |
| Generator Name | varchar(100) | 100 |
| Generator Address | varchar(3000) | 3000 |
| Profile Number | varchar(50) | 50 |
| Customer Id | bigint | 8 |
| Customer Name | varchar(50) | 50 |
| Vendor Id | bigint | 8 |
| Vendor Name | varchar(50) | 50 |
| Direction | varchar(50) | 50 |
| ProfileType | varchar(50) | 50 |
| WasteCode | varchar(50) | 50 |
| MaterialClassification | varchar(200) | 200 |
| MaterialCodeId | int | 4 |
| ProductCategory | varchar(50) | 50 |
| SalesPersonId | varchar(50) | 50 |
| DocumentType | varchar(50) | 50 |
| ContactName | varchar(50) | 50 |
| ContactEmail | varchar(50) | 50 |
| ContactPhone | varchar(50) | 50 |
| ContactFax | varchar(50) | 50 |
| DeepWell | varchar(50) | 50 |
| HazMat | varchar(50) | 50 |
| ShippingName | varchar(1000) | 1000 |
| Status | varchar(20) | 20 |
| CertificationDate | nvarchar(4000) | 8000 |
| LastLoadDate | nvarchar(4000) | 8000 |


---

## <a name="#sqlscript"></a>SQL Script

```sql

CREATE VIEW [dbo].[vwSelectProfilesRecertificationDateExpired]
AS
SELECT        TOP (100) PERCENT fnSelectProfile.Id, fnSelectProfile.GeneratorId AS [Generator Id], fnSelectGenerator.Name AS [Generator Name], 
                         fnSelectGenerator.Address AS [Generator Address], fnSelectProfile.ProfileNumber AS [Profile Number], fnSelectProfile.CustomerId AS [Customer Id], 
                         fnSelectCustomer.Name AS [Customer Name], fnSelectProfile.VendorId AS [Vendor Id], fnSelectVendor.Name AS [Vendor Name], fnSelectProfile.Direction, 
                         fnSelectProfile.ProfileType, fnSelectProfile.WasteCode, fnSelectProfile.MaterialClassification, fnSelectProfile.MaterialCodeId, fnSelectProfile.ProductCategory, 
                         fnSelectProfile.SalesPersonId, fnSelectProfile.DocumentType, fnSelectProfile.ContactName, fnSelectProfile.ContactEmail, fnSelectProfile.ContactPhone, 
                         fnSelectProfile.ContactFax, fnSelectProfile.DeepWell, fnSelectProfile.HazMat, fnSelectProfile.ShippingName, fnSelectProfile.Status, 
                         Format(fnSelectProfile.EffectiveDate, 'MM/dd/yyyy') AS CertificationDate, Format
                             ((SELECT        MAX(ScheduledDate) AS MaxDate
                                 FROM            dbo.Loads
                                 GROUP BY ProfileId
                                 HAVING        (ProfileId = fnSelectProfile.Id)), 'MM/dd/yyyy') AS LastLoadDate
FROM            dbo.fnSelectProfile() AS fnSelectProfile LEFT OUTER JOIN
                         dbo.fnSelectCustomer() AS fnSelectCustomer ON fnSelectProfile.CustomerId = fnSelectCustomer.Id LEFT OUTER JOIN
                         dbo.fnSelectVendor() AS fnSelectVendor ON fnSelectProfile.VendorId = fnSelectVendor.Id LEFT OUTER JOIN
                         dbo.fnSelectGenerator() AS fnSelectGenerator ON fnSelectProfile.GeneratorId = fnSelectGenerator.Id
WHERE        (fnSelectProfile.Status = 'Active') AND (Format(fnSelectProfile.EffectiveDate, 'MM/dd/yyyy') <= '11/15/2017')
ORDER BY [Generator Name]

GO

```


---

## <a name="#uses"></a>Uses

* [[dbo].[Loads]](../Tables/dbo_Loads.md)
* [[dbo].[fnSelectCustomer]](../Programmability/Functions/Table-valued_Functions/dbo_fnSelectCustomer.md)
* [[dbo].[fnSelectGenerator]](../Programmability/Functions/Table-valued_Functions/dbo_fnSelectGenerator.md)
* [[dbo].[fnSelectProfile]](../Programmability/Functions/Table-valued_Functions/dbo_fnSelectProfile.md)
* [[dbo].[fnSelectVendor]](../Programmability/Functions/Table-valued_Functions/dbo_fnSelectVendor.md)


---

###### Author:  Sastry

###### Copyright 2023 - All Rights Reserved

###### Created: Thursday, October 5, 2023 9:55:17 PM

