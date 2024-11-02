# linkshap3

1) Web Crawling:
The script fetches HTML content from a specified URL, parses it, and extracts all unique hyperlinks.
It supports a configurable crawling depth to limit how deeply the crawler explores links on a website.

2) Concurrency Control:
To enhance performance, the script utilizes goroutines for concurrent fetching of links, controlled by a semaphore to limit the number of simultaneous requests.

3) Filtering and Highlighting:
Users can specify filter words to include or exclude certain links based on their content.
Valid links are highlighted in the output, with specific colors for better visibility.
Password Protection:

4) The script incorporates a password prompt, allowing access to its functionalities only for users who provide the correct password.
Passwords can be stored and loaded from a local file, with the option to check against a remote GitHub-hosted password.
Output Management:

5) All valid links discovered during the crawl are saved to a specified output file.
The script checks if the output file already exists to prevent accidental overwrites.

6) Update Checks:
Before executing its primary functions, the script checks for updates by fetching the latest changes from a specified Git repository.
It executes Git commands to pull any updates if the local script version is out of date.
Error Handling:

The script includes comprehensive error handling, providing user-friendly messages for issues such as invalid URLs, failed fetch requests, and password validation errors.
