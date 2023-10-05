#### 

[Project](../../../../index.md) > [(local)\\](../../../index.md) > [User databases](../../index.md) > [Intergulf](../index.md) > [Views](Views.md) > dbo.vwSelectLoadRequestProfileMaterialCode

# ![Views](../../../../Images/View32.png) [dbo].[vwSelectLoadRequestProfileMaterialCode]

---

## <a name="#properties"></a>Properties

| Property | Value |
|---|---|
| Collation | SQL_Latin1_General_CP1_CI_AS |
| ANSI Nulls On | YES |
| Quoted Identifier On | YES |
| Created | 11:17:17 PM Monday, December 17, 2012 |
| Last Modified | 2:05:38 PM Sunday, January 25, 2015 |


---

## <a name="#columns"></a>Columns

| Name | Data Type | Max Length (Bytes) |
|---|---|---|
| Id | bigint | 8 |
| MaterialCodeId | int | 4 |
| ProfileNumber | varchar(50) | 50 |
| SalespersonName | varchar(101) | 101 |


---

## <a name="#sqlscript"></a>SQL Script

```sql

CREATE VIEW [dbo].[vwSelectLoadRequestProfileMaterialCode]
AS
SELECT     dbo.LoadRequest.Id, dbo.Profile.MaterialCodeId, dbo.Profile.ProfileNumber, 
                      RTRIM(LTRIM(dbo.UserMaster.FirstName + ' ' + dbo.UserMaster.LastName)) AS SalespersonName
FROM         dbo.UserMaster INNER JOIN
                      dbo.Profile ON dbo.UserMaster.UserName = dbo.Profile.SalesPersonId RIGHT OUTER JOIN
                      dbo.LoadRequest ON dbo.Profile.Id = dbo.LoadRequest.ProfileId

GO

```


---

## <a name="#uses"></a>Uses

* [[dbo].[LoadRequest]](../Tables/dbo_LoadRequest.md)
* [[dbo].[Profile]](../Tables/dbo_Profile.md)
* [[dbo].[UserMaster]](../Tables/dbo_UserMaster.md)


---

###### Author:  Sastry

###### Copyright 2023 - All Rights Reserved

###### Created: Thursday, October 5, 2023 9:55:17 PM

