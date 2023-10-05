#### 

[Project](../../../../index.md) > [(local)\\](../../../index.md) > [User databases](../../index.md) > [Intergulf](../index.md) > [Views](Views.md) > dbo.vwSelectLoadRequestSP

# ![Views](../../../../Images/View32.png) [dbo].[vwSelectLoadRequestSP]

---

## <a name="#properties"></a>Properties

| Property | Value |
|---|---|
| Collation | SQL_Latin1_General_CP1_CI_AS |
| ANSI Nulls On | YES |
| Quoted Identifier On | YES |
| Created | 2:57:07 PM Friday, May 31, 2019 |
| Last Modified | 3:04:22 PM Friday, May 31, 2019 |


---

## <a name="#columns"></a>Columns

| Name | Data Type | Max Length (Bytes) |
|---|---|---|
| Id | bigint | 8 |
| LQSP | varchar(50) | 50 |
| ProfileNumber | varchar(50) | 50 |
| PSP | varchar(50) | 50 |
| Processed | int | 4 |


---

## <a name="#sqlscript"></a>SQL Script

```sql
CREATE VIEW [dbo].[vwSelectLoadRequestSP]
AS
SELECT        dbo.LoadRequest.Id, dbo.LoadRequest.SalesPersonId AS LQSP, dbo.Profile.ProfileNumber, dbo.Profile.SalesPersonId AS PSP, dbo.LoadRequest.Processed
FROM            dbo.LoadRequest LEFT OUTER JOIN
                         dbo.Profile ON dbo.LoadRequest.ProfileId = dbo.Profile.Id
WHERE        (dbo.LoadRequest.Processed = 0) AND (dbo.LoadRequest.SalesPersonId <> dbo.Profile.SalesPersonId)
GO

```


---

## <a name="#uses"></a>Uses

* [[dbo].[LoadRequest]](../Tables/dbo_LoadRequest.md)
* [[dbo].[Profile]](../Tables/dbo_Profile.md)


---

###### Author:  Sastry

###### Copyright 2023 - All Rights Reserved

###### Created: Thursday, October 5, 2023 9:55:17 PM

