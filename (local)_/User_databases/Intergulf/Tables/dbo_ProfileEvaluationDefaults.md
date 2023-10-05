#### 

[Project](../../../../index.md) > [(local)\\](../../../index.md) > [User databases](../../index.md) > [Intergulf](../index.md) > [Tables](Tables.md) > dbo.ProfileEvaluationDefaults

# ![Tables](../../../../Images/Table32.png) [dbo].[ProfileEvaluationDefaults]

---

## <a name="#properties"></a>Properties

| Property | Value |
|---|---|
| Collation | SQL_Latin1_General_CP1_CI_AS |
| Row Count (~) | 20 |
| Created | 6:47:36 PM Monday, January 29, 2007 |
| Last Modified | 11:50:50 AM Sunday, January 15, 2017 |


---

## <a name="#columns"></a>Columns

| Key | Name | Data Type | Max Length (Bytes) | Nullability | Identity |
|---|---|---|---|---|---|
| [![Cluster Primary Key PK_ProfileEvaluationDefaults: Id](../../../../Images/pkcluster.png)](#indexes) | Id | numeric(18,0) | 9 | NOT NULL | 1 - 1 |
|  | Description | varchar(255) | 255 | NOT NULL |  |
|  | SortOrder | int | 4 | NULL allowed |  |


---

## <a name="#indexes"></a>Indexes

| Key | Name | Key Columns | Unique |
|---|---|---|---|
| [![Cluster Primary Key PK_ProfileEvaluationDefaults: Id](../../../../Images/pkcluster.png)](#indexes) | PK_ProfileEvaluationDefaults | Id | YES |


---

## <a name="#sqlscript"></a>SQL Script

```sql
CREATE TABLE [dbo].[ProfileEvaluationDefaults]
(
[Id] [numeric] (18, 0) NOT NULL IDENTITY(1, 1),
[Description] [varchar] (255) COLLATE SQL_Latin1_General_CP1_CI_AS NOT NULL,
[SortOrder] [int] NULL
) ON [PRIMARY]
GO
ALTER TABLE [dbo].[ProfileEvaluationDefaults] ADD CONSTRAINT [PK_ProfileEvaluationDefaults] PRIMARY KEY CLUSTERED ([Id]) ON [PRIMARY]
GO

```


---

###### Author:  Sastry

###### Copyright 2023 - All Rights Reserved

###### Created: Thursday, October 5, 2023 9:55:17 PM

