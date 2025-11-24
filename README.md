# Botanical Species Web Scraper

A Python-based web scraping project that collects botanical species data from Wikipedia, focusing on four major plant genera: Pinus, Rosa, Iris, and Eucalyptus.

## Overview

This Jupyter notebook scrapes Wikipedia pages to extract comprehensive information about plant species, including scientific names, common names, family classifications, and native regions. The data is organized into a structured pandas DataFrame for easy analysis and export.

## Features

- **Multi-genus scraping**: Collects data from four plant genera (Pinus, Rosa, Iris, Eucalyptus)
- **Comprehensive data extraction**: Captures scientific names, common names, genus, family, plant type, and native regions
- **Data cleaning and organization**: Structures raw HTML data into a clean, analyzable format
- **Unique identification**: Assigns unique IDs to each plant species
- **Export functionality**: Saves data to CSV format for further use
- **Visualization capabilities**: Includes matplotlib for potential data visualization

## Data Collected

The scraper extracts **1,623 species** across four genera:
- **Pinus** (Pine trees): 25 species
- **Rosa** (Roses): 332 species
- **Iris** (Irises): 269 species
- **Eucalyptus**: 997 species

## Dataset Structure

The resulting dataset includes the following columns:

| Column | Description |
|--------|-------------|
| Plant_ID | Unique identifier for each species |
| Scientific_Name | Latin/scientific name of the species |
| Common_Names | Common name(s) or additional information |
| Genus | Taxonomic genus classification |
| Family | Taxonomic family classification |
| Plant_Type | General plant category (Tree, Shrub, Perennial) |
| Native_Region | Geographic origin or native habitat |

## Requirements

```python
requests
beautifulsoup4
pandas
matplotlib
```

## Installation

1. Clone this repository:
```bash
git clone https://github.com/yourusername/botanical-webscraper.git
cd botanical-webscraper
```

2. Install required packages:
```bash
pip install requests beautifulsoup4 pandas matplotlib
```

## Usage

1. Open the Jupyter notebook:
```bash
jupyter notebook BotanicalCode.ipynb
```

2. Run all cells sequentially to:
   - Import necessary libraries
   - Set up headers for web requests
   - Define genera and their taxonomic classifications
   - Scrape Wikipedia pages for species data
   - Process and clean the collected data
   - Export to CSV format

## Code Structure

### 1. Library Imports
Imports essential libraries including requests, BeautifulSoup, pandas, and matplotlib.

### 2. Header Configuration
Sets up user-agent headers to ensure successful HTTP requests.

### 3. Genus Dictionary
Defines target genera with their corresponding family and plant type classifications.

### 4. Web Scraping Loop
Iterates through Wikipedia pages, extracting species information from list items containing italic (scientific name) formatting.

### 5. Data Processing
Converts scraped data into a pandas DataFrame with structured columns.

### 6. Data Export
Saves the cleaned dataset to a CSV file for preservation and sharing.

## Ethical Considerations

- **Respectful scraping**: Includes `time.sleep(1)` delays between requests to avoid overwhelming Wikipedia servers
- **User-agent identification**: Uses proper headers to identify the scraper
- **Public data**: Only accesses publicly available Wikipedia content
- **Educational purpose**: Designed for learning and research purposes

## Output

The script generates a CSV file containing all scraped botanical data, which can be used for:
- Botanical research and analysis
- Educational projects
- Database population
- Species distribution studies
- Taxonomy visualization

## Limitations

- Data quality depends on Wikipedia article formatting
- Some entries may have incomplete information (marked as "N/A")
- Common names may include additional descriptive text
- Native region data varies in specificity

## Acknowledgments

- Data sourced from Wikipedia
- Built with Python, BeautifulSoup, and pandas

## Disclaimer

This tool is for educational and research purposes. Please respect Wikipedia's terms of service and scraping guidelines. Always verify scraped data against original sources for accuracy.
