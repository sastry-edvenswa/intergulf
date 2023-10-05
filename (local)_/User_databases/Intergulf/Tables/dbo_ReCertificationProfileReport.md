#### 

[Project](../../../../index.md) > [(local)\\](../../../index.md) > [User databases](../../index.md) > [Intergulf](../index.md) > [Tables](Tables.md) > dbo.ReCertificationProfileReport

# ![Tables](../../../../Images/Table32.png) [dbo].[ReCertificationProfileReport]

---

## <a name="#properties"></a>Properties

| Property | Value |
|---|---|
| Collation | SQL_Latin1_General_CP1_CI_AS |
| Heap | YES |
| Row Count (~) | 3285 |
| Created | 1:36:57 PM Friday, October 19, 2012 |
| Last Modified | 7:28:27 PM Wednesday, April 29, 2020 |


---

## <a name="#columns"></a>Columns

| Name | Data Type | Max Length (Bytes) | Nullability | Identity |
|---|---|---|---|---|
| Id | bigint | 8 | NOT NULL | 1 - 1 |
| UserName | varchar(50) | 50 | NULL allowed |  |
| ProfileId | varchar(50) | 50 | NULL allowed |  |
| GeneratorName | varchar(100) | 100 | NULL allowed |  |
| CustomerName | varchar(100) | 100 | NULL allowed |  |
| ProfileType | varchar(50) | 50 | NULL allowed |  |
| ProfileNo | varchar(50) | 50 | NULL allowed |  |
| WasteCode | varchar(50) | 50 | NULL allowed |  |
| Description | varchar(1000) | 1000 | NULL allowed |  |
| Status | varchar(50) | 50 | NULL allowed |  |
| TreatmentCode | varchar(50) | 50 | NULL allowed |  |
| GCApprovalDate | datetime | 8 | NULL allowed |  |
| LastLoadDate | datetime | 8 | NULL allowed |  |
| ExpirationDate | datetime | 8 | NULL allowed |  |
| SalesPersonId | varchar(50) | 50 | NULL allowed |  |
| CSRPersonId | varchar(50) | 50 | NULL allowed |  |


---

## <a name="#sqlscript"></a>SQL Script

```sql
CREATE TABLE [dbo].[ReCertificationProfileReport]
(
[Id] [bigint] NOT NULL IDENTITY(1, 1),
[UserName] [varchar] (50) COLLATE SQL_Latin1_General_CP1_CI_AS NULL,
[ProfileId] [varchar] (50) COLLATE SQL_Latin1_General_CP1_CI_AS NULL,
[GeneratorName] [varchar] (100) COLLATE SQL_Latin1_General_CP1_CI_AS NULL,
[CustomerName] [varchar] (100) COLLATE SQL_Latin1_General_CP1_CI_AS NULL,
[ProfileType] [varchar] (50) COLLATE SQL_Latin1_General_CP1_CI_AS NULL,
[ProfileNo] [varchar] (50) COLLATE SQL_Latin1_General_CP1_CI_AS NULL,
[WasteCode] [varchar] (50) COLLATE SQL_Latin1_General_CP1_CI_AS NULL,
[Description] [varchar] (1000) COLLATE SQL_Latin1_General_CP1_CI_AS NULL,
[Status] [varchar] (50) COLLATE SQL_Latin1_General_CP1_CI_AS NULL,
[TreatmentCode] [varchar] (50) COLLATE SQL_Latin1_General_CP1_CI_AS NULL,
[GCApprovalDate] [datetime] NULL,
[LastLoadDate] [datetime] NULL,
[ExpirationDate] [datetime] NULL,
[SalesPersonId] [varchar] (50) COLLATE SQL_Latin1_General_CP1_CI_AS NULL,
[CSRPersonId] [varchar] (50) COLLATE SQL_Latin1_General_CP1_CI_AS NULL
) ON [PRIMARY]
GO

```


---

## <a name="#usedby"></a>Used By

* [[dbo].[vwRptProfileReCertification]](../Views/dbo_vwRptProfileReCertification.md)


---

###### Author:  Sastry

###### Copyright 2023 - All Rights Reserved

###### Created: Thursday, October 5, 2023 9:55:17 PM

