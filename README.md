# Nepal Government Officials Data

I started this project while searching for agricultural officials across Nepal and trying to find out who worked where. I compiled URL lists for municipalities and rural municipalities, then scraped the public staff pages linked from those lists. For example, one source is [Belauri Municipality's Our Team page](https://belaurimun.gov.np/our-team/). The project grew to collate available public staff listings from local governments in one place, making them easier to find.

The goal is to organize the collected information into a useful dataset, make the workflow understandable to other users, and provide the combined workbook for download from a GitHub Pages site.

## Project contents

- `notebooks/extract_table_from_url_gaupalika.ipynb` — collect staff tables from rural municipality websites.
- `notebooks/extract_table_from_url_muni.ipynb` — collect staff tables from municipality websites.
- `notebooks/merging_province_district_with_staff_data.ipynb` — combine scraped staff data with local-government information.
- `notebooks/combine_final_staff_data.ipynb` — standardize selected headers and concatenate the municipality and rural-municipality datasets.
- `docs/index.html` — the GitHub Pages download page.
- `docs/combined_staff_final.xlsx` — the combined workbook published for download.
- `data/geodata/` — province and district reference tables.
- `steps.md` — project workflow and remaining tasks.

The source contact and website URL lists in `data/Gaupalika_Municipality_url_list/` are included. Intermediate staff workbooks remain local; the combined workbook is published as the project download.

## Running the notebooks

The notebooks are currently the workflow; this project does not yet include a one-command runner or a dependency manifest. Open the project in Jupyter and run notebooks from the `notebooks/` directory, since their relative paths expect that working directory. The scraper notebooks make HTTP requests to the source websites. Input workbooks referenced by the notebooks must be prepared locally and are not shipped in this repository.

The combined workbook is written locally to `data/Officials_combined/Combined_staff_final.xlsx` by `combine_final_staff_data.ipynb`. The published copy is `docs/combined_staff_final.xlsx`; replace it when releasing an updated dataset.

## Data notes

Staff data was collected from the municipality and rural-municipality URLs in the project's source lists, including staff pages on individual local-government websites. The collected pages and tables may change, and the resulting dataset can be incomplete, inconsistent, or out of date. The workbook is an aggregation of public source-site information, not an official government publication. Check each record against its `source_url` when accuracy matters.

The downloadable workbook is a point-in-time aggregation of information listed on public source pages, not an official government publication. Source pages and records can change; use each record's `source_url` to verify current information. Notebook outputs are cleared so the repository does not duplicate the dataset in multiple places.

## Sources

- [Municipality Association of Nepal (MUAN) municipality profiles](https://muannepal.org.np/municipality-profiles/)
- [Ministry of Federal Affairs and General Administration (MoFAGA) local contacts](https://mofaga.gov.np/local-contacts)
- Individual municipality and rural municipality websites listed in the [rural-municipality (Gaupalika) URL workbook](data/Gaupalika_Municipality_url_list/updated_gaupalika_contacts.xlsx) and the [municipality URL workbook](data/Gaupalika_Municipality_url_list/updated_Muan_contacts.xlsx), such as [Belauri Municipality's Our Team page](https://belaurimun.gov.np/our-team/).

## Project status

The initial collection, cleanup, and province/district-name enrichment are complete. The combined workbook is available from the [GitHub Pages site](https://saralkarki.github.io/nepal-local-government-staff/). Remaining work includes standardizing geographic and other mixed-language fields in English, adding province and district codes for GIS mapping, and later adding filters and maps to the Pages site. See [steps.md](steps.md).

## License

No license has been selected yet. A license should be added before describing this repository as open source.
