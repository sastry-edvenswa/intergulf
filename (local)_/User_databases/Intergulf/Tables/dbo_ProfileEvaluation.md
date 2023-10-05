#### 

[Project](../../../../index.md) > [(local)\\](../../../index.md) > [User databases](../../index.md) > [Intergulf](../index.md) > [Tables](Tables.md) > dbo.ProfileEvaluation

# ![Tables](../../../../Images/Table32.png) [dbo].[ProfileEvaluation]

---

## <a name="#properties"></a>Properties

| Property | Value |
|---|---|
| Collation | SQL_Latin1_General_CP1_CI_AS |
| Row Count (~) | 100 |
| Created | 6:47:36 PM Monday, January 29, 2007 |
| Last Modified | 11:50:50 AM Sunday, January 15, 2017 |


---

## <a name="#columns"></a>Columns

| Key | Name | Data Type | Max Length (Bytes) | Nullability | Identity |
|---|---|---|---|---|---|
| [![Cluster Primary Key PK_ProfileEvaluation: Id](../../../../Images/pkcluster.png)](#indexes) | Id | numeric(18,0) | 9 | NOT NULL | 1 - 1 |
|  | CustomerId | varchar(50) | 50 | NULL allowed |  |
|  | GeneratorId | varchar(50) | 50 | NULL allowed |  |
|  | ProfileId | varchar(50) | 50 | NULL allowed |  |
|  | YesNo | int | 4 | NULL allowed |  |
|  | PK | int | 4 | NULL allowed |  |
|  | AD | int | 4 | NULL allowed |  |
|  | DescriptionId | numeric(18,0) | 9 | NULL allowed |  |
|  | SortOrder | int | 4 | NULL allowed |  |


---

## <a name="#indexes"></a>Indexes

| Key | Name | Key Columns | Unique |
|---|---|---|---|
| [![Cluster Primary Key PK_ProfileEvaluation: Id](../../../../Images/pkcluster.png)](#indexes) | PK_ProfileEvaluation | Id | YES |


---

## <a name="#sqlscript"></a>SQL Script

```sql
CREATE TABLE [dbo].[ProfileEvaluation]
(
[Id] [numeric] (18, 0) NOT NULL IDENTITY(1, 1),
[CustomerId] [varchar] (50) COLLATE SQL_Latin1_General_CP1_CI_AS NULL,
[GeneratorId] [varchar] (50) COLLATE SQL_Latin1_General_CP1_CI_AS NULL,
[ProfileId] [varchar] (50) COLLATE SQL_Latin1_General_CP1_CI_AS NULL,
[YesNo] [int] NULL,
[PK] [int] NULL,
[AD] [int] NULL,
[DescriptionId] [numeric] (18, 0) NULL,
[SortOrder] [int] NULL
) ON [PRIMARY]
GO
ALTER TABLE [dbo].[ProfileEvaluation] ADD CONSTRAINT [PK_ProfileEvaluation] PRIMARY KEY CLUSTERED ([Id]) ON [PRIMARY]
GO

```


---

## <a name="#usedby"></a>Used By

* [[dbo].[fnSelectProfileEvaluation]](../Programmability/Functions/Table-valued_Functions/dbo_fnSelectProfileEvaluation.md)


---

###### Author:  Sastry

###### Copyright 2023 - All Rights Reserved

###### Created: Thursday, October 5, 2023 9:55:17 PM

