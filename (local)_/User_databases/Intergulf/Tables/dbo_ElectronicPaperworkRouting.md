#### 

[Project](../../../../index.md) > [(local)\\](../../../index.md) > [User databases](../../index.md) > [Intergulf](../index.md) > [Tables](Tables.md) > dbo.ElectronicPaperworkRouting

# ![Tables](../../../../Images/Table32.png) [dbo].[ElectronicPaperworkRouting]

---

## <a name="#properties"></a>Properties

| Property | Value |
|---|---|
| Collation | SQL_Latin1_General_CP1_CI_AS |
| Heap | YES |
| Row Count (~) | 274 |
| Created | 1:10:22 PM Wednesday, December 26, 2018 |
| Last Modified | 1:10:22 PM Wednesday, December 26, 2018 |


---

## <a name="#columns"></a>Columns

| Name | Data Type | Max Length (Bytes) | Nullability | Identity |
|---|---|---|---|---|
| Id | bigint | 8 | NOT NULL | 1 - 1 |
| BillingDepartment | varchar(50) | 50 | NULL allowed |  |
| SalesPersonId | varchar(50) | 50 | NULL allowed |  |
| DestinationId | bigint | 8 | NULL allowed |  |
| BillingPersonId | varchar(50) | 50 | NULL allowed |  |
| CreateUser | varchar(50) | 50 | NULL allowed |  |
| CreateDateTime | datetime | 8 | NULL allowed |  |
| CreateComputer | varchar(50) | 50 | NULL allowed |  |
| UpdateDateTime | datetime | 8 | NULL allowed |  |
| UpdateUser | varchar(50) | 50 | NULL allowed |  |
| UpdateComputer | varchar(50) | 50 | NULL allowed |  |


---

## <a name="#sqlscript"></a>SQL Script

```sql
CREATE TABLE [dbo].[ElectronicPaperworkRouting]
(
[Id] [bigint] NOT NULL IDENTITY(1, 1),
[BillingDepartment] [varchar] (50) COLLATE SQL_Latin1_General_CP1_CI_AS NULL,
[SalesPersonId] [varchar] (50) COLLATE SQL_Latin1_General_CP1_CI_AS NULL,
[DestinationId] [bigint] NULL,
[BillingPersonId] [varchar] (50) COLLATE SQL_Latin1_General_CP1_CI_AS NULL,
[CreateUser] [varchar] (50) COLLATE SQL_Latin1_General_CP1_CI_AS NULL,
[CreateDateTime] [datetime] NULL,
[CreateComputer] [varchar] (50) COLLATE SQL_Latin1_General_CP1_CI_AS NULL,
[UpdateDateTime] [datetime] NULL,
[UpdateUser] [varchar] (50) COLLATE SQL_Latin1_General_CP1_CI_AS NULL,
[UpdateComputer] [varchar] (50) COLLATE SQL_Latin1_General_CP1_CI_AS NULL
) ON [PRIMARY]
GO

```


---

## <a name="#usedby"></a>Used By

* [[dbo].[vwSelectElectronicPaperworkRoutingOrder]](../Views/dbo_vwSelectElectronicPaperworkRoutingOrder.md)


---

###### Author:  Sastry

###### Copyright 2023 - All Rights Reserved

###### Created: Thursday, October 5, 2023 9:55:17 PM

