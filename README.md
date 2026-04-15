# Zen Power Challenge

## Objectives

Build an effective business intelligence dashboard using the Zen Power solar dataset.

---

# Questions to Potentially Answer: 
- How much could any given person potentially save with solar?
- How much could each city / municipality save based if they swapped to solar? 
- How much of a positive effect would we have on the environment on a city / state basis? 
- Where are the hotspots for solar? What cities are seeing the most amount of people that have solar? 
- Which cities are hanging on the fastest rate? 
- What kinds of time data can we see here? Is there a time of year that sees the most people switching to solar?
- Are there any geospatial insights we an use to see where would be the best solar cities? 


## Recommended Resources

| Resource | Link / Info |
|---|---|
| Sample Database (Supabase) | Shared via link — open to anyone |
| Data Dictionary | Includes header and first 5 rows |
| Google Sun API | For solar irradiance / geospatial data |

---

## Repository

[github.com/Zen-Power-Solar/DataHacks-ZenPower-Challenge-Spring-2026](https://github.com/Zen-Power-Solar/DataHacks-ZenPower-Challenge-Spring-2026)

---



# Data Dictionary:

### Records
| Variable | Description | Datatype |
|---|---|---|
| id | Unique identifier. Given per row of data. | UUID |
| created_at | When the record was uploaded to our DB. | Timestamptz |
| source_id | Internal DB use. Not important. | UUID |
| source_type | Internal also. Not important. | Text |
| permit_id | Unique ID for the permit with the city. | UUID |
| permit_type | The different types of permits filed. Each has their own purposing. Photovoltaic is pretty much the same thing as a solar permit. Each city largely has their own titles / types of permits. | Text |
| kind | Will always be SOLAR for this dataset. | Text |
| company_name | The name of the construction company that's providing the solar service. | Text |
| kilowatt_value | Measure of the power rate for an electrical device, in this case the house / location provided. This is per hour (likely) | Float |
| issue_date | When the permit for the Solar installation was issued. | Timestamptz |
| apply_date | When the owner applied for the permit | Timestamptz | 
| latitude | One half of the coordinates of the location. | Float |
| longitude | The other half of the coordinates of the location | Float |
| full_address | Self-Explanatory | Text |
| city | The municipality in which the POI is. | Text | 
| state | The State in which the POI is. Abbreviated. | Text | 
| county | The County of the POI. (Not a ton of filled values here) | Text |
| postal_code | The US Postal code of the POI. | Text |
| is_active | Is the permit still valid. | Bool | 
| is_system_size_estimation | This is pretty much an accuracy tell on the kilowatt hours. If it's false, kilowatt_value may or may not be accurate. | Bool |


### Titan All Addresses
| Column Name    | Data Type | Description                                              |
|---------------|----------|----------------------------------------------------------|
| BIZ_NAME      | object   | The registered legal or trading name of the business entity.               |
| NAME          | object   | The name of the primary contact person or authorized representative.       |
| PRIMARY_EMAIL | object   | Primary contact email address for the company            |
| PRIMARY_PHONE | object   | Main telephone number for the business                   |
| LICENSE       | object   | Professional contractor license number                   |
| PERMIT_ID     | object   | A unique alphanumeric identifier assigned to the specific installation permit. |
| STREET_NO     | float64  | House or building number of the project site             |
| STREET        | object   | Name of the street where the project is located          |
| CITY          | object   | City of the project location                             |
| STATE         | object   | Two-letter state code     
| ZIPCODE       | float64  | The five-digit postal code for the project address.                        |
| PERMIT_DATE   | object   | Date the permit was issued or recorded                   |

### SunRun
| Column Name      | Data Type | Description                         |
|------------------|----------|-------------------------------------|
| CONTRACTOR_NAME  | object   | Name of the contractor              |
| PROJECT_ADDRESS  | object   | Address of the project site         |
| INSTALL_DATE     | object   | Date of project installation        |

### Sullivan Solar
| Column Name    | Data Type | Description                                              |
|---------------|----------|----------------------------------------------------------|
| BIZ_NAME      | object   | Legal or trade name of the business entity               |
| PRIMARY_EMAIL | object   | Primary contact email address for the company            |
| PRIMARY_PHONE | object   | Main telephone number for the business                   |
| LICENSE       | object   | Professional contractor license number                   |
| PERMIT_ID     | object   | A unique alphanumeric identifier assigned to the specific installation permit. |
| STREET_NO     | float64  | House or building number of the project site             |
| STREET        | object   | Name of the street where the project is located          |
| CITY          | object   | City of the project location                             |
| STATE         | object   | Two-letter state code                                    |
| ZIPCODE       | float64  | The five-digit postal code for the project address.                        |
| PERMIT_DATE   | object   | Date the permit was issued or recorded                   |

### Solar City
| Variable | Description | Datatype |
|---|---|---|
| BIZ_NAME | The name of the business | Text |
| ID | Unique identifier for the permit. | Text |
| Permit Number | Additional identifier of the permit. | Text | 
| APN | Assessor's Parcel Number. Official authorization of the permit | Text | 
| COUNTY_FIPS | A County FIPS code is a five-digit Federal Information Processing Standard code that uniquely identifies counties and county equivalents in the US. It consists of a two-digit state code combined with a three-digit county code, ensuring standardized identification across government data. For example, 06037 identifies California (06) and Los Angeles County (037). | Number |
| STATE_FIPS | Same as above but for state | Number | 
CBSA | Core based statistical area. Geographic entity defined by the Office of Management and Budget for Federal Data Collection. | Text | 
| CBSA_FIPS | FIPS number for the previous column | Number | 
|
### Freedom Forever
| Variable | Description | Datatype |
|---|---|---|
| CONTRACTOR_NAME | Name of the company that filed the permit / did the solar installation | Text | 
| PROJECT_ADDRESS | The address of the installation | Text | 
| INSTALL_DATE | When the project is listed to be installed | Timestamptz
