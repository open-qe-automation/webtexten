# WEBTEXTEN - Web Text Extraction Node

WEBTEXTEN is a versatile web text extraction application designed to crawl websites, extract textual content from web pages and PDFs, and save the extracted content into organized text files. This tool is ideal for web scraping tasks where large volumes of web data need to be processed and stored efficiently.

Key Features
- Web Crawling: Traverses web pages starting from a given URL, following links within the same domain to gather content comprehensively.
- Content Extraction: Extracts text from HTML elements such as paragraphs and headers, as well as from PDF files.
- File Conversion and Saving: Converts extracted content into text files, ensuring it is stored in a structured and accessible format.
- URL Filtering and Throttling: Implements rules to skip irrelevant URLs and throttles requests to avoid overloading web servers.
- Logging and Reporting: Maintains detailed logs of the crawling and extraction process, including any errors encountered.

## Git Repositories
- https://github.com/open-qe-automation/texten.git
- https://github.com/open-qe-automation/webtexten.git
- https://github.com/open-qe-automation/chunken.git
- https://github.com/open-qe-automation/datamyn.git

## Related Packages
- https://github.com/open-qe-automation/package.utils.git
- https://github.com/open-qe-automation/package.data.loaders.git
- https://github.com/open-qe-automation/package.helpers.git

## Table of Contents
- [Prerequisites](#prerequisites)
- [Installation](#installation)
- [Usage](#usage)
- [Configuration](#configuration)

## Prerequisites

Before you begin, ensure you have met the following requirements:
- Python 3.12 or later
- pip

## Installation

1. **Clone the repository:**

    ```bash
    git clone https://github.com/open-qe-automation/webtexten.git
    cd webtexten
    ```

2. **Set up a virtual environment:**

    ```bash
    python -m venv venv
    source venv/bin/activate   # On Windows, use `venv\Scripts\activate`
    ```

3. **Install the dependencies:**

    ```bash
    pip install -r requirements.txt
    ```

    For local development, use dev-requirements.txt:
    ```bash
    pip install -r dev-requirements.txt
    ```

## Usage

To run the WEBTEXTEN application, use the following command:

```bash
python app.py
```

### Configuration

The configuration is managed through a `config.json` file:

```json
{
  "input_directories": ["../share/input"],
  "text_output_directory": "../share/text_output",
  "hash_file_path": "file_hashes.json",
  "scheduler_interval": 60
}
```

## Input

WEBTEXTEN reads URLs from files in the input directory. Each file can contain multiple URLs (one per line).