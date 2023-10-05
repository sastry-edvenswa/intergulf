#### 

[Project](../../../../index.md) > [(local)\\](../../../index.md) > [User databases](../../index.md) > [Intergulf](../index.md) > [Views](Views.md) > dbo.vwSelectOutgoingEmailsForProfile07888

# ![Views](../../../../Images/View32.png) [dbo].[vwSelectOutgoingEmailsForProfile07888]

---

## <a name="#properties"></a>Properties

| Property | Value |
|---|---|
| Collation | SQL_Latin1_General_CP1_CI_AS |
| ANSI Nulls On | YES |
| Quoted Identifier On | YES |
| Created | 5:04:10 PM Friday, August 11, 2017 |
| Last Modified | 1:36:37 PM Monday, April 29, 2019 |


---

## <a name="#columns"></a>Columns

| Name | Data Type | Max Length (Bytes) | Identity |
|---|---|---|---|
| Id | bigint | 8 | 0 - 0 |
| Subject | varchar(500) | 500 |  |
| Body | varchar(3000) | 3000 |  |
| WhoTo | varchar(50) | 50 |  |
| WhoFrom | varchar(50) | 50 |  |
| Importance | int | 4 |  |
| Sent | int | 4 |  |
| UpdateDateTime | datetime | 8 |  |
| UpdateUser | varchar(50) | 50 |  |
| UpdateComputer | varchar(50) | 50 |  |


---

## <a name="#sqlscript"></a>SQL Script

```sql
CREATE VIEW [dbo].[vwSelectOutgoingEmailsForProfile07888]
AS
SELECT        TOP (100) PERCENT Id, Subject, Body, WhoTo, WhoFrom, Importance, Sent, UpdateDateTime, UpdateUser, UpdateComputer
FROM            dbo.OutGoingEmails
WHERE        (UpdateDateTime > CONVERT(DATETIME, '2019-04-26 00:00:00', 102))
ORDER BY UpdateDateTime
GO

```


---

## <a name="#uses"></a>Uses

* [[dbo].[OutGoingEmails]](../Tables/dbo_OutGoingEmails.md)


---

###### Author:  Sastry

###### Copyright 2023 - All Rights Reserved

###### Created: Thursday, October 5, 2023 9:55:17 PM

