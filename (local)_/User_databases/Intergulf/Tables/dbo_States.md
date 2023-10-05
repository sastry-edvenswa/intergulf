#### 

[Project](../../../../index.md) > [(local)\\](../../../index.md) > [User databases](../../index.md) > [Intergulf](../index.md) > [Tables](Tables.md) > dbo.States

# ![Tables](../../../../Images/Table32.png) [dbo].[States]

---

## <a name="#properties"></a>Properties

| Property | Value |
|---|---|
| Collation | SQL_Latin1_General_CP1_CI_AS |
| Heap | YES |
| Row Count (~) | 59 |
| Created | 6:47:37 PM Monday, January 29, 2007 |
| Last Modified | 6:47:37 PM Monday, January 29, 2007 |


---

## <a name="#columns"></a>Columns

| Name | Data Type | Max Length (Bytes) | Nullability |
|---|---|---|---|
| State | varchar(50) | 50 | NOT NULL |
| StateName | varchar(50) | 50 | NULL allowed |


---

## <a name="#sqlscript"></a>SQL Script

```sql
CREATE TABLE [dbo].[States]
(
[State] [varchar] (50) COLLATE SQL_Latin1_General_CP1_CI_AS NOT NULL,
[StateName] [varchar] (50) COLLATE SQL_Latin1_General_CP1_CI_AS NULL
) ON [PRIMARY]
GO

```


---

## <a name="#usedby"></a>Used By

* [[dbo].[fnSelectStates]](../Programmability/Functions/Table-valued_Functions/dbo_fnSelectStates.md)


---

###### Author:  Sastry

###### Copyright 2023 - All Rights Reserved

###### Created: Thursday, October 5, 2023 9:55:17 PM

