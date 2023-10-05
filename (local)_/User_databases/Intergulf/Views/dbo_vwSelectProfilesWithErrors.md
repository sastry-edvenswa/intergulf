#### 

[Project](../../../../index.md) > [(local)\\](../../../index.md) > [User databases](../../index.md) > [Intergulf](../index.md) > [Views](Views.md) > dbo.vwSelectProfilesWithErrors

# ![Views](../../../../Images/View32.png) [dbo].[vwSelectProfilesWithErrors]

---

## <a name="#properties"></a>Properties

| Property | Value |
|---|---|
| Collation | SQL_Latin1_General_CP1_CI_AS |
| ANSI Nulls On | YES |
| Quoted Identifier On | YES |
| Created | 11:16:21 PM Monday, December 17, 2012 |
| Last Modified | 2:05:38 PM Sunday, January 25, 2015 |


---

## <a name="#columns"></a>Columns

| Name | Data Type | Max Length (Bytes) |
|---|---|---|
| ProfileId | bigint | 8 |
| MaterialCodeId | int | 4 |
| MaterialCode | nvarchar(50) | 100 |
| FunctionProperShippingName | varchar(5000) | 5000 |
| ShippingName | varchar(1000) | 1000 |
| ProblemDescription | varchar(3000) | 3000 |


---

## <a name="#sqlscript"></a>SQL Script

```sql

CREATE VIEW [dbo].[vwSelectProfilesWithErrors]
AS
SELECT     dbo.ProfilesWithErrors.ProfileId, dbo.Profile.MaterialCodeId, dbo.MaterialCode.MaterialCode, 
                      dbo.fnProperShippingName(dbo.Profile.MaterialCodeId) AS FunctionProperShippingName, dbo.Profile.ShippingName, 
                      dbo.ProfilesWithErrors.ProblemDescription
FROM         dbo.MaterialCode INNER JOIN
                      dbo.Profile ON dbo.MaterialCode.ID = dbo.Profile.MaterialCodeId RIGHT OUTER JOIN
                      dbo.ProfilesWithErrors ON dbo.Profile.Id = dbo.ProfilesWithErrors.ProfileId

GO

```


---

## <a name="#uses"></a>Uses

* [[dbo].[MaterialCode]](../Tables/dbo_MaterialCode.md)
* [[dbo].[Profile]](../Tables/dbo_Profile.md)
* [[dbo].[ProfilesWithErrors]](../Tables/dbo_ProfilesWithErrors.md)
* [[dbo].[fnProperShippingName]](../Programmability/Functions/Scalar-valued_Functions/dbo_fnProperShippingName.md)


---

###### Author:  Sastry

###### Copyright 2023 - All Rights Reserved

###### Created: Thursday, October 5, 2023 9:55:17 PM

