# Cleaning Data and Transformation: Disaster Dataset (BNPB records)
This project focuses on data cleaning and exploratory analysis using Microsoft Excel, based on the dataset from Kaggle: Indonesia Natural Disaster Dataset (BNPB Records).  The workflow includes handling inconsistent data formats, standardizing categorical variables, removing duplicates, and building pivot for further analysis.

# Documenting Issues Log
![Alt_text](https://github.com/saffa-zafirah/disaster_data_cleaning_analysis/blob/main/issue%20log.jpg)

# Steps
1. disaster type turning into some categories
   - Klimatologi (cuaca ekstrem, kekeringan)
   - Hidrologi (banjir)
   - Meteorologi (karhutla, tanah longsor, puting beliung)
   - Geofisik (erupsi gunung api, letusan, gempa bumi, tsunami, gelombang pasang)
=IF(OR(E2="Cuaca Ekstrem";E2="Kekeringan");"Klimatologi";IF(OR(E2="Banjir");"Hidrologi";IF(OR(E2="Kebakaran Hutan Dan Lahan";E2="Tanah Longsor";E2="Putting Beliung");"Meteorologi";"Geofisik")))
