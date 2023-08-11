# Capstone-Project--SponsorMotion
Welcome to the SponsorMotion Data Ingestion Optimization project repository! 

Our goal is to optimize the data ingestion process of SponsorMotion, a data consulting company specializing in a comprehensive database of healthcare-related events in the United States. This project focuses on improving scalability and effective cost optimization, as well as establishing automated data quality control processes to identify problematic or duplicate records. This repository contains the necessary resources, source code, and documentation for the project. Our goal is to help streamline these processes and drive advancements in event sponsorship within the healthcare industry in the United States. 

###  How to use the Final Notebook SponsorMotion

-  Once you have imported the numpy and pandas libraries in your notebook, the second cell is responsible for importing the provided events dump dataset from the company. To use a different dataset, simply update the dataset's name in the code by specifying the correct location of the new dataset.

In the notebook's 15th cell, you'll find a data frame named 'filtered_data' that is configured to filter data specifically for the states of Florida (FL) and Nevada (NV). This is designed to showcase the algorithm's functionality within these two states. Should you wish to work with different states, you can easily modify this filter by replacing the state names accordingly.

-  In case you prefer to execute the code for all states without applying any filters, you can achieve this by substituting the code in cell 15 with the following line:

                               filtered_data = ordered_data.copy()

This will ensure that the algorithm runs on the entire dataset without any state-specific filters.

-  Within cell 23 of the notebook, you will encounter the code responsible for executing the fuzzy match operation. The threshold for determining a successful match is pre-set to 75, a value that has been determined as optimal through rigorous testing of outcomes. Should you wish to tailor the threshold to a different value, you have the flexibility to modify this number according to your preferences. However, unless you specifically intend to adjust this threshold, it is recommended to retain the default value of 75 for consistent and reliable results.

-  The final output is exported as a CSV file in the last row of the final cell. The user can change the name and location to export the file in the desired manner. The final output has 2 additional columns: 
'flagged_duplicates_numbers': The column that represents the duplicates identified by the code by giving a unique number to each set of duplicates.
'human_verification_needed':  This will indicate if that record needs further verification. It will appear as "yes" if the records have similar names but different start dates (+ or - 1 day) and it will appear as "no" if the records have similar names and same dates.

For questions, issues, or further information, please reach out to the project maintainers or create a new issue in the repository.
rohanc@bu.edu, sarmadk@bu.edu, vtorresg@bu.edu
