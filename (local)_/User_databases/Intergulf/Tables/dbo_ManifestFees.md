#### 

[Project](../../../../index.md) > [(local)\\](../../../index.md) > [User databases](../../index.md) > [Intergulf](../index.md) > [Tables](Tables.md) > dbo.ManifestFees

# ![Tables](../../../../Images/Table32.png) [dbo].[ManifestFees]

---

## <a name="#properties"></a>Properties

| Property | Value |
|---|---|
| Collation | SQL_Latin1_General_CP1_CI_AS |
| Row Count (~) | 2 |
| Created | 6:24:12 PM Saturday, April 18, 2020 |
| Last Modified | 6:24:12 PM Saturday, April 18, 2020 |


---

## <a name="#columns"></a>Columns

| Key | Name | Data Type | Max Length (Bytes) | Nullability |
|---|---|---|---|---|
| [![Cluster Primary Key PK_ManifestFees: Id](../../../../Images/pkcluster.png)](#indexes) | Id | varchar(50) | 50 | NOT NULL |
|  | Fee | numeric(18,2) | 9 | NULL allowed |


---

## <a name="#indexes"></a>Indexes

| Key | Name | Key Columns | Unique |
|---|---|---|---|
| [![Cluster Primary Key PK_ManifestFees: Id](../../../../Images/pkcluster.png)](#indexes) | PK_ManifestFees | Id | YES |


---

## <a name="#sqlscript"></a>SQL Script

```sql
CREATE TABLE [dbo].[ManifestFees]
(
[Id] [varchar] (50) COLLATE SQL_Latin1_General_CP1_CI_AS NOT NULL,
[Fee] [numeric] (18, 2) NULL
) ON [PRIMARY]
GO
ALTER TABLE [dbo].[ManifestFees] ADD CONSTRAINT [PK_ManifestFees] PRIMARY KEY CLUSTERED ([Id]) ON [PRIMARY]
GO

```


---

## <a name="#usedby"></a>Used By

* [[dbo].[vwSelectProfileManifestFee]](../Views/dbo_vwSelectProfileManifestFee.md)


---

###### Author:  Sastry

###### Copyright 2023 - All Rights Reserved

###### Created: Thursday, October 5, 2023 9:55:17 PM

