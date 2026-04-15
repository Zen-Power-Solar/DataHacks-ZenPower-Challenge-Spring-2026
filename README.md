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
| BIZ_NAME | Name of the business or company that filed or is associated with the permit (e.g., contractor or solar installer). | Text |
| ID | Internal unique identifier for the permit record. | Text |
| PERMIT_NUMBER | Official permit number assigned by the issuing jurisdiction (e.g., BLD2017-05386). | Text |
| APN | Assessor's Parcel Number — a unique identifier assigned by the county assessor to a parcel of real property. | Text |
| COUNTY_FIPS | Three-digit Federal Information Processing Standard (FIPS) code identifying a county within a state. Often paired with STATE_FIPS to form a full five-digit county FIPS code (e.g., 001 = Alameda County, CA). | Text |
| STATE_FIPS | Two-digit FIPS code identifying the U.S. state in which the permit was issued (e.g., 06 = California). | Text |
| CBSA | Core-Based Statistical Area name — a geographic entity defined by the Office of Management and Budget (OMB) grouping counties around an urban center (e.g., "San Francisco-Oakland-Berkeley, CA"). | Text |
| CBSA_FIPS | Numeric FIPS code corresponding to the CBSA (e.g., 41860 = San Francisco-Oakland-Berkeley, CA). | Number |
| STATUS | Current status of the permit in the approval/inspection lifecycle (e.g., final, issued, pending). | Text |
| START_DATE | Date on which permitted work was started or the permit became active. | Date |
| END_DATE | Date on which the permit period ended or work was completed. | Date |
| ISSUE_DATE | Date the permit was officially issued by the jurisdiction. | Date |
| FILE_DATE | Date the permit application was filed with the jurisdiction. | Date |
| FINAL_DATE | Date the permit received its final inspection or sign-off. | Date |
| TYPE | High-level category of the permit (e.g., Building, Electrical, Mechanical). | Text |
| SUBTYPE | More granular classification within the permit type. | Text |
| APPROVAL_DURATION | Number of days between the file date and the issue date — represents how long the approval process took. | Number |
| CONSTRUCTION_DURATION | Number of days between the issue date and the final date — represents how long construction took. | Number |
| TOTAL_DURATION | Total number of days from file date to final date, encompassing both approval and construction phases. | Number |
| FEES | Total fees assessed for the permit, in USD. | Number |
| JOB_VALUE | Estimated dollar value of the work covered by the permit, in USD. | Number |
| INSPECTION_PASS_RATE | Ratio of passed inspections to total inspections conducted, expressed as a decimal (e.g., 0.667 = 2 out of 3 passed). | Number |
| INSPECTION_PASSED | Indicates whether the permit ultimately passed its final inspection (true/false). | Boolean |
| DESCRIPTION | Free-text description of the permitted work as entered by the applicant or jurisdiction (e.g., system size, panel count, scope of work). | Text |
| OWNER_NAME | Full name of the property owner. | Text |
| OWNER_STREET | Street address of the property owner. | Text |
| OWNER_CITY | City of the property owner's mailing address. | Text |
| OWNER_STATE | State of the property owner's mailing address. | Text |
| OWNER_ZIPCODE | ZIP code of the property owner's mailing address. | Text |
| OWNER_EMAIL | Email address of the property owner. | Text |
| OWNER_PHONE | Phone number of the property owner. | Text |
| APPLICANT_NAME | Full name of the permit applicant, typically the contractor or installer. | Text |
| APPLICANT_STREET | Street address of the permit applicant. | Text |
| APPLICANT_CITY | City of the permit applicant's address. | Text |
| APPLICANT_STATE | State of the permit applicant's address. | Text |
| APPLICANT_ZIPCODE | ZIP code of the permit applicant's address. | Text |
| APPLICANT_EMAIL | Email address of the permit applicant. | Text |
| APPLICANT_PHONE | Phone number of the permit applicant. | Text |
| WINDOW_DOOR | Indicates whether the permit includes window or door work (true/false). | Boolean |
| STREET_NO | Street number of the property where work is being performed. | Text |
| STREET | Street name of the property where work is being performed. | Text |
| CITY | City where the permitted property is located. | Text |
| ZIPCODE | ZIP code of the permitted property. | Text |
| ZIPCODE_EXT | ZIP+4 extension code for more precise mail routing. | Text |
| JURISDICTION | Name of the local government entity (city, county, or special district) that issued the permit. | Text |
| COUNTY | Name of the county where the permitted property is located. | Text |
| STATE | Two-letter state abbreviation where the permitted property is located (e.g., CA). | Text |
| LAT | Latitude coordinate of the permitted property. | Number |
| LONG | Longitude coordinate of the permitted property. | Number |
| ADDRESS_ID | Internal identifier for the property address. | Text |
| CITY_ID | Internal identifier for the city. | Text |
| JURISDICTION_ID | Internal identifier for the issuing jurisdiction. | Text |
| COUNTY_ID | Internal identifier for the county. | Text |
| ADDITION | Indicates whether the permit includes a building addition (true/false). | Boolean |
| ADU | Indicates whether the permit includes an Accessory Dwelling Unit (true/false). | Boolean |
| BATHROOM | Indicates whether the permit includes bathroom work (true/false). | Boolean |
| BATTERY | Indicates whether the permit includes battery storage installation (true/false). | Boolean |
| DEMOLITION | Indicates whether the permit includes demolition work (true/false). | Boolean |
| ELECTRIC_METER | Indicates whether the permit includes electric meter work (true/false). | Boolean |
| ELECTRICAL | Indicates whether the permit includes general electrical work (true/false). | Boolean |
| EV_CHARGER | Indicates whether the permit includes EV charger installation (true/false). | Boolean |
| FIRE_SPRINKLER | Indicates whether the permit includes fire sprinkler work (true/false). | Boolean |
| GAS | Indicates whether the permit includes gas line work (true/false). | Boolean |
| GENERATOR | Indicates whether the permit includes generator installation (true/false). | Boolean |
| GRADING | Indicates whether the permit includes grading or earthwork (true/false). | Boolean |
| HEAT_PUMP | Indicates whether the permit includes heat pump installation (true/false). | Boolean |
| HVAC | Indicates whether the permit includes HVAC work (true/false). | Boolean |
| KITCHEN | Indicates whether the permit includes kitchen work (true/false). | Boolean |
| NEW_CONSTRUCTION | Indicates whether the permit is for new construction rather than a modification to an existing structure (true/false). | Boolean |
| PLUMBING | Indicates whether the permit includes plumbing work (true/false). | Boolean |
| POOL_AND_HOT_TUB | Indicates whether the permit includes pool or hot tub installation (true/false). | Boolean |
| REMODEL | Indicates whether the permit includes remodeling work (true/false). | Boolean |
| ROOFING | Indicates whether the permit includes roofing work (true/false). | Boolean |
| SOLAR | Indicates whether the permit includes solar installation (true/false). | Boolean |
| WATER_HEATER | Indicates whether the permit includes water heater installation or replacement (true/false). | Boolean |
| PROPERTY_YEAR_BUILT | The year the property was originally constructed. | Number |
| PROPERTY_LOT_SIZE | Size of the property lot in square feet. | Number |
| PROPERTY_STORY_COUNT | Number of stories in the primary structure on the property. | Number |
| PROPERTY_UNIT_COUNT | Number of residential or commercial units on the property. | Number |
| PROPERTY_ASSESS_MARKET_VALUE | Assessed market value of the property in USD, as determined by the county assessor. | Number |
| PROPERTY_TYPE | Broad classification of the property (e.g., residential, commercial). | Text |
| PROPERTY_TYPE_DETAIL | More granular property type classification (e.g., Single Family, Multi-Family, Commercial Office). | Text |
| PROPERTY_BUILDING_AREA | Total building area of the structure in square feet. | Number |
| PROPERTY_LEGAL_OWNER | Legal name(s) of the property owner(s) as recorded in public records. | Text |
| PROPERTY_OWNER_TYPE | Classification of the property owner (e.g., individual, LLC, trust, corporate). | Text |
| PROPERTY_CENSUS_TRACT | Census tract identifier for the property, used for demographic and geographic analysis. | Text |
| PROPERTY_CONGRESSIONAL_DISTRICT | The U.S. Congressional district number in which the property is located. | Text |
| CONTRACTOR_ID | Internal identifier for the individual contractor associated with the permit. | Text |
| CONTRACTOR_GROUP_ID | Internal identifier for the contractor's company or group. | Text |
| FIRST_SEEN_DATE | Date the permit record was first observed or ingested into the dataset. | Date |
| _META_LOADED_AT | Timestamp indicating when the record was loaded into the data warehouse. | Timestamp |
| _META_SOURCE_FILE_NAME | Name of the source file from which the record was ingested, used for data lineage and auditing. | Text |

### Freedom Forever
| Variable | Description | Datatype |
|---|---|---|
| CONTRACTOR_NAME | Name of the company that filed the permit / did the solar installation | Text | 
| PROJECT_ADDRESS | The address of the installation | Text | 
| INSTALL_DATE | When the project is listed to be installed | Timestamptz
