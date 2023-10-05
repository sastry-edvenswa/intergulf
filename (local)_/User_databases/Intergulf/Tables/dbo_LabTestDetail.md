#### 

[Project](../../../../index.md) > [(local)\\](../../../index.md) > [User databases](../../index.md) > [Intergulf](../index.md) > [Tables](Tables.md) > dbo.LabTestDetail

# ![Tables](../../../../Images/Table32.png) [dbo].[LabTestDetail]

---

## <a name="#properties"></a>Properties

| Property | Value |
|---|---|
| Collation | SQL_Latin1_General_CP1_CI_AS |
| Row Count (~) | 162 |
| Created | 6:47:34 PM Monday, January 29, 2007 |
| Last Modified | 11:50:39 AM Sunday, January 15, 2017 |


---

## <a name="#columns"></a>Columns

| Key | Name | Data Type | Max Length (Bytes) | Nullability | Identity |
|---|---|---|---|---|---|
| [![Cluster Primary Key PK_LabTestDetail: Id\LabTestId\Phase](../../../../Images/pkcluster.png)](#indexes) | Id | bigint | 8 | NOT NULL | 1 - 1 |
| [![Cluster Primary Key PK_LabTestDetail: Id\LabTestId\Phase](../../../../Images/pkcluster.png)](#indexes) | LabTestId | bigint | 8 | NOT NULL |  |
| [![Cluster Primary Key PK_LabTestDetail: Id\LabTestId\Phase](../../../../Images/pkcluster.png)](#indexes) | Phase | varchar(50) | 50 | NOT NULL |  |
|  | Metal | varchar(50) | 50 | NULL allowed |  |
|  | Quantity | numeric(18,2) | 9 | NULL allowed |  |


---

## <a name="#indexes"></a>Indexes

| Key | Name | Key Columns | Unique |
|---|---|---|---|
| [![Cluster Primary Key PK_LabTestDetail: Id\LabTestId\Phase](../../../../Images/pkcluster.png)](#indexes) | PK_LabTestDetail | Id, LabTestId, Phase | YES |


---

## <a name="#sqlscript"></a>SQL Script

```sql
CREATE TABLE [dbo].[LabTestDetail]
(
[Id] [bigint] NOT NULL IDENTITY(1, 1),
[LabTestId] [bigint] NOT NULL,
[Phase] [varchar] (50) COLLATE SQL_Latin1_General_CP1_CI_AS NOT NULL,
[Metal] [varchar] (50) COLLATE SQL_Latin1_General_CP1_CI_AS NULL,
[Quantity] [numeric] (18, 2) NULL
) ON [PRIMARY]
GO
ALTER TABLE [dbo].[LabTestDetail] ADD CONSTRAINT [PK_LabTestDetail] PRIMARY KEY CLUSTERED ([Id], [LabTestId], [Phase]) ON [PRIMARY]
GO

```


---

## <a name="#usedby"></a>Used By

* [[dbo].[vwRptLabTestFormDetail]](../Views/dbo_vwRptLabTestFormDetail.md)


---

###### Author:  Sastry

###### Copyright 2023 - All Rights Reserved

###### Created: Thursday, October 5, 2023 9:55:17 PM

