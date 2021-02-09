**Meta Data Name**: Drug-Related Death Rate  
**Environment**: Health Factors  
**Last Modified**: February 5, 2021  
**Author**: Susan Paykin  

### Data Location: 
Health01 - Policy Scan Environment Report at XX spatial scales. Files can be found [here](https://github.com/GeoDaCenter/opioid-policy-scan/tree/master/Policy_Scan/data_final).
* Health01_C
* Health01_S

### Data Source(s) Description:  

The Underlying Cause of Death data available on [CDC's WONDER database](https://wonder.cdc.gov/) are county-level national mortality and population data spanning the years 1999-2019. Data are based on death certificates for U.S. residents. Each death certificate identifies a single underlying cause of death and demographic data. 

The mortality data are based on information from all death certificates filed in the fifty states and the District of Columbia. Deaths of nonresidents (e.g. nonresident aliens, nationals living abroad, residents of Puerto Rico, Guam, the Virgin Islands, and other territories of the U.S.) and fetal deaths are excluded. Mortality data from the death certificates are coded by the states and provided to NCHS through the Vital Statistics Cooperative Program or coded by NCHS from copies of the original death certificates provided to NCHS by the State registration offices. For more information, see [CDC](https://wonder.cdc.gov/wonder/help/ucd.html#).

### Description of Data Source Tables: 

Data was aggregated to state and county-levels, including total population and total deaths, for all demographics, times, and places for the period 2009-2018. The ICD-10 codes included as drug-related deaths were as follows:  

**Drug-induced diseases:**
D52.1, D59.0, D59.2, D61.1, D64.2, E06.4, E23.1, E24.2, E27.3, G24.0, G25.1, G25.4, G25.6, G72.0, J70, K03.2, K73, K85.3, L10.5, M10.2, M81.4, M87.1

**Mental/behavioral disorders due to drugs:**
F10-F19 

**Drugs in the blood:**
R78, R82.5, R83.2-R89.2 

**Poisoning of undetermined intent by exposure to drugs:**
X40-44, Y10-Y14, Y50.1 

**Accidental poisoning, intentional self-poisoning:**
X60-X64 

### Description of Data Processing: 

Data was wrangled, cleaned and filtered for only contiguous U.S. states & Washington, D.C. The crude death rate per 100,000 population was calculated by dividing total deaths by population, weighted by 100,000 (death / pop * 100,000). 

### Key Variable and Definitions:

| Variable | Variable ID in .csv | Description |
|:---------|:--------------------|:------------|
| GEOID | GEOID | Unique 5-digit identifier for counties, 2-digit indentifier for states |
| Deaths | deaths | Total deaths from drug-related causes, 2009-2018 |
| Population | pop | Total population |
| Raw mortality rate | rawDeathRate | Raw mortality rate normalized per 100K population |

### Data Limitations: 

County-level and other subnational data representing fewer than ten persons (0-9) are suppressed for year 1989 and later years, including our years of interest 2009-2018. Furthermore, rates may be considered "unreliable" when the death count is less than 20. For more information, see [CDC](https://wonder.cdc.gov/wonder/help/ucd.html#). 

### Comments/Notes:

Data includes 48 contiguous U.S. states and District of Columbia. Does not include Alaska, Hawaii, or U.S. territories FM, GU, MP, PR, VI.