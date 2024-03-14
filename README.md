## FATCAT and MDPI projects
## FATCAT:
  - downloading data from the open access database, storing PDFs, generating txt and bibfiles (metadata), storing all to the database, and running a web application on the top of it
## MDPI:
  - scraping data from the MDPI, generating bibfiles (metadata) and running a web application on top of it
 --- 
## FATCAT description
This project contains two scripts: **app_fatcat.py** and **main.py**.

- **main.py**: This project is a Python script for downloading PDFs of academic papers from URLs stored in a PostgreSQL database. It also generates BibTeX entries for the downloaded papers and stores the processed data in a SQLite database.

- **app_fatcat.py**: This project is a Streamlit application for analyzing data stored in a SQLite database related to academic papers. It provides statistics and visualizations on various attributes of the papers, such as download status, publication year, and publisher.

#### Project Structure

- **main.py**

1. Ensure you have Python installed on your system.
2. Install the required Python packages using `pip install -r requirements.txt`.
3. Modify the PostgreSQL connection details and other configurations in `pdf_downloader.py` if necessary.
4. Run the script using `python pdf_downloader.py --filter_values="<value>"`, where `<value>` is the filter value for the PostgreSQL query.
   
- **app_fatcat.py**

1. Ensure you have Python installed on your system.
2. Install the required Python packages using `pip install -r requirements.txt`.
3. Run the FATCAT application using `streamlit run fatcat_app.py`.
4. Access the application via the provided URL.


## MDPI description

## Description
This repository contains two Python files: **MDPI_paper_download.py** and **app.py**.

- **MDPI_paper_download.py**: This file contains the backend logic for scraping articles from MDPI website. It defines a class `MDPIArticleScraper` with methods for extracting links, downloading PDFs, finding metadata, generating BibTeX IDs, and writing BibTeX files. The `scan_urls` method iterates through the specified range of years and pages, extracts article links, downloads PDFs, and saves metadata in BibTeX format.

- **app.py**: This file contains a Streamlit application for scraping articles from MDPI (Multidisciplinary Digital Publishing Institute) website. It allows users to configure the scraper parameters such as base URL, year range, file path, page count, and starting page. The application then scrapes articles from the specified range of years and saves PDFs and BibTeX files locally.


#### Project Structure

- **MDPI_paper_download.py**

1. Ensure you have Python installed on your system.
2. Open the file and specify the scraper parameters such as `base_url`, `year_from`, `year_to`, `page_count`, `file_path`, and `page`.
3. Run the script using `python MDPIArticleScraper.py`.

- **app.py**

1. Ensure you have Python installed on your system.
2. Install the required Python packages using `pip install -r requirements.txt`.
3. Run the Streamlit application using `streamlit run MDPI_paper_download.py`.
4. Configure the scraper parameters in the sidebar and click "Start Scraping" to initiate the scraping process.
