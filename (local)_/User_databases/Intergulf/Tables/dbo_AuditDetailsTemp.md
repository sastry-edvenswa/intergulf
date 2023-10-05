#### 

[Project](../../../../index.md) > [(local)\\](../../../index.md) > [User databases](../../index.md) > [Intergulf](../index.md) > [Tables](Tables.md) > dbo.AuditDetailsTemp

# ![Tables](../../../../Images/Table32.png) [dbo].[AuditDetailsTemp]

---

## <a name="#properties"></a>Properties

| Property | Value |
|---|---|
| Collation | SQL_Latin1_General_CP1_CI_AS |
| Heap | YES |
| Row Count (~) | 35567 |
| Created | 4:28:02 PM Friday, December 6, 2019 |
| Last Modified | 4:28:02 PM Friday, December 6, 2019 |


---

## <a name="#columns"></a>Columns

| Name | Data Type | Max Length (Bytes) | Nullability | Identity |
|---|---|---|---|---|
| Id | bigint | 8 | NOT NULL | 1000 - 1 |
| TableName | varchar(50) | 50 | NULL allowed |  |
| KeyValue | bigint | 8 | NULL allowed |  |
| OriginalRecordSet | varchar(max) | max | NULL allowed |  |
| NewRecordSet | varchar(max) | max | NULL allowed |  |
| Processed | bit | 1 | NULL allowed |  |
| UpdateUser | varchar(50) | 50 | NULL allowed |  |
| UpdateDateTime | datetime | 8 | NULL allowed |  |
| UpdateComputer | varchar(50) | 50 | NULL allowed |  |
| FieldList | varchar(max) | max | NULL allowed |  |


---

## <a name="#sqlscript"></a>SQL Script

```sql
CREATE TABLE [dbo].[AuditDetailsTemp]
(
[Id] [bigint] NOT NULL IDENTITY(1000, 1),
[TableName] [varchar] (50) COLLATE SQL_Latin1_General_CP1_CI_AS NULL,
[KeyValue] [bigint] NULL,
[OriginalRecordSet] [varchar] (max) COLLATE SQL_Latin1_General_CP1_CI_AS NULL,
[NewRecordSet] [varchar] (max) COLLATE SQL_Latin1_General_CP1_CI_AS NULL,
[Processed] [bit] NULL,
[UpdateUser] [varchar] (50) COLLATE SQL_Latin1_General_CP1_CI_AS NULL,
[UpdateDateTime] [datetime] NULL,
[UpdateComputer] [varchar] (50) COLLATE SQL_Latin1_General_CP1_CI_AS NULL,
[FieldList] [varchar] (max) COLLATE SQL_Latin1_General_CP1_CI_AS NULL
) ON [PRIMARY]
GO

```


---

###### Author:  Sastry

###### Copyright 2023 - All Rights Reserved

###### Created: Thursday, October 5, 2023 9:55:17 PM

