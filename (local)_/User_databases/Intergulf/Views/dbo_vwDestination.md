#### 

[Project](../../../../index.md) > [(local)\\](../../../index.md) > [User databases](../../index.md) > [Intergulf](../index.md) > [Views](Views.md) > dbo.vwDestination

# ![Views](../../../../Images/View32.png) [dbo].[vwDestination]

---

## <a name="#properties"></a>Properties

| Property | Value |
|---|---|
| Collation | SQL_Latin1_General_CP1_CI_AS |
| ANSI Nulls On | YES |
| Quoted Identifier On | YES |
| Created | 10:20:47 PM Saturday, February 10, 2007 |
| Last Modified | 5:34:07 PM Tuesday, October 26, 2021 |


---

## <a name="#columns"></a>Columns

| Name | Data Type | Max Length (Bytes) |
|---|---|---|
| Id | int | 4 |
| Name | nvarchar(100) | 200 |
| Address | nvarchar(50) | 100 |
| City | nvarchar(50) | 100 |
| State | nvarchar(50) | 100 |
| Zip | nvarchar(50) | 100 |
| Contact | nvarchar(50) | 100 |
| Phone | nvarchar(50) | 100 |
| Fax | nvarchar(50) | 100 |
| Email | nvarchar(50) | 100 |
| Notes | nvarchar(500) | 1000 |
| EpaIdNo | nvarchar(50) | 100 |
| TceqNo | nvarchar(50) | 100 |
| UpdateDateTime | datetime | 8 |
| UpdateUser | varchar(50) | 50 |
| UpdateComputer | varchar(50) | 50 |
| AllowHazards | varchar(2) | 2 |
| FacilityName | varchar(50) | 50 |
| Facility | varchar(50) | 50 |
| Status | varchar(50) | 50 |
| DestinationDisplay | varchar(255) | 255 |


---

## <a name="#sqlscript"></a>SQL Script

```sql
CREATE VIEW [dbo].[vwDestination]
AS
SELECT        Id, Name, Address, City, State, Zip, Contact, Phone, Fax, Email, Notes, EpaIdNo, TceqNo, UpdateDateTime, UpdateUser, UpdateComputer, AllowHazards, FacilityName, Facility, Status, 
                         dbo.fnGetDestinationDisplay(Name, Facility) AS DestinationDisplay
FROM            dbo.fnSelectDestination() AS fnSelectDestination
GO

```


---

## <a name="#uses"></a>Uses

* [[dbo].[fnGetDestinationDisplay]](../Programmability/Functions/Scalar-valued_Functions/dbo_fnGetDestinationDisplay.md)
* [[dbo].[fnSelectDestination]](../Programmability/Functions/Table-valued_Functions/dbo_fnSelectDestination.md)


---

###### Author:  Sastry

###### Copyright 2023 - All Rights Reserved

###### Created: Thursday, October 5, 2023 9:55:17 PM

