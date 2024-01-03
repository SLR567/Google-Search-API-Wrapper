# Google Search API Wrapper

## Overview
The Google Search API Wrapper is a versatile tool designed to facilitate seamless interaction with the Google Custom Search JSON API. This project enables users to effortlessly perform advanced web and image searches, harnessing the power of Google's robust search technology. The script is particularly useful for applications that require automated search functionalities, such as data mining, content aggregation, academic research, or any project that benefits from structured search results.

## Key Features
- Web and image search functionality using Google Custom Search JSON API.
- Customizable search queries and result limits.
- Formatted search results including titles, links, snippets, and images.
- Error handling for missing credentials or invalid queries.

## Prerequisites
- `Python 3.x`
- An API Key for Google's Custom Search JSON API and a `CX` id for Google's Programmable Search Engine

## Installation
To use this wrapper, clone the repository and install dependencies:
```bash
git clone https://github.com/RMNCLDYO/Google-Search-API-Wrapper.git
cd Google-Search-API-Wrapper
pip install -r requirements.txt
```

## Dependencies
The following Python packages are required:
- `requests`
- `python-dotenv`

## Setup
Set your Google Custom Search JSON API credentials (API key and CX) as environment variables `api_key` and `cx`.

### Obtaining Google Custom Search API Credentials

#### Obtaining an API Key
1. Visit the [Google Developers Introduction page](https://developers.google.com/custom-search/v1/introduction) for the Custom Search JSON API.
2. Scroll down to the middle of the page and click on 'Get a Key' to obtain your API key.
3. Use this key in your application by appending the query parameter `api_key=yourAPIKey` to all request URLs.

#### What is a Programmable Search Engine?
A Programmable Search Engine allows you to search google via the API, using Google's core search technology. You can customize it extensively, including the look and feel, search features, and even link it with Google Analytics for user behavior insights.

#### Creating a Programmable Search Engine
Before using the Google Custom Search API, you need to create a Programmable Search Engine. Follow these steps:

1. Visit the [Control Panel](https://programmablesearchengine.google.com/controlpanel/all).
2. Name your search engine and specify what to search:
   - Choose specific sites or the entire web.
3. Set your search settings, such as enabling image search and/or SafeSearch.
4. Complete the reCAPTCHA verification and create your search engine.
5. Once created, find your Search Engine ID (cx parameter) in the Overview page's Basic section.

## Usage

#### Text Search Example

```python
from google_search_api import GoogleSearchAPI

# Initialize the GoogleSearchAPI class
request = GoogleSearchAPI()

# Perform a text search and retrieve results
response = request.response(method='text', max_results=5, query='Python')

# Print the formatted search results
print(response)
```

#### Image Search Example

```python
from google_search_api import GoogleSearchAPI

# Initialize the GoogleSearchAPI class
request = GoogleSearchAPI()

# Perform an image search and retrieve results
response = request.response(method='image', max_results=5, query='Nature')

# Print the formatted search results
print(response)
```

## Contributing
Contributions are welcome. Please follow the guidelines in our [CONTRIBUTING.md](.github/CONTRIBUTING.md).

## Reporting Issues
Report issues via the GitHub issue tracker.

## License
Licensed under the MIT License - see the [LICENSE](LICENSE) file for details.
