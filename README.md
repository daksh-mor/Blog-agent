# Autonomous AI News Agent

This project implements an autonomous AI agent that searches, summarizes, and publishes news content.

## Installation

1.  **Clone the repository:**
    ```bash
    git clone <your_repository_url>
    cd <your_repository_directory>
    ```
2.  **Install the required Python packages:**
    ```bash
    pip install tavily-python requests beautifulsoup4 transformers torch google-api-python-client google-auth-httplib2 google-auth-oauthlib
    ```
3.  **Set up Google Blogger API credentials:**
    * Create a Google Cloud project and enable the Blogger API.
    * Download the `credentials.json` file and place it in the project directory.

## Usage

1.  **Run the script:**
    * The code is structured as a series of python code cells.
    * The first cell install the required packages.
    * The second cell uses the Tavily API to search for news articles based on a query. It then extracts the text content of the articles using BeautifulSoup.
    * The third cell uses a T5 model (from Hugging Face Transformers) to summarize the extracted text and generate a title.
    * The fourth cell authenticates with the Google Blogger API and publishes the summarized content as a new blog post.
    * Run the python code cells in sequential order.
2.  **Authentication:**
    * When the script runs the authentication step, it will open a browser window to authenticate with your Google account. Follow the prompts to grant the necessary permissions.
3.  **Blogger Configuration:**
    * Replace `"7894317275629685509"` with your actual Blogger blog ID in the `create_blog_post` function.
    * Replace `"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"` with your tavily api key.
4. **Running the code**
    * The code was run inside a jupyter notebook environment.

## Code Description

* **`give_content(query)`:**
    * Uses the Tavily API to search for news articles.
    * Extracts the text content from the articles using `requests` and `BeautifulSoup`.
* **`TextSummarizer` class:**
    * Initializes a T5 model and tokenizer.
    * Provides methods for preprocessing text, generating summaries, and generating titles.
* **`authenticate()`:**
    * Authenticates with the Google Blogger API using OAuth 2.0.
* **`create_blog_post(creds, title, content)`:**
    * Publishes a new blog post using the Blogger API.

## Dependencies

* `tavily-python`
* `requests`
* `beautifulsoup4`
* `transformers`
* `torch`
* `google-api-python-client`
* `google-auth-httplib2`
* `google-auth-oauthlib`

## Output

The script will output the URL of the newly created blog post.
