#### 

[Project](../../../../index.md) > [(local)\\](../../../index.md) > [User databases](../../index.md) > [Intergulf](../index.md) > [Tables](Tables.md) > dbo.LoadFrequency

# ![Tables](../../../../Images/Table32.png) [dbo].[LoadFrequency]

---

## <a name="#properties"></a>Properties

| Property | Value |
|---|---|
| Collation | SQL_Latin1_General_CP1_CI_AS |
| Row Count (~) | 10 |
| Created | 6:47:34 PM Monday, January 29, 2007 |
| Last Modified | 11:50:40 AM Sunday, January 15, 2017 |


---

## <a name="#columns"></a>Columns

| Key | Name | Data Type | Max Length (Bytes) | Nullability |
|---|---|---|---|---|
| [![Cluster Primary Key PK_LoadFrequency: Description](../../../../Images/pkcluster.png)](#indexes) | Description | varchar(50) | 50 | NOT NULL |


---

## <a name="#indexes"></a>Indexes

| Key | Name | Key Columns | Unique |
|---|---|---|---|
| [![Cluster Primary Key PK_LoadFrequency: Description](../../../../Images/pkcluster.png)](#indexes) | PK_LoadFrequency | Description | YES |


---

## <a name="#sqlscript"></a>SQL Script

```sql
CREATE TABLE [dbo].[LoadFrequency]
(
[Description] [varchar] (50) COLLATE SQL_Latin1_General_CP1_CI_AS NOT NULL
) ON [PRIMARY]
GO
ALTER TABLE [dbo].[LoadFrequency] ADD CONSTRAINT [PK_LoadFrequency] PRIMARY KEY CLUSTERED ([Description]) ON [PRIMARY]
GO

```


---

## <a name="#usedby"></a>Used By

* [[dbo].[fnSelectLoadFrequency]](../Programmability/Functions/Table-valued_Functions/dbo_fnSelectLoadFrequency.md)


---

###### Author:  Sastry

###### Copyright 2023 - All Rights Reserved

###### Created: Thursday, October 5, 2023 9:55:17 PM

