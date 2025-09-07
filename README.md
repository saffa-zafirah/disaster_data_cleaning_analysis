# Cleaning Data and Transformation: Disaster Dataset (BNPB records)
This project focuses on data cleaning and exploratory analysis using Microsoft Excel, based on the dataset from Kaggle: Indonesia Natural Disaster Dataset (BNPB Records).  The workflow includes handling inconsistent data formats, standardizing categorical variables, removing duplicates, and building pivot for further analysis.

# Documenting Issues Log
![Alt_text](https://github.com/saffa-zafirah/disaster_data_cleaning_analysis/blob/main/issue%20log.jpg)

# Steps
1. Checking and removing any duplicates
   Tool used: IF functions to show duplicated row count. Or directly click "remove duplicates".
   =IF(COUNTIFS(A:A;A3;B:B;B3;C:C;C3;...)>1;"Duplicate";"Unique")

   Outputs and Insights:
   - from 28.773 records of disasters, 329 duplicate records. 28.444 unique values remain.
  
2. Changing disaster type into some categories
   Tool used: IF function and pivot table
   - Klimatologi (cuaca ekstrem, kekeringan)
   - Hidrologi (banjir)
   - Meteorologi (karhutla, tanah longsor, puting beliung)
   - Geofisik (erupsi gunung api, letusan, gempa bumi, tsunami, gelombang pasang)

=IF(OR(E2="Cuaca Ekstrem";E2="Kekeringan");"Klimatologi";IF(OR(E2="Banjir");"Hidrologi";IF(OR(E2="Kebakaran Hutan Dan Lahan";E2="Tanah Longsor";E2="Putting Beliung");"Meteorologi";"Geofisik")))

Output and Insights

![Alt_text](https://github.com/saffa-zafirah/disaster_data_cleaning_analysis/blob/main/pivot_disaster_type.jpg)
- Most disasters in Indonesia between 2018-2024 are hydrological, dominated by floods.

3. Changing number of columns into ranges
   Tool used: VLOOKUP
   =VLOOKUP(N2;tabel_referensi!$A$2:$B$5;2;TRUE)
![Alt_text](https://github.com/saffa-zafirah/disaster_data_cleaning_analysis/blob/main/tabel_referensi_vlookup.jpg)

Output and Insights:
![Alt_text](https://github.com/saffa-zafirah/disaster_data_cleaning_analysis/blob/main/before-after_number%20into%20range.jpg)



