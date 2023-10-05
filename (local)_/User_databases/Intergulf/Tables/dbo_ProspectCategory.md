#### 

[Project](../../../../index.md) > [(local)\\](../../../index.md) > [User databases](../../index.md) > [Intergulf](../index.md) > [Tables](Tables.md) > dbo.ProspectCategory

# ![Tables](../../../../Images/Table32.png) [dbo].[ProspectCategory]

---

## <a name="#properties"></a>Properties

| Property | Value |
|---|---|
| Collation | SQL_Latin1_General_CP1_CI_AS |
| Row Count (~) | 8 |
| Created | 6:47:36 PM Monday, January 29, 2007 |
| Last Modified | 11:50:50 AM Sunday, January 15, 2017 |


---

## <a name="#columns"></a>Columns

| Key | Name | Data Type | Max Length (Bytes) | Nullability | Identity |
|---|---|---|---|---|---|
| [![Cluster Primary Key PK_ProspectClassification: Id](../../../../Images/pkcluster.png)](#indexes) | Id | numeric(18,0) | 9 | NOT NULL | 1 - 1 |
|  | Name | varchar(50) | 50 | NULL allowed |  |


---

## <a name="#indexes"></a>Indexes

| Key | Name | Key Columns | Unique |
|---|---|---|---|
| [![Cluster Primary Key PK_ProspectClassification: Id](../../../../Images/pkcluster.png)](#indexes) | PK_ProspectClassification | Id | YES |


---

## <a name="#sqlscript"></a>SQL Script

```sql
CREATE TABLE [dbo].[ProspectCategory]
(
[Id] [numeric] (18, 0) NOT NULL IDENTITY(1, 1),
[Name] [varchar] (50) COLLATE SQL_Latin1_General_CP1_CI_AS NULL
) ON [PRIMARY]
GO
ALTER TABLE [dbo].[ProspectCategory] ADD CONSTRAINT [PK_ProspectClassification] PRIMARY KEY CLUSTERED ([Id]) ON [PRIMARY]
GO

```


---

## <a name="#usedby"></a>Used By

* [[dbo].[vwRptProspectContactByName]](../Views/dbo_vwRptProspectContactByName.md)
* [[dbo].[vwSelectProspectContact]](../Views/dbo_vwSelectProspectContact.md)


---

###### Author:  Sastry

###### Copyright 2023 - All Rights Reserved

###### Created: Thursday, October 5, 2023 9:55:17 PM

