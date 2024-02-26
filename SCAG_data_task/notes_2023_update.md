# Notes on Updating code for new 2023 5-year ACS PUMS data:
1. Go to the end of the first code chunk named `setup` (code line #288), un-comment this last section and run so that new file paths will be written when the `setup` code chunk is evaluated.
2. Go to the end of the second code chunk named `acs_data_dwnld` (code line #377), un-comment this last section and run so that the new housing and person level data is downloaded and saved/renamed to the correct folders. *NOTE: You will have to confirm that the URLs for each of the housing and person level data in the ACS PUM FTP are correct, the year is updated to 2023 which may be the only necessary change.*
3. Go to the code chunk named `ACS 2023 FTP data` (code line #731), un-comment this whole code chunk and after steps 1 and 2, this will merge, clean and save the 2023 data. *NOTE: You will have to confirm that new 2023 5-year ACS PUMS data doesn't have any large changes and will have to check to see how the 2023 data calculate PUMA's, if it is the same as the 2022 data, this code chunk will work as written (2022 data had PUMA10 for the years 2018-2021, and PUMA20 for 2022, this code combines the two columns into a new column named `PUMA`.*
4. Finally, go to the code chunk that reads in the clean data before making the tables, which is named `read recode SCAG data`, go to code line #883, un-comment this line and comment out the previous other two lines that would read in the 2021 and 2022 data like the in-line code comments describe.

This should be all that is necessary to update the code to create output tables for next year's (beginning of 2024) 2023 5-year ACS PUMS data release.