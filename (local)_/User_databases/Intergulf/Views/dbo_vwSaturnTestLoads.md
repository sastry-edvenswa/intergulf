#### 

[Project](../../../../index.md) > [(local)\\](../../../index.md) > [User databases](../../index.md) > [Intergulf](../index.md) > [Views](Views.md) > dbo.vwSaturnTestLoads

# ![Views](../../../../Images/View32.png) [dbo].[vwSaturnTestLoads]

---

## <a name="#properties"></a>Properties

| Property | Value |
|---|---|
| Collation | SQL_Latin1_General_CP1_CI_AS |
| ANSI Nulls On | YES |
| Quoted Identifier On | YES |
| Created | 3:18:44 PM Thursday, February 16, 2023 |
| Last Modified | 3:18:44 PM Thursday, February 16, 2023 |


---

## <a name="#columns"></a>Columns

| Name | Data Type | Max Length (Bytes) | Identity |
|---|---|---|---|
| Id | bigint | 8 | 0 - 0 |
| ContractNumber | varchar(50) | 50 |  |
| UpdateDateTime | datetime | 8 |  |
| VendorId | bigint | 8 |  |
| TransactionType | varchar(20) | 20 |  |
| LoadType | varchar(50) | 50 |  |
| CustomerPickupDelivery | varchar(3) | 3 |  |
| ScheduledDate | datetime | 8 |  |
| TransporterId | bigint | 8 |  |
| DispatchStatus | varchar(50) | 50 |  |
| AccountingStatus | varchar(40) | 40 |  |
| AccountingAction | varchar(40) | 40 |  |
| EquipmentType | varchar(50) | 50 |  |
| DriverId | bigint | 8 |  |


---

## <a name="#sqlscript"></a>SQL Script

```sql
CREATE VIEW [dbo].[vwSaturnTestLoads]
AS
SELECT        Id, ContractNumber, UpdateDateTime, VendorId, TransactionType, LoadType, CustomerPickupDelivery, ScheduledDate, TransporterId, DispatchStatus, AccountingStatus, AccountingAction, EquipmentType, 
                         DriverId
FROM            dbo.Loads
WHERE        (Id = 495980)
GO

```


---

## <a name="#uses"></a>Uses

* [[dbo].[Loads]](../Tables/dbo_Loads.md)


---

###### Author:  Sastry

###### Copyright 2023 - All Rights Reserved

###### Created: Thursday, October 5, 2023 9:55:17 PM

