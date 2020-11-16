# Police Stops Data Dictionary  
Data about police stops of drivers and pedestrians. Used by [police_stop notebooks](../../notebooks/police_stops/)  

### Standard fields  
| Field | Data Type | Description | Length | Expected Pattern | null? |  
| ----- | ---- | ---- | ---- | ---- |---- |  
| stop_date | datetime | The date and time when the stop occurred. | 19 | YYYY/MM/DD HH24:MM:SS |no |  
| subject_race | string | Reported race of the person being stopped. | varies | varies, 'Unknown' | yes |  
| subject_sex | string | Gender of person being stopped. | varies | ('Male', 'Female', 'Non-Binary', 'Unknown') | yes |  
| subject_age | integer | Age of person being stopped. | 3 | [10-150] | yes |  
| search_conducted | string | Was a vehicle searched? | 1 | ('Y','N') | yes |  
| contraband_found | string | Was contraband found in the search or frisk? | 1 | ('Y','N') | yes |  
| citation_issued | string | Was a citation issued? | 1 | ('Y','N') | yes |  
| warning_issued | string | Was a warning issued? | 1 | ('Y','N') | yes |  
| frisk_performed | string | Was a body search performed? | 1 | ('Y','N') | yes |  
| arrest_made | string | Was the person being stopped arrested? | 1 | ('Y','N') | yes |  
| reason_for_stop | string | What was the reason for the stop? | varies | varies, 'Unknown' | yes |  

### Extended fields  
| Field | Data Type | Description | Length | Expected Pattern | null? |  
| ----- | ---- | ---- | ---- | ---- |---- |  
| stop_latitude | string | Latitude of where the stop occurred. | 9-10 | DDD MM SS('N','S','E','W') |---- |  
| stop_longitude | string | Longitude of where the stop occurred. | 9-10 | DDD MM SS('N','S','E','W') |---- |  


## Additional metadata / information

- Minneapolis Police Department, ["Using data dashboards"](https://www.minneapolismn.gov/resident-services/public-safety/police-public-safety/crime-maps-dashboards/using-police-dashboards/) - Gives information on codes found in the 'call disposition' field in the raw data file for Minneapolis police stops.