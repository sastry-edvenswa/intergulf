#### 

[Project](../../../../../../index.md) > [(local)\\](../../../../../index.md) > [User databases](../../../../index.md) > [Intergulf](../../../index.md) > Programmability > Functions > [Table-valued Functions](Table-valued_Functions.md) > dbo.fnSelectOneLoads

# ![Table-valued Functions](../../../../../../Images/Function_Table32.png) [dbo].[fnSelectOneLoads]

---

## <a name="#properties"></a>Properties

| Property | Value |
|---|---|
| ANSI Nulls On | NO |
| Quoted Identifier On | YES |


---

## <a name="#parameters"></a>Parameters

| Name | Data Type | Max Length (Bytes) |
|---|---|---|
| @Id | int | 4 |


---

## <a name="#sqlscript"></a>SQL Script

```sql
SET ANSI_NULLS OFF
GO



CREATE    FUNCTION [dbo].[fnSelectOneLoads]
                 (@Id as int)
RETURNS table
AS
RETURN (
        SELECT *
        FROM dbo.Loads
       WHERE ID = @Id
       )
















GO

```


---

## <a name="#uses"></a>Uses

* [[dbo].[Loads]](../../../Tables/dbo_Loads.md)


---

###### Author:  Sastry

###### Copyright 2023 - All Rights Reserved

###### Created: Thursday, October 5, 2023 9:55:17 PM

