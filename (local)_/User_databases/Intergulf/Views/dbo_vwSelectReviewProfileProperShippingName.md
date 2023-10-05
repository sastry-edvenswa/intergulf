#### 

[Project](../../../../index.md) > [(local)\\](../../../index.md) > [User databases](../../index.md) > [Intergulf](../index.md) > [Views](Views.md) > dbo.vwSelectReviewProfileProperShippingName

# ![Views](../../../../Images/View32.png) [dbo].[vwSelectReviewProfileProperShippingName]

---

## <a name="#properties"></a>Properties

| Property | Value |
|---|---|
| Collation | SQL_Latin1_General_CP1_CI_AS |
| ANSI Nulls On | YES |
| Quoted Identifier On | YES |
| Created | 11:09:34 PM Monday, December 17, 2012 |
| Last Modified | 2:05:38 PM Sunday, January 25, 2015 |


---

## <a name="#columns"></a>Columns

| Name | Data Type | Max Length (Bytes) |
|---|---|---|
| Id | bigint | 8 |
| ProfileNumber | varchar(50) | 50 |
| ShippingName | varchar(1000) | 1000 |
| FunctionProperShippingName | varchar(5000) | 5000 |
| UseProperShippingName | nvarchar(500) | 1000 |


---

## <a name="#sqlscript"></a>SQL Script

```sql

CREATE VIEW [dbo].[vwSelectReviewProfileProperShippingName]
AS
SELECT     TOP 100 PERCENT dbo.Profile.Id, dbo.Profile.ProfileNumber, dbo.Profile.ShippingName, dbo.fnProperShippingName(dbo.Profile.MaterialCodeId) 
                      AS FunctionProperShippingName, dbo.MaterialCode.UseProperShippingName
FROM         dbo.Profile LEFT OUTER JOIN
                      dbo.MaterialCode ON dbo.Profile.MaterialCodeId = dbo.MaterialCode.ID
ORDER BY dbo.Profile.ProfileNumber

GO

```


---

## <a name="#uses"></a>Uses

* [[dbo].[MaterialCode]](../Tables/dbo_MaterialCode.md)
* [[dbo].[Profile]](../Tables/dbo_Profile.md)
* [[dbo].[fnProperShippingName]](../Programmability/Functions/Scalar-valued_Functions/dbo_fnProperShippingName.md)


---

###### Author:  Sastry

###### Copyright 2023 - All Rights Reserved

###### Created: Thursday, October 5, 2023 9:55:17 PM

