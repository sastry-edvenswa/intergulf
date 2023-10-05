#### 

[Project](../../../../index.md) > [(local)\\](../../../index.md) > [User databases](../../index.md) > [Intergulf](../index.md) > [Tables](Tables.md) > dbo.Sales

# ![Tables](../../../../Images/Table32.png) [dbo].[Sales]

---

## <a name="#properties"></a>Properties

| Property | Value |
|---|---|
| Collation | SQL_Latin1_General_CP1_CI_AS |
| Heap | YES |
| Row Count (~) | 593 |
| Created | 6:47:37 PM Monday, January 29, 2007 |
| Last Modified | 6:47:37 PM Monday, January 29, 2007 |


---

## <a name="#columns"></a>Columns

| Name | Data Type | Max Length (Bytes) | Nullability |
|---|---|---|---|
| Company | nvarchar(255) | 510 | NULL allowed |
| Refinery | nvarchar(255) | 510 | NULL allowed |
| Primary Products | nvarchar(255) | 510 | NULL allowed |
| Primary Feedstocks | nvarchar(255) | 510 | NULL allowed |
| Byproducts | nvarchar(255) | 510 | NULL allowed |
| Mailing Address | nvarchar(255) | 510 | NULL allowed |
| City | nvarchar(255) | 510 | NULL allowed |
| State | nvarchar(255) | 510 | NULL allowed |
| Zip Code | nvarchar(255) | 510 | NULL allowed |
| Physical Address | nvarchar(255) | 510 | NULL allowed |
| Physical City | nvarchar(255) | 510 | NULL allowed |
| Physical State | nvarchar(255) | 510 | NULL allowed |
| Primary Contact | nvarchar(255) | 510 | NULL allowed |
| Phone Number | nvarchar(255) | 510 | NULL allowed |
| Fax Number | nvarchar(255) | 510 | NULL allowed |
| Plant Manager | nvarchar(255) | 510 | NULL allowed |
| PM Phone # | nvarchar(255) | 510 | NULL allowed |
| Purchasing Manager | nvarchar(255) | 510 | NULL allowed |
| Pur M Phone # | nvarchar(255) | 510 | NULL allowed |
| Engineering Manager | nvarchar(255) | 510 | NULL allowed |
| EM Phone # | nvarchar(255) | 510 | NULL allowed |
| Environmental Manager | nvarchar(255) | 510 | NULL allowed |
| Env Manager Phone # | nvarchar(255) | 510 | NULL allowed |
| Notes | nvarchar(255) | 510 | NULL allowed |
| Production Capacity | nvarchar(255) | 510 | NULL allowed |
| Processes | nvarchar(255) | 510 | NULL allowed |
| Location | nvarchar(255) | 510 | NULL allowed |
| Website | nvarchar(255) | 510 | NULL allowed |


---

## <a name="#sqlscript"></a>SQL Script

```sql
CREATE TABLE [dbo].[Sales]
(
[Company] [nvarchar] (255) COLLATE SQL_Latin1_General_CP1_CI_AS NULL,
[Refinery] [nvarchar] (255) COLLATE SQL_Latin1_General_CP1_CI_AS NULL,
[Primary Products] [nvarchar] (255) COLLATE SQL_Latin1_General_CP1_CI_AS NULL,
[Primary Feedstocks] [nvarchar] (255) COLLATE SQL_Latin1_General_CP1_CI_AS NULL,
[Byproducts] [nvarchar] (255) COLLATE SQL_Latin1_General_CP1_CI_AS NULL,
[Mailing Address] [nvarchar] (255) COLLATE SQL_Latin1_General_CP1_CI_AS NULL,
[City] [nvarchar] (255) COLLATE SQL_Latin1_General_CP1_CI_AS NULL,
[State] [nvarchar] (255) COLLATE SQL_Latin1_General_CP1_CI_AS NULL,
[Zip Code] [nvarchar] (255) COLLATE SQL_Latin1_General_CP1_CI_AS NULL,
[Physical Address] [nvarchar] (255) COLLATE SQL_Latin1_General_CP1_CI_AS NULL,
[Physical City] [nvarchar] (255) COLLATE SQL_Latin1_General_CP1_CI_AS NULL,
[Physical State] [nvarchar] (255) COLLATE SQL_Latin1_General_CP1_CI_AS NULL,
[Primary Contact] [nvarchar] (255) COLLATE SQL_Latin1_General_CP1_CI_AS NULL,
[Phone Number] [nvarchar] (255) COLLATE SQL_Latin1_General_CP1_CI_AS NULL,
[Fax Number] [nvarchar] (255) COLLATE SQL_Latin1_General_CP1_CI_AS NULL,
[Plant Manager] [nvarchar] (255) COLLATE SQL_Latin1_General_CP1_CI_AS NULL,
[PM Phone #] [nvarchar] (255) COLLATE SQL_Latin1_General_CP1_CI_AS NULL,
[Purchasing Manager] [nvarchar] (255) COLLATE SQL_Latin1_General_CP1_CI_AS NULL,
[Pur M Phone #] [nvarchar] (255) COLLATE SQL_Latin1_General_CP1_CI_AS NULL,
[Engineering Manager] [nvarchar] (255) COLLATE SQL_Latin1_General_CP1_CI_AS NULL,
[EM Phone #] [nvarchar] (255) COLLATE SQL_Latin1_General_CP1_CI_AS NULL,
[Environmental Manager] [nvarchar] (255) COLLATE SQL_Latin1_General_CP1_CI_AS NULL,
[Env Manager Phone #] [nvarchar] (255) COLLATE SQL_Latin1_General_CP1_CI_AS NULL,
[Notes] [nvarchar] (255) COLLATE SQL_Latin1_General_CP1_CI_AS NULL,
[Production Capacity] [nvarchar] (255) COLLATE SQL_Latin1_General_CP1_CI_AS NULL,
[Processes] [nvarchar] (255) COLLATE SQL_Latin1_General_CP1_CI_AS NULL,
[Location] [nvarchar] (255) COLLATE SQL_Latin1_General_CP1_CI_AS NULL,
[Website] [nvarchar] (255) COLLATE SQL_Latin1_General_CP1_CI_AS NULL
) ON [PRIMARY]
GO

```


---

###### Author:  Sastry

###### Copyright 2023 - All Rights Reserved

###### Created: Thursday, October 5, 2023 9:55:17 PM

