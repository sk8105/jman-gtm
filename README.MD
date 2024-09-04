
# Google Maps Places API Data Fetching Script

This script fetches data from the Google Maps Places API based on a query and retrieves additional details for each place found. The results are then saved to a CSV file.

## Requirements

- Python 3.7+
- Required Python packages:
  - `requests`
  - `pandas`
  - `python-dotenv`

## Setup

### 1. Clone the Repository

If you haven't already, clone the repository containing this script:

```bash
git clone <repository_url>
cd <repository_directory>
```

### 2. Install Required Packages

Install the required Python packages using `pip`:

```bash
pip install requests pandas python-dotenv
```

### 3. Create a `.env` File

Create a `.env` file in the root directory of the project to store your environment variables. This file should contain your Google Maps Places API key and the URLs for the Places API and Place Details API.

Example `.env` file:

```env
API_KEY=your_google_maps_api_key
TEXT_SEARCH_URL=https://maps.googleapis.com/maps/api/place/textsearch/json
DETAILS_URL=https://maps.googleapis.com/maps/api/place/details/json
QUERY= "Here you have to do the prompt"
```

Replace `your_google_maps_api_key` with your actual API key from Google Cloud Platform.

## Usage

### 1. Run the Script

Run the script using Python:

```bash
python script.py
```

### 2. Specify the Query (DOTENV File)

In the script, modify the `QUERY` variable to specify the type of places you're searching for and with location. For example, to search for Lenovo showrooms in Chennai:

```python
query = 'Lenovo showrooms in chennai'
```

### 3. View Results

The script will fetch the places matching your query and retrieve additional details for each place. The results will be displayed in a pandas DataFrame and saved to a CSV file with the current date and query name as the filename.

### 4. CSV Output

The CSV file will be named using the format `YYYYMMDD <query>.csv` and will include the following columns:
- Name
- Address
- Rating
- Total Ratings
- Place ID
- Phone Number
- Website

## Troubleshooting

- **Error Fetching Data**: If the script encounters an error while fetching data, it will print the HTTP status code and error message.
- **Empty DataFrame**: If no results are found for the query, the resulting DataFrame will be empty.

## License

This project is licensed under the #### License.