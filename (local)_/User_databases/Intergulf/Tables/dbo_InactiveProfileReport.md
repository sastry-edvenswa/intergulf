#### 

[Project](../../../../index.md) > [(local)\\](../../../index.md) > [User databases](../../index.md) > [Intergulf](../index.md) > [Tables](Tables.md) > dbo.InactiveProfileReport

# ![Tables](../../../../Images/Table32.png) [dbo].[InactiveProfileReport]

---

## <a name="#properties"></a>Properties

| Property | Value |
|---|---|
| Collation | SQL_Latin1_General_CP1_CI_AS |
| Row Count (~) | 0 |
| Created | 9:35:16 PM Tuesday, November 8, 2011 |
| Last Modified | 11:50:36 AM Sunday, January 15, 2017 |


---

## <a name="#columns"></a>Columns

| Key | Name | Data Type | Max Length (Bytes) | Nullability | Identity |
|---|---|---|---|---|---|
| [![Cluster Primary Key PK_InactiveProfileReport: Id](../../../../Images/pkcluster.png)](#indexes) | Id | bigint | 8 | NOT NULL | 1 - 1 |
|  | UserName | varchar(50) | 50 | NULL allowed |  |
|  | ProfileId | varchar(50) | 50 | NULL allowed |  |
|  | GeneratorName | varchar(300) | 300 | NULL allowed |  |
|  | CustomerName | varchar(300) | 300 | NULL allowed |  |
|  | ProfileNo | varchar(50) | 50 | NULL allowed |  |
|  | WasteCode | varchar(50) | 50 | NULL allowed |  |
|  | MaterialCode | varchar(50) | 50 | NULL allowed |  |
|  | Description | varchar(500) | 500 | NULL allowed |  |
|  | LastDate | datetime | 8 | NULL allowed |  |
|  | LoadCount | bigint | 8 | NULL allowed |  |
|  | Status | varchar(50) | 50 | NULL allowed |  |
|  | SalesPersonId | varchar(50) | 50 | NULL allowed |  |


---

## <a name="#indexes"></a>Indexes

| Key | Name | Key Columns | Unique |
|---|---|---|---|
| [![Cluster Primary Key PK_InactiveProfileReport: Id](../../../../Images/pkcluster.png)](#indexes) | PK_InactiveProfileReport | Id | YES |


---

## <a name="#sqlscript"></a>SQL Script

```sql
CREATE TABLE [dbo].[InactiveProfileReport]
(
[Id] [bigint] NOT NULL IDENTITY(1, 1),
[UserName] [varchar] (50) COLLATE SQL_Latin1_General_CP1_CI_AS NULL,
[ProfileId] [varchar] (50) COLLATE SQL_Latin1_General_CP1_CI_AS NULL,
[GeneratorName] [varchar] (300) COLLATE SQL_Latin1_General_CP1_CI_AS NULL,
[CustomerName] [varchar] (300) COLLATE SQL_Latin1_General_CP1_CI_AS NULL,
[ProfileNo] [varchar] (50) COLLATE SQL_Latin1_General_CP1_CI_AS NULL,
[WasteCode] [varchar] (50) COLLATE SQL_Latin1_General_CP1_CI_AS NULL,
[MaterialCode] [varchar] (50) COLLATE SQL_Latin1_General_CP1_CI_AS NULL,
[Description] [varchar] (500) COLLATE SQL_Latin1_General_CP1_CI_AS NULL,
[LastDate] [datetime] NULL,
[LoadCount] [bigint] NULL,
[Status] [varchar] (50) COLLATE SQL_Latin1_General_CP1_CI_AS NULL,
[SalesPersonId] [varchar] (50) COLLATE SQL_Latin1_General_CP1_CI_AS NULL
) ON [PRIMARY]
GO
ALTER TABLE [dbo].[InactiveProfileReport] ADD CONSTRAINT [PK_InactiveProfileReport] PRIMARY KEY CLUSTERED ([Id]) ON [PRIMARY]
GO

```


---

## <a name="#usedby"></a>Used By

* [[dbo].[vwRptProfileInactive]](../Views/dbo_vwRptProfileInactive.md)


---

###### Author:  Sastry

###### Copyright 2023 - All Rights Reserved

###### Created: Thursday, October 5, 2023 9:55:17 PM

