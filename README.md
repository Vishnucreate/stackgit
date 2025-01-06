# stackgit
# AI-Powered Google Search and Summarization Tool

## Overview
This project combines the power of the **Google Search API** and **OpenAI's GPT** to create a streamlined search assistant for developers. The tool extracts the top 10 search results for a given query, summarizes the content, and provides actionable insights—all in a single step. It's designed to save time and effort, particularly for developers troubleshooting issues or researching topics.

## Features
- **Efficient Search:** Uses the free Google Search API to fetch the top 10 most relevant results.
- **Automated Summarization:** Leverages OpenAI's GPT model to summarize search results into concise, actionable insights.
- **Real-Time Updates:** Provides up-to-date information by sourcing data from Google, GitHub, and Stack Overflow.
- **Cost-Effective:** The Google Search API is free, and the only cost is for AI-powered summarization at just $1 per request.

## Installation

1. Clone the repository:
   ```bash
   git clone https://github.com/Vishnucreate/stackgit.git
   cd stackgit
   ```

2. Install the required Python libraries:
   ```bash
   pip install openai requests
   ```

3. Ensure you have valid API keys for Google Search and OpenAI:
   - [Google Search API Key and CX](https://developers.google.com/custom-search/v1/introduction)
   - [OpenAI API Key](https://platform.openai.com/account/api-keys)

## Usage

1. Replace the placeholders in the code with your API keys:
   ```python
   GOOGLE_API_KEY = "your_google_api_key"
   CX = "your_google_cx"
   OPENAI_API_KEY = "your_openai_api_key"
   ```

2. Run the script:
   ```bash
   python your_script_name.py
   ```

3. Enter a query when prompted:
   ```plaintext
   Enter your Python error message or query: AttributeError: module 'openai' has no attribute 'error'
   ```

4. View the extracted search results and the AI-generated summary.

## Sample Output

### Query
```plaintext
AttributeError: module 'openai' has no attribute 'error'
```

### Extracted Results
1. **Title:** python - AttributeError: module 'openai' has no attribute 'error' - Stack Overflow  
   **Snippet:** Nov 20, 2023 ... I am strangely getting the above error. My OpenAI version is 1.3.3 and langchain 0.0.301, and python 3.8...  
   **Link:** [Stack Overflow](https://stackoverflow.com/questions/77513190/attributeerror-module-openai-has-no-attribute-error)

2. *(Other results follow similarly...)*

### Summary
```
The search results indicate that users have encountered the error "AttributeError: module 'openai' has no attribute 'error'" while working with the OpenAI library in Python. The issue seems to be related to changes or updates in the OpenAI module, leading to the 'error' attribute being removed or renamed in some cases. Users have tried troubleshooting solutions such as checking documentation, updating the library, uninstalling and reinstalling, and adjusting code parameters. The error message has been reported in various contexts, such as chat completions, rate limit errors, and API usage.
```

## Requirements
- Python 3.8+
- Libraries: `openai`, `requests`
- Valid API keys for Google Search and OpenAI.

## How It Works
1. **Search Google:** The script sends the query to the Google Search API and fetches the top 10 results.
2. **Extract Data:** Extracts the titles, snippets, and links from the raw JSON response.
3. **Summarize Results:** Uses OpenAI's GPT to summarize the results into a concise, user-friendly format.

## Troubleshooting
- **Issue:** `AttributeError: module 'openai' has no attribute 'ChatCompletion'`  
  **Solution:** Ensure you're using the latest version of the OpenAI library. Update with:
  ```bash
  pip install --upgrade openai
  ```

- **Issue:** `Error with Google Search API: ...`  
  **Solution:** Verify your Google API key and CX configuration in the script.

## Contribution
Contributions are welcome! Feel free to fork the repository and submit pull requests with improvements.

## License
This project is licensed under the MIT License. See the `LICENSE` file for details.

## Contact
For any issues or feature requests, please open an issue in the [GitHub repository](https://github.com/Vishnucreate/stackgit.git).
