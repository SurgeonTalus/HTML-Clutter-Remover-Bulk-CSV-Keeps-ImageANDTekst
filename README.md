```markdown
# URL to HTML Converter

This tool allows you to convert URLs listed in a CSV file to HTML files.
It cleans the HTML content using `readability-lxml` and removes iframes before saving to remove ads

## Features

- Parses URLs from a CSV file.
- Generates filenames based on the URL structure.
- Cleans HTML content to improve readability.
- Removes iframes from the HTML content.
- Saves the cleaned HTML content as `.html` files.
- Adds the source URL as a comment to the saved file using `appscript` for MacOS Finder integration.

![Alt Text](https://github.com/SurgeonTalus/HTML-Clutter-Remover-Bulk-CSV-Keeps-ImageANDTekst/raw/main/ExamplePageFontPrecerved.png)


## Requirements

- Python 3
- `tkinter` for the GUI
- `csv` for CSV file processing
- `re` for regular expression operations
- `requests` for HTTP requests (not used in the provided code, but may be required for future expansions)
- `subprocess` for running shell commands
- `os` for OS-level operations
- `urllib.parse` for parsing URLs
- `bs4` (BeautifulSoup) for HTML parsing
- `readability-lxml` for cleaning HTML content
- `appscript` and `mactypes` for MacOS Finder integration
- Docker for running `singlefile` to save HTML content

## Installation

Before running the script, make sure you have the required packages installed:

```bash
pip install beautifulsoup4
pip install readability-lxml
pip install appscript
```

You also need to have Docker installed and `singlefile` Docker image pulled:

```bash
docker pull singlefile/singlefile
```

## Usage

To use the URL to HTML Converter, follow these steps:

1. Launch the script.
2. Click on the "Browse CSV File" button to select your CSV file containing URLs.
3. Select the directory where you want to save the HTML files.
4. The program will process each URL and save the cleaned HTML content as a file.

## Script Functions

### `generate_filename(url)`

- Parses the given URL and creates a filename based on its components.

### `clean_html(html_content)`

- Cleans the given HTML content using the `readability-lxml` library.

### `remove_iframes(html_content)`

- Removes iframe elements from the given HTML content.

### `save_html(url, save_path)`

- Saves the cleaned HTML content of the given URL to the specified path.

### `process_csv(csv_file, save_path)`

- Processes each URL in the given CSV file and saves the HTML content.

### `browse_file()`

- Opens a file dialog to select a CSV file and a directory to save HTML files.

## GUI

The script uses `tkinter` to provide a simple graphical user interface with a button to browse for a CSV file and a status label to provide feedback.

## License

This project is licensed under the MIT License - see the LICENSE file for details.
```

Replace "Your Name" with your actual name or GitHub username if you want to provide authorship information. Additionally, ensure that you have a LICENSE file in your repository if you mention it in the README.
