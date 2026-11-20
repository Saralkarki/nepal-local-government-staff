# Extension agents data workflow for Nepal

1. Muncipality and rural municipality url's were defined for scraping the data from MUAN
   sources : https://muannepal.org.np/municipality-profiles/
   and https://mofaga.gov.np/local-contacts
   https://mofaga.gov.np/local-contacts?page={page}

2. The data saved as
   - updated_gaupalika_contacts.xlsx (Rural Municipality)
   - updated_Muan_contact.xlsx (Municipality)

3. This data was then used to -

- Scrape data from URLs present in the updated_muan_contact.xlsx
- And scrpae data from the urls in the updated_gaupalika_contacts.xlsx

Files : Extract_table_from_url_gaupalika.ipynb
extract_table_from_url_muni.ipynb
(These are old working codes from local system make changes accordingly )

- The clean data was exported as final*combined_data*<name>\_cleaned.xlsx (for gauplaika and municipality)

4. The clean data though did not have the Province and District names thus they were added.

5. Standardize District and Municipality/Rural Municipality names in English, translating values that are currently in Nepali or a mix of English and Nepali.

6. Standardize other data points that are currently in Nepali or a mix of English and Nepali into English.

7. Add Province Code and District Code to support GIS shapefile mapping.

8. Publish the combined workbook on GitHub Pages for download. (Completed.)

9. Add filters to the GitHub Pages site.

10. Add maps to the GitHub Pages site using the province and district GIS codes.
