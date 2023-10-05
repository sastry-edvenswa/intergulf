#### 

[Project](../../../../index.md) > [(local)\\](../../../index.md) > [User databases](../../index.md) > [Intergulf](../index.md) > [Tables](Tables.md) > dbo.ProspectList1

# ![Tables](../../../../Images/Table32.png) [dbo].[ProspectList1]

---

## <a name="#properties"></a>Properties

| Property | Value |
|---|---|
| Collation | SQL_Latin1_General_CP1_CI_AS |
| Heap | YES |
| Row Count (~) | 2151 |
| Created | 6:47:37 PM Monday, January 29, 2007 |
| Last Modified | 6:47:37 PM Monday, January 29, 2007 |


---

## <a name="#columns"></a>Columns

| Name | Data Type | Max Length (Bytes) | Nullability |
|---|---|---|---|
| Case Number | nvarchar(10) | 20 | NULL allowed |
| Accession Number | nvarchar(10) | 20 | NULL allowed |
| Generic Name | ntext | max | NULL allowed |
| EPA Inventory Flag | nvarchar(20) | 40 | NULL allowed |


---

## <a name="#sqlscript"></a>SQL Script

```sql
CREATE TABLE [dbo].[ProspectList1]
(
[Case Number] [nvarchar] (10) COLLATE SQL_Latin1_General_CP1_CI_AS NULL,
[Accession Number] [nvarchar] (10) COLLATE SQL_Latin1_General_CP1_CI_AS NULL,
[Generic Name] [ntext] COLLATE SQL_Latin1_General_CP1_CI_AS NULL,
[EPA Inventory Flag] [nvarchar] (20) COLLATE SQL_Latin1_General_CP1_CI_AS NULL
) ON [PRIMARY]
GO

```


---

###### Author:  Sastry

###### Copyright 2023 - All Rights Reserved

###### Created: Thursday, October 5, 2023 9:55:17 PM

