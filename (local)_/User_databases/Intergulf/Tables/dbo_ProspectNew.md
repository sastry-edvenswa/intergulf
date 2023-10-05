#### 

[Project](../../../../index.md) > [(local)\\](../../../index.md) > [User databases](../../index.md) > [Intergulf](../index.md) > [Tables](Tables.md) > dbo.ProspectNew

# ![Tables](../../../../Images/Table32.png) [dbo].[ProspectNew]

---

## <a name="#properties"></a>Properties

| Property | Value |
|---|---|
| Collation | SQL_Latin1_General_CP1_CI_AS |
| Heap | YES |
| Row Count (~) | 3883 |
| Created | 6:47:37 PM Monday, January 29, 2007 |
| Last Modified | 6:47:37 PM Monday, January 29, 2007 |


---

## <a name="#columns"></a>Columns

| Name | Data Type | Max Length (Bytes) | Nullability |
|---|---|---|---|
| refinery list for us as of 05 | nvarchar(255) | 510 | NULL allowed |
| PERIOD | nvarchar(255) | 510 | NULL allowed |
| COMPANY_NAME | nvarchar(255) | 510 | NULL allowed |
| STATE | nvarchar(255) | 510 | NULL allowed |
| SITE | nvarchar(255) | 510 | NULL allowed |
| PADD | nvarchar(255) | 510 | NULL allowed |
| PRODUCT | nvarchar(255) | 510 | NULL allowed |
| SUPPLY | nvarchar(255) | 510 | NULL allowed |
| QUANTITY | float | 8 | NULL allowed |


---

## <a name="#sqlscript"></a>SQL Script

```sql
CREATE TABLE [dbo].[ProspectNew]
(
[refinery list for us as of 05] [nvarchar] (255) COLLATE SQL_Latin1_General_CP1_CI_AS NULL,
[PERIOD] [nvarchar] (255) COLLATE SQL_Latin1_General_CP1_CI_AS NULL,
[COMPANY_NAME] [nvarchar] (255) COLLATE SQL_Latin1_General_CP1_CI_AS NULL,
[STATE] [nvarchar] (255) COLLATE SQL_Latin1_General_CP1_CI_AS NULL,
[SITE] [nvarchar] (255) COLLATE SQL_Latin1_General_CP1_CI_AS NULL,
[PADD] [nvarchar] (255) COLLATE SQL_Latin1_General_CP1_CI_AS NULL,
[PRODUCT] [nvarchar] (255) COLLATE SQL_Latin1_General_CP1_CI_AS NULL,
[SUPPLY] [nvarchar] (255) COLLATE SQL_Latin1_General_CP1_CI_AS NULL,
[QUANTITY] [float] NULL
) ON [PRIMARY]
GO

```


---

###### Author:  Sastry

###### Copyright 2023 - All Rights Reserved

###### Created: Thursday, October 5, 2023 9:55:17 PM

