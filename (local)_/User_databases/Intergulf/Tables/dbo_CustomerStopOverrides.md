#### 

[Project](../../../../index.md) > [(local)\\](../../../index.md) > [User databases](../../index.md) > [Intergulf](../index.md) > [Tables](Tables.md) > dbo.CustomerStopOverrides

# ![Tables](../../../../Images/Table32.png) [dbo].[CustomerStopOverrides]

---

## <a name="#properties"></a>Properties

| Property | Value |
|---|---|
| Collation | SQL_Latin1_General_CP1_CI_AS |
| Row Count (~) | 246 |
| Created | 5:59:40 PM Sunday, April 30, 2017 |
| Last Modified | 5:59:40 PM Sunday, April 30, 2017 |


---

## <a name="#columns"></a>Columns

| Key | Name | Data Type | Max Length (Bytes) | Nullability | Identity |
|---|---|---|---|---|---|
| [![Cluster Primary Key PK_CustomerStopOverrides: Id](../../../../Images/pkcluster.png)](#indexes) | Id | bigint | 8 | NOT NULL | 1 - 1 |
|  | TableName | varchar(50) | 50 | NULL allowed |  |
|  | TableKey | bigint | 8 | NULL allowed |  |
|  | OverrideUser | varchar(50) | 50 | NULL allowed |  |
|  | OverrideDateTime | datetime | 8 | NULL allowed |  |


---

## <a name="#indexes"></a>Indexes

| Key | Name | Key Columns | Unique |
|---|---|---|---|
| [![Cluster Primary Key PK_CustomerStopOverrides: Id](../../../../Images/pkcluster.png)](#indexes) | PK_CustomerStopOverrides | Id | YES |


---

## <a name="#sqlscript"></a>SQL Script

```sql
CREATE TABLE [dbo].[CustomerStopOverrides]
(
[Id] [bigint] NOT NULL IDENTITY(1, 1),
[TableName] [varchar] (50) COLLATE SQL_Latin1_General_CP1_CI_AS NULL,
[TableKey] [bigint] NULL,
[OverrideUser] [varchar] (50) COLLATE SQL_Latin1_General_CP1_CI_AS NULL,
[OverrideDateTime] [datetime] NULL
) ON [PRIMARY]
GO
ALTER TABLE [dbo].[CustomerStopOverrides] ADD CONSTRAINT [PK_CustomerStopOverrides] PRIMARY KEY CLUSTERED ([Id]) ON [PRIMARY]
GO

```


---

###### Author:  Sastry

###### Copyright 2023 - All Rights Reserved

###### Created: Thursday, October 5, 2023 9:55:17 PM

