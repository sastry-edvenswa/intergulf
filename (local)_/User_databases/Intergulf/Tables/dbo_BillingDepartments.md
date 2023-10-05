#### 

[Project](../../../../index.md) > [(local)\\](../../../index.md) > [User databases](../../index.md) > [Intergulf](../index.md) > [Tables](Tables.md) > dbo.BillingDepartments

# ![Tables](../../../../Images/Table32.png) [dbo].[BillingDepartments]

---

## <a name="#properties"></a>Properties

| Property | Value |
|---|---|
| Collation | SQL_Latin1_General_CP1_CI_AS |
| Row Count (~) | 44 |
| Created | 9:34:38 PM Wednesday, November 4, 2009 |
| Last Modified | 1:45:47 PM Thursday, January 16, 2020 |


---

## <a name="#columns"></a>Columns

| Key | Name | Data Type | Max Length (Bytes) | Nullability |
|---|---|---|---|---|
| [![Cluster Primary Key PK_BillingCode: Description](../../../../Images/pkcluster.png)](#indexes) | Description | varchar(200) | 200 | NOT NULL |
|  | SortOrder | bigint | 8 | NULL allowed |
|  | ServiceTypeId | varchar(2) | 2 | NULL allowed |
|  | SageCostCenter | varchar(5) | 5 | NULL allowed |
|  | Status | varchar(10) | 10 | NULL allowed |
|  | CreateUser | varchar(50) | 50 | NULL allowed |
|  | CreateDateTime | datetime | 8 | NULL allowed |
|  | CreateComputer | varchar(50) | 50 | NULL allowed |
|  | UpdateDateTime | datetime | 8 | NULL allowed |
|  | UpdateUser | varchar(50) | 50 | NULL allowed |
|  | UpdateComputer | varchar(50) | 50 | NULL allowed |


---

## <a name="#indexes"></a>Indexes

| Key | Name | Key Columns | Unique |
|---|---|---|---|
| [![Cluster Primary Key PK_BillingCode: Description](../../../../Images/pkcluster.png)](#indexes) | PK_BillingCode | Description | YES |


---

## <a name="#sqlscript"></a>SQL Script

```sql
CREATE TABLE [dbo].[BillingDepartments]
(
[Description] [varchar] (200) COLLATE SQL_Latin1_General_CP1_CI_AS NOT NULL,
[SortOrder] [bigint] NULL,
[ServiceTypeId] [varchar] (2) COLLATE SQL_Latin1_General_CP1_CI_AS NULL,
[SageCostCenter] [varchar] (5) COLLATE SQL_Latin1_General_CP1_CI_AS NULL,
[Status] [varchar] (10) COLLATE SQL_Latin1_General_CP1_CI_AS NULL,
[CreateUser] [varchar] (50) COLLATE SQL_Latin1_General_CP1_CI_AS NULL,
[CreateDateTime] [datetime] NULL,
[CreateComputer] [varchar] (50) COLLATE SQL_Latin1_General_CP1_CI_AS NULL,
[UpdateDateTime] [datetime] NULL,
[UpdateUser] [varchar] (50) COLLATE SQL_Latin1_General_CP1_CI_AS NULL,
[UpdateComputer] [varchar] (50) COLLATE SQL_Latin1_General_CP1_CI_AS NULL
) ON [PRIMARY]
GO
ALTER TABLE [dbo].[BillingDepartments] ADD CONSTRAINT [PK_BillingCode] PRIMARY KEY CLUSTERED ([Description]) ON [PRIMARY]
GO

```


---

## <a name="#usedby"></a>Used By

* [[dbo].[vwSelectExportToSage]](../Views/dbo_vwSelectExportToSage.md)
* [[dbo].[vwSelectExportToSageAccrual]](../Views/dbo_vwSelectExportToSageAccrual.md)
* [[dbo].[vwSelectExportToSageTest]](../Views/dbo_vwSelectExportToSageTest.md)


---

###### Author:  Sastry

###### Copyright 2023 - All Rights Reserved

###### Created: Thursday, October 5, 2023 9:55:17 PM

