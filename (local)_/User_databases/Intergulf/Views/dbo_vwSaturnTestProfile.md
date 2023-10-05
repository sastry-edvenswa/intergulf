#### 

[Project](../../../../index.md) > [(local)\\](../../../index.md) > [User databases](../../index.md) > [Intergulf](../index.md) > [Views](Views.md) > dbo.vwSaturnTestProfile

# ![Views](../../../../Images/View32.png) [dbo].[vwSaturnTestProfile]

---

## <a name="#properties"></a>Properties

| Property | Value |
|---|---|
| Collation | SQL_Latin1_General_CP1_CI_AS |
| ANSI Nulls On | YES |
| Quoted Identifier On | YES |
| Created | 3:18:05 PM Thursday, February 16, 2023 |
| Last Modified | 3:18:05 PM Thursday, February 16, 2023 |


---

## <a name="#columns"></a>Columns

| Name | Data Type | Max Length (Bytes) | Identity |
|---|---|---|---|
| Id | bigint | 8 | 0 - 0 |
| ProfileNumber | varchar(50) | 50 |  |
| ContractNumber | varchar(20) | 20 |  |
| VendorId | bigint | 8 |  |
| Product | varchar(20) | 20 |  |


---

## <a name="#sqlscript"></a>SQL Script

```sql
CREATE VIEW [dbo].[vwSaturnTestProfile]
AS
SELECT        Id, ProfileNumber, ContractNumber, VendorId, Product
FROM            dbo.Profile
WHERE        (ProfileNumber = '01207')
GO

```


---

## <a name="#uses"></a>Uses

* [[dbo].[Profile]](../Tables/dbo_Profile.md)


---

###### Author:  Sastry

###### Copyright 2023 - All Rights Reserved

###### Created: Thursday, October 5, 2023 9:55:17 PM

