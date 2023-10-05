#### 

[Project](../../../../index.md) > [(local)\\](../../../index.md) > [User databases](../../index.md) > [Intergulf](../index.md) > [Tables](Tables.md) > dbo.SageCustomers

# ![Tables](../../../../Images/Table32.png) [dbo].[SageCustomers]

---

## <a name="#properties"></a>Properties

| Property | Value |
|---|---|
| Collation | SQL_Latin1_General_CP1_CI_AS |
| Row Count (~) | 1078 |
| Created | 7:37:28 PM Monday, May 7, 2018 |
| Last Modified | 7:37:28 PM Monday, May 7, 2018 |


---

## <a name="#columns"></a>Columns

| Key | Name | Data Type | Max Length (Bytes) | Nullability |
|---|---|---|---|---|
| [![Cluster Primary Key PK_SageCustomers: CustomerNo](../../../../Images/pkcluster.png)](#indexes) | CustomerNo | varchar(20) | 20 | NOT NULL |
|  | Name | varchar(50) | 50 | NULL allowed |
|  | Status | varchar(20) | 20 | NULL allowed |
|  | AddressLine1 | varchar(50) | 50 | NULL allowed |
|  | AddressLine2 | varchar(50) | 50 | NULL allowed |
|  | AddressLine3 | varchar(50) | 50 | NULL allowed |
|  | City | varchar(50) | 50 | NULL allowed |
|  | ZipCode | varchar(20) | 20 | NULL allowed |
|  | PhoneNumber | varchar(50) | 50 | NULL allowed |
|  | State | varchar(10) | 10 | NULL allowed |


---

## <a name="#indexes"></a>Indexes

| Key | Name | Key Columns | Unique |
|---|---|---|---|
| [![Cluster Primary Key PK_SageCustomers: CustomerNo](../../../../Images/pkcluster.png)](#indexes) | PK_SageCustomers | CustomerNo | YES |


---

## <a name="#sqlscript"></a>SQL Script

```sql
CREATE TABLE [dbo].[SageCustomers]
(
[CustomerNo] [varchar] (20) COLLATE SQL_Latin1_General_CP1_CI_AS NOT NULL,
[Name] [varchar] (50) COLLATE SQL_Latin1_General_CP1_CI_AS NULL,
[Status] [varchar] (20) COLLATE SQL_Latin1_General_CP1_CI_AS NULL,
[AddressLine1] [varchar] (50) COLLATE SQL_Latin1_General_CP1_CI_AS NULL,
[AddressLine2] [varchar] (50) COLLATE SQL_Latin1_General_CP1_CI_AS NULL,
[AddressLine3] [varchar] (50) COLLATE SQL_Latin1_General_CP1_CI_AS NULL,
[City] [varchar] (50) COLLATE SQL_Latin1_General_CP1_CI_AS NULL,
[ZipCode] [varchar] (20) COLLATE SQL_Latin1_General_CP1_CI_AS NULL,
[PhoneNumber] [varchar] (50) COLLATE SQL_Latin1_General_CP1_CI_AS NULL,
[State] [varchar] (10) COLLATE SQL_Latin1_General_CP1_CI_AS NULL
) ON [PRIMARY]
GO
ALTER TABLE [dbo].[SageCustomers] ADD CONSTRAINT [PK_SageCustomers] PRIMARY KEY CLUSTERED ([CustomerNo]) ON [PRIMARY]
GO

```


---

###### Author:  Sastry

###### Copyright 2023 - All Rights Reserved

###### Created: Thursday, October 5, 2023 9:55:17 PM

