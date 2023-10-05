#### 

[Project](../../../../index.md) > [(local)\\](../../../index.md) > [User databases](../../index.md) > [Intergulf](../index.md) > [Tables](Tables.md) > dbo.ProspectList2

# ![Tables](../../../../Images/Table32.png) [dbo].[ProspectList2]

---

## <a name="#properties"></a>Properties

| Property | Value |
|---|---|
| Collation | SQL_Latin1_General_CP1_CI_AS |
| Heap | YES |
| Row Count (~) | 7796 |
| Created | 6:47:37 PM Monday, January 29, 2007 |
| Last Modified | 6:47:37 PM Monday, January 29, 2007 |


---

## <a name="#columns"></a>Columns

| Name | Data Type | Max Length (Bytes) | Nullability |
|---|---|---|---|
| FRL | nvarchar(20) | 40 | NULL allowed |
| CITATION | nvarchar(32) | 64 | NULL allowed |
| CAS | nvarchar(31) | 62 | NULL allowed |
| PMN | nvarchar(32) | 64 | NULL allowed |
| NAME | nvarchar(160) | 320 | NULL allowed |
| SECTION | nvarchar(52) | 104 | NULL allowed |
| 5E_DATE | smalldatetime | 4 | NULL allowed |


---

## <a name="#sqlscript"></a>SQL Script

```sql
CREATE TABLE [dbo].[ProspectList2]
(
[FRL] [nvarchar] (20) COLLATE SQL_Latin1_General_CP1_CI_AS NULL,
[CITATION] [nvarchar] (32) COLLATE SQL_Latin1_General_CP1_CI_AS NULL,
[CAS] [nvarchar] (31) COLLATE SQL_Latin1_General_CP1_CI_AS NULL,
[PMN] [nvarchar] (32) COLLATE SQL_Latin1_General_CP1_CI_AS NULL,
[NAME] [nvarchar] (160) COLLATE SQL_Latin1_General_CP1_CI_AS NULL,
[SECTION] [nvarchar] (52) COLLATE SQL_Latin1_General_CP1_CI_AS NULL,
[5E_DATE] [smalldatetime] NULL
) ON [PRIMARY]
GO

```


---

###### Author:  Sastry

###### Copyright 2023 - All Rights Reserved

###### Created: Thursday, October 5, 2023 9:55:17 PM

