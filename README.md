# Nepal Government Officials Data

This project grew out of a practical question: who works where, especially among agricultural staff? While gathering that information, the project expanded to collect publicly listed staff information from Nepal's municipalities and rural municipalities where it is available.

The goal is to organize the collected information into a useful dataset, make the workflow understandable to other users, and eventually provide an approved combined workbook for download from a GitHub Pages site.

## Project contents

- `notebooks/extract_table_from_url_gaupalika.ipynb` — collect staff tables from rural municipality websites.
- `notebooks/extract_table_from_url_muni.ipynb` — collect staff tables from municipality websites.
- `notebooks/merging_province_district_with_staff_data.ipynb` — combine scraped staff data with local-government information.
- `notebooks/combine_final_staff_data.ipynb` — standardize selected headers and concatenate the municipality and rural-municipality datasets.
- `data/geodata/` — province and district reference tables.
- `steps.md` — project workflow and remaining tasks.

The source contact and website lists in `data/Gaupalika_Municipality_url_list/` are included. Staff workbooks and combined results are kept locally and excluded from the public repository because they contain identifiable staff information. They are not included as downloads in this initial release.

## Running the notebooks

The notebooks are currently the workflow; this project does not yet include a one-command runner or a dependency manifest. Open the project in Jupyter and run notebooks from the `notebooks/` directory, since their relative paths expect that working directory. The scraper notebooks make HTTP requests to the source websites. Input workbooks referenced by the notebooks must be prepared locally and are not shipped in this repository.

The combined workbook is written locally to `data/Officials_combined/Combined_staff_final.xlsx` by `combine_final_staff_data.ipynb`. It is ignored by Git and is not part of the public release.

## Data notes

The collected pages and tables may change, and the resulting dataset can be incomplete, inconsistent, or out of date. The workbook is an aggregation of source-site information, not an official government publication. Check each record against its `source_url` when accuracy matters.

Before publishing staff-level or combined workbooks or their notebook outputs, review the fields and source-site terms and ensure the public release is appropriate. A GitHub Pages download is planned after that review; no staff-level or combined workbook is currently published there.

## Sources

- [Municipality Association of Nepal (MUAN) municipality profiles](https://muannepal.org.np/municipality-profiles/)
- [Ministry of Federal Affairs and General Administration (MoFAGA) local contacts](https://mofaga.gov.np/local-contacts)
- Individual municipality and rural municipality websites listed in the contact workbooks.

## Project status

The initial collection, cleanup, and province/district-name enrichment are complete. Remaining work includes standardizing geographic and other mixed-language fields in English, adding province and district codes for GIS mapping, publishing an approved workbook download, and later adding filters and maps to the Pages site. See [steps.md](steps.md).

## License

No license has been selected yet. A license should be added before describing this repository as open source.
