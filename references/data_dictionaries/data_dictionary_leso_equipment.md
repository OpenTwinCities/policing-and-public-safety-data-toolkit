# Defense Logistics Agency LESO Public Information  

## DISP_AllStatesAndTerritories_mmddyyyy.xlsx  
Snapshot of DoD inventory possessed by law enforcement agencies published quarterly with each sheet containing data for one state or territory. Used by [police equipment notebooks](../../notebooks/police_equipment/)  

### Standard Fields   
| Field | Data Type | Description | Length | Expected Pattern | null? |   
| ----- | ---- | ---- | ---- | ---- |---- |   
| State | string | two digit postal abbreviation for U.S. state or territory | 2 | \[A-Z\]\[A-Z\] | no |   
| Station Name (LEA) | string | descriptive name of requesting law enforcement agency | varies | varies | no |   
| NSN | string | [NATO Stock Number](https://en.wikipedia.org/wiki/NATO_Stock_Number) a government-assigned identifier for requested item | 9 | \[0-9\]{4}-\[0-9\]{2}-\[A-Z0-9\]{3}-\[A-Z0-9\]{4} | no |   
| Item Name | string | descriptive name of requested item | varies | varies | no |   
| UI | string | units of requested item known as unit increments | varies | varies | no |   
| Quantity | integer | number of units requested | varies | [0-9]+ | no |   
| Acquisition Value | float | U.S. dollar amount paid when the item was originally purchased by the government | varies | [0-9]+.[0-9]{2} | no |   
| DEMIL Code | character | [demilitarization code](https://www.dla.mil/HQ/LogisticsOperations/Services/FIC/DEMILCoding/DEMILCodes/) for level of destruction required when the item leaves Department of Defense control | 1 | \[GPFDCEBQA\] | no |   
| DEMIL IC | integer | [demilitarization itegrity code](https://www.dla.mil/HQ/LogisticsOperations/Services/FIC/DEMILCoding/DEMILCodes/) validity of DEMIL Code (a missing value means it has not yet been reviewed), see [FLIS manual](https://www.dla.mil/HQ/LogisticsOperations/TrainingandReference/FLISProcedures/) for more information | 1 | [0-9] or blank | yes |   
| Ship Date | datetime64 | date transfered; needs further research | 29 | yyyy-mm-ddT00:00:00.000000000 | no |   
| Station Type | string | level of government associated with requesting agency; needs further research | 5 | 'State' | no |   

## DISP_Shipments_Cancellations_mmddyyyy_to_mmddyyyy.xlsx  
Shipments and cancellations of requests for DoD materials in the specified quarter.   

### Standard Fields (Shipments sheet of the file)   
| Field | Data Type | Description | Length | Expected Pattern | null? |   
| ----- | ---- | ---- | ---- | ---- |---- |   
| State | string | two digit postal abbreviation for U.S. state or territory| 2 | \[A-Z\]\[A-Z\] | no |   
| Station Name (LEA) | string | descriptive name of requesting law enforcement agency | varies | varies | no |   
| Requisition ID | string | apparently unique identifier needs further research | 14 | [A-z0-9]{14} | no |   
| FSC | string | [Federal Supply Number](https://en.wikipedia.org/wiki/NATO_Stock_Number#Federal_Supply_Classification_Group_(FSCG)) consisting of the Federal Supply Group and Federal Supply Classification | 4 | \[0-9\]{4} | no |   
| NIIN | string | [National Item Identification Number](https://en.wikipedia.org/wiki/NATO_Stock_Number#National_Item_Identification_Number_(NIIN)) a Country Code followed by a 7-digit item identifier string | 9 | \[0-9\]{9} | no |   
| Item Name | string | descriptive name of requested item | varies | varies | no |   
| UI | string | units of requested item known as unit increments | varies | varies | no |   
| Quantity | integer | number of units requested | varies | [0-9]+ | no |   
| Acquisition Value | float | U.S. dollar amount paid when the item was originally purchased by the government | varies | [0-9]+.[0-9]{2} | no |   
| Date Shipped | datetime64 | date shipped maybe; needs further research | 29 | yyyy-mm-ddT00:00:00.000000000 | no |   
| Justification | string | descriptive text justifying request; needs further research | varies | varies | yes |

### Standard Fields (Cancellations sheet of the file)   
| Field | Data Type | Description | Length | Expected Pattern | null? |   
| ----- | ---- | ---- | ---- | ---- |---- |   
| Cancelled By | string | apparently agency that cancelled request; needs further research | varies | varies | yes | 
| RTD Ref | string | apparently unique identifier; needs further research | 6 or 7 | [0-9]{7} | no |   
| State | string | two digit postal abbreviation for U.S. state or territory| 2 | \[A-Z\]\[A-Z\] | no |   
| Station Name (LEA) | string | descriptive name of requesting law enforcement agency | varies | varies | no |   
| FSC | string | [Federal Supply Number](https://en.wikipedia.org/wiki/NATO_Stock_Number#Federal_Supply_Classification_Group_(FSCG)) consisting of the Federal Supply Group and Federal Supply Classification | 4 | \[0-9\]{4} | no |   
| NIIN | string | [National Item Identification Number](https://en.wikipedia.org/wiki/NATO_Stock_Number#National_Item_Identification_Number_(NIIN)) a Country Code followed by a 7-digit item identifier string | 9 | \[0-9\]{9} | no |   
| Item Name | string | descriptive name of requested item | varies | varies | no |   
| UI | string | units of requested item known as unit increments | varies | varies | no |   
| Quantity | integer | number of units requested | varies | [0-9]+ | no |   
| Acquisition Value | float | U.S. dollar amount paid when the item was originally purchased by the government | varies | [0-9]+.[0-9]{2} | no |   
| Date Requested | datetime64 | date request made; needs further research | 29 | yyyy-mm-ddT00:00:00.000000000 | no |   
