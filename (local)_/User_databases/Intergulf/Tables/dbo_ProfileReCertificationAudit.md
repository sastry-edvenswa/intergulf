#### 

[Project](../../../../index.md) > [(local)\\](../../../index.md) > [User databases](../../index.md) > [Intergulf](../index.md) > [Tables](Tables.md) > dbo.ProfileReCertificationAudit

# ![Tables](../../../../Images/Table32.png) [dbo].[ProfileReCertificationAudit]

---

## <a name="#properties"></a>Properties

| Property | Value |
|---|---|
| Collation | SQL_Latin1_General_CP1_CI_AS |
| Heap | YES |
| Row Count (~) | 1878 |
| Created | 11:29:30 AM Tuesday, March 20, 2012 |
| Last Modified | 11:29:30 AM Tuesday, March 20, 2012 |


---

## <a name="#columns"></a>Columns

| Name | Data Type | Max Length (Bytes) | Nullability | Identity |
|---|---|---|---|---|
| Id | bigint | 8 | NOT NULL | 1 - 1 |
| ProfileId | bigint | 8 | NULL allowed |  |
| SalesPersonId | varchar(50) | 50 | NULL allowed |  |
| OriginalDate | datetime | 8 | NULL allowed |  |
| NewDate | datetime | 8 | NULL allowed |  |
| UpdateUser | varchar(50) | 50 | NULL allowed |  |
| UpdateDateTime | datetime | 8 | NULL allowed |  |
| UpdateComputer | varchar(50) | 50 | NULL allowed |  |


---

## <a name="#sqlscript"></a>SQL Script

```sql
CREATE TABLE [dbo].[ProfileReCertificationAudit]
(
[Id] [bigint] NOT NULL IDENTITY(1, 1),
[ProfileId] [bigint] NULL,
[SalesPersonId] [varchar] (50) COLLATE SQL_Latin1_General_CP1_CI_AS NULL,
[OriginalDate] [datetime] NULL,
[NewDate] [datetime] NULL,
[UpdateUser] [varchar] (50) COLLATE SQL_Latin1_General_CP1_CI_AS NULL,
[UpdateDateTime] [datetime] NULL,
[UpdateComputer] [varchar] (50) COLLATE SQL_Latin1_General_CP1_CI_AS NULL
) ON [PRIMARY]
GO

```


---

###### Author:  Sastry

###### Copyright 2023 - All Rights Reserved

###### Created: Thursday, October 5, 2023 9:55:17 PM

