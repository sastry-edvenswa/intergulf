#### 

[Project](../../../../index.md) > [(local)\\](../../../index.md) > [User databases](../../index.md) > [Intergulf](../index.md) > [Tables](Tables.md) > dbo.Counters

# ![Tables](../../../../Images/Table32.png) [dbo].[Counters]

---

## <a name="#properties"></a>Properties

| Property | Value |
|---|---|
| Collation | SQL_Latin1_General_CP1_CI_AS |
| Row Count (~) | 5 |
| Created | 6:47:33 PM Monday, January 29, 2007 |
| Last Modified | 11:50:36 AM Sunday, January 15, 2017 |


---

## <a name="#columns"></a>Columns

| Key | Name | Data Type | Max Length (Bytes) | Nullability |
|---|---|---|---|---|
| [![Cluster Primary Key PK_Counters: TableName](../../../../Images/pkcluster.png)](#indexes) | TableName | char(50) | 50 | NOT NULL |
|  | Id | bigint | 8 | NULL allowed |


---

## <a name="#indexes"></a>Indexes

| Key | Name | Key Columns | Unique |
|---|---|---|---|
| [![Cluster Primary Key PK_Counters: TableName](../../../../Images/pkcluster.png)](#indexes) | PK_Counters | TableName | YES |


---

## <a name="#sqlscript"></a>SQL Script

```sql
CREATE TABLE [dbo].[Counters]
(
[TableName] [char] (50) COLLATE SQL_Latin1_General_CP1_CI_AS NOT NULL,
[Id] [bigint] NULL
) ON [PRIMARY]
GO
ALTER TABLE [dbo].[Counters] ADD CONSTRAINT [PK_Counters] PRIMARY KEY CLUSTERED ([TableName]) ON [PRIMARY]
GO

```


---

## <a name="#usedby"></a>Used By

* [[dbo].[fnSelectCounters]](../Programmability/Functions/Table-valued_Functions/dbo_fnSelectCounters.md)


---

###### Author:  Sastry

###### Copyright 2023 - All Rights Reserved

###### Created: Thursday, October 5, 2023 9:55:17 PM

