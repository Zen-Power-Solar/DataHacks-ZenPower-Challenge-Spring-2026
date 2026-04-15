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

### Freedom Forever

