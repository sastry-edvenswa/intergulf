#### 

[Project](../../../../index.md) > [(local)\\](../../../index.md) > [User databases](../../index.md) > [Intergulf](../index.md) > [Views](Views.md) > dbo.vwSelectProfilePOInformation

# ![Views](../../../../Images/View32.png) [dbo].[vwSelectProfilePOInformation]

---

## <a name="#properties"></a>Properties

| Property | Value |
|---|---|
| Collation | SQL_Latin1_General_CP1_CI_AS |
| ANSI Nulls On | YES |
| Quoted Identifier On | YES |
| Created | 7:44:10 PM Sunday, February 28, 2021 |
| Last Modified | 7:44:10 PM Sunday, February 28, 2021 |


---

## <a name="#columns"></a>Columns

| Name | Data Type | Max Length (Bytes) | Identity |
|---|---|---|---|
| Id | bigint | 8 | 0 - 0 |
| PoNumber | varchar(50) | 50 |  |
| PoNumberExpirationDate | date | 3 |  |


---

## <a name="#sqlscript"></a>SQL Script

```sql
CREATE VIEW [dbo].[vwSelectProfilePOInformation]
AS
SELECT        Id, PoNumber, PoNumberExpirationDate
FROM            dbo.Profile
GO

```


---

## <a name="#uses"></a>Uses

* [[dbo].[Profile]](../Tables/dbo_Profile.md)


---

###### Author:  Sastry

###### Copyright 2023 - All Rights Reserved

###### Created: Thursday, October 5, 2023 9:55:17 PM

