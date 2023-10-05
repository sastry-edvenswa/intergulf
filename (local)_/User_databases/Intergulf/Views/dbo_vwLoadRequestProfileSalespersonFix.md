#### 

[Project](../../../../index.md) > [(local)\\](../../../index.md) > [User databases](../../index.md) > [Intergulf](../index.md) > [Views](Views.md) > dbo.vwLoadRequestProfileSalespersonFix

# ![Views](../../../../Images/View32.png) [dbo].[vwLoadRequestProfileSalespersonFix]

---

## <a name="#properties"></a>Properties

| Property | Value |
|---|---|
| Collation | SQL_Latin1_General_CP1_CI_AS |
| ANSI Nulls On | YES |
| Quoted Identifier On | YES |
| Created | 8:10:06 PM Monday, September 23, 2019 |
| Last Modified | 8:10:06 PM Monday, September 23, 2019 |


---

## <a name="#columns"></a>Columns

| Name | Data Type | Max Length (Bytes) |
|---|---|---|
| Id | bigint | 8 |
| ProfileId | bigint | 8 |
| ProfileNumber | varchar(50) | 50 |
| LR Salesperson | varchar(50) | 50 |
| P Salesperson | varchar(50) | 50 |
| Processed | int | 4 |


---

## <a name="#sqlscript"></a>SQL Script

```sql
CREATE VIEW [dbo].[vwLoadRequestProfileSalespersonFix]
AS
SELECT        dbo.LoadRequest.Id, dbo.LoadRequest.ProfileId, dbo.Profile.ProfileNumber, dbo.LoadRequest.SalesPersonId AS [LR Salesperson], dbo.Profile.SalesPersonId AS [P Salesperson], 
                         dbo.LoadRequest.Processed
FROM            dbo.LoadRequest LEFT OUTER JOIN
                         dbo.Profile ON dbo.LoadRequest.ProfileId = dbo.Profile.Id
WHERE        (dbo.LoadRequest.SalesPersonId <> dbo.Profile.SalesPersonId) AND (dbo.LoadRequest.Processed = 0)
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

