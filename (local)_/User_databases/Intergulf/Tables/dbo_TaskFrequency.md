#### 

[Project](../../../../index.md) > [(local)\\](../../../index.md) > [User databases](../../index.md) > [Intergulf](../index.md) > [Tables](Tables.md) > dbo.TaskFrequency

# ![Tables](../../../../Images/Table32.png) [dbo].[TaskFrequency]

---

## <a name="#properties"></a>Properties

| Property | Value |
|---|---|
| Collation | SQL_Latin1_General_CP1_CI_AS |
| Row Count (~) | 5 |
| Created | 10:09:14 PM Sunday, September 17, 2017 |
| Last Modified | 10:09:14 PM Sunday, September 17, 2017 |


---

## <a name="#columns"></a>Columns

| Key | Name | Data Type | Max Length (Bytes) | Nullability |
|---|---|---|---|---|
| [![Cluster Primary Key PK_Frequency: Frequency](../../../../Images/pkcluster.png)](#indexes) | Frequency | varchar(50) | 50 | NOT NULL |
|  | SortOrder | int | 4 | NULL allowed |


---

## <a name="#indexes"></a>Indexes

| Key | Name | Key Columns | Unique |
|---|---|---|---|
| [![Cluster Primary Key PK_Frequency: Frequency](../../../../Images/pkcluster.png)](#indexes) | PK_Frequency | Frequency | YES |


---

## <a name="#sqlscript"></a>SQL Script

```sql
CREATE TABLE [dbo].[TaskFrequency]
(
[Frequency] [varchar] (50) COLLATE SQL_Latin1_General_CP1_CI_AS NOT NULL,
[SortOrder] [int] NULL
) ON [PRIMARY]
GO
ALTER TABLE [dbo].[TaskFrequency] ADD CONSTRAINT [PK_Frequency] PRIMARY KEY CLUSTERED ([Frequency]) ON [PRIMARY]
GO

```


---

## <a name="#usedby"></a>Used By

* [[dbo].[vwSelectTasks]](../Views/dbo_vwSelectTasks.md)


---

###### Author:  Sastry

###### Copyright 2023 - All Rights Reserved

###### Created: Thursday, October 5, 2023 9:55:17 PM

