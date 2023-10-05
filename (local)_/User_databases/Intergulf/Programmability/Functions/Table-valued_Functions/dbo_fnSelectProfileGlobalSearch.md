#### 

[Project](../../../../../../index.md) > [(local)\\](../../../../../index.md) > [User databases](../../../../index.md) > [Intergulf](../../../index.md) > Programmability > Functions > [Table-valued Functions](Table-valued_Functions.md) > dbo.fnSelectProfileGlobalSearch

# ![Table-valued Functions](../../../../../../Images/Function_Table32.png) [dbo].[fnSelectProfileGlobalSearch]

---

## <a name="#properties"></a>Properties

| Property | Value |
|---|---|
| ANSI Nulls On | NO |
| Quoted Identifier On | NO |


---

## <a name="#sqlscript"></a>SQL Script

```sql
SET QUOTED_IDENTIFIER OFF
GO
SET ANSI_NULLS OFF
GO



CREATE   FUNCTION [dbo].[fnSelectProfileGlobalSearch]
                 (  )
RETURNS table
AS
RETURN (
SELECT        TOP (100) PERCENT fnSelectProfile.Id, fnSelectProfile.GeneratorId AS [Generator Id], fnSelectGenerator.Name AS [Generator Name], fnSelectGenerator.Address AS [Generator Address], 
                         fnSelectProfile.ProfileNumber AS [Profile Number], fnSelectProfile.CustomerId AS [Customer Id], fnSelectCustomer.Name AS [Customer Name], fnSelectProfile.VendorId AS [Vendor Id], 
                         fnSelectVendor.Name AS [Vendor Name], fnSelectProfile.MaterialDescription, fnSelectProfile.Direction, fnSelectProfile.ProfileType, fnSelectProfile.WasteCode, fnSelectProfile.MaterialClassification, 
                         fnSelectProfile.MaterialCodeId, fnSelectProfile.ProductCategory, fnSelectProfile.SalesPersonId, fnSelectProfile.ProcessDescription, fnSelectProfile.DocumentType, fnSelectProfile.ContactName, 
                         fnSelectProfile.ContactEmail, fnSelectProfile.ContactPhone, fnSelectProfile.ContactFax, fnSelectProfile.DeepWell, fnSelectProfile.DispatchNotes, fnSelectProfile.HazMat, fnSelectProfile.ShippingName, 
                         fnSelectProfile.SpecialEquipment, fnSelectProfile.SpecialInstructions, fnSelectProfile.ReviewedBySales, fnSelectProfile.ReviewedByDispatch, fnSelectProfile.MSDSFileName, fnSelectProfile.LinkProfileId, 
                         fnSelectProfile.DestinationId, fnSelectProfile.HTYes, fnSelectProfile.Status, fnSelectProfile.EffectiveDate, fnSelectProfile.LoadFrequency, fnSelectProfile.CompanyProfileNumber, fnSelectProfile.CSRPersonId, 
                         dbo.Destination.Name AS Destination, dbo.fnGetDestinationDisplay(dbo.Destination.Name, dbo.Destination.Facility) AS DestinationDisplay, fnSelectProfile.EPAWasteCode1, fnSelectProfile.EPAWasteCode2, fnSelectProfile.EPAWasteCode3, 
                         fnSelectProfile.EPAWasteCode4,fnSelectProfile.ContractNumber
FROM            dbo.fnSelectProfile() AS fnSelectProfile LEFT OUTER JOIN
                         dbo.Destination ON fnSelectProfile.DestinationId = dbo.Destination.Id LEFT OUTER JOIN
                         dbo.fnSelectCustomer() AS fnSelectCustomer ON fnSelectProfile.CustomerId = fnSelectCustomer.Id LEFT OUTER JOIN
                         dbo.fnSelectVendor() AS fnSelectVendor ON fnSelectProfile.VendorId = fnSelectVendor.Id LEFT OUTER JOIN
                         dbo.fnSelectGenerator() AS fnSelectGenerator ON fnSelectProfile.GeneratorId = fnSelectGenerator.Id
ORDER BY [Generator Name]
       )














GO

```


---

## <a name="#uses"></a>Uses

* [[dbo].[Destination]](../../../Tables/dbo_Destination.md)
* [[dbo].[fnGetDestinationDisplay]](../Scalar-valued_Functions/dbo_fnGetDestinationDisplay.md)
* [[dbo].[fnSelectCustomer]](dbo_fnSelectCustomer.md)
* [[dbo].[fnSelectGenerator]](dbo_fnSelectGenerator.md)
* [[dbo].[fnSelectProfile]](dbo_fnSelectProfile.md)
* [[dbo].[fnSelectVendor]](dbo_fnSelectVendor.md)


---

###### Author:  Sastry

###### Copyright 2023 - All Rights Reserved

###### Created: Thursday, October 5, 2023 9:55:17 PM

