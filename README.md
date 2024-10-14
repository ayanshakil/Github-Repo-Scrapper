# GitHub Repo Scraper

## Overview
The GitHub Repo Scraper is a Python tool designed to fetch code snippets from a specified GitHub repository. It utilizes the GitHub API to access repository contents and clones the repository locally to extract relevant code files. The tool creates a structured dataset in JSON format, which can be used for training machine learning models or other applications.

## Features
- Fetches repository data from GitHub using the GitHub API.
- Clones the specified repository to your local machine.
- Extracts code snippets from specific file types (.kt, .gradle, .xml, .txt, .md, .res, .pro, .properties, .json).
- Creates a dataset in JSON format with input-output pairs.
- Easy to use and extend for various purposes.

## Requirements
- Python 3.x
- `requests` library (install via `pip install requests`)
- `git` installed on your machine for cloning repositories

## Usage
1. Clone this repository to your local machine or download the script.
2. Open the script in your favorite text editor or IDE.
3. Replace `user_name` and `repo_name` with the respective GitHub username and repository name in the main execution section.
4. Run the script using the command:

   ```bash
   python github_repo_scraper.py
5. The tool will clone the specified repository, extract code snippets, and create a training_data.json file in the current directory.

## Example
To scrape a repository owned by your_username named your_repo, modify the script:
```pyhton
   owner = 'your_username'
   repo_name = 'your_repo'
   ```


## Functions
- `fetch_repo_data(repo_url)`: Fetches repository contents from the GitHub API.

- `clone_repo(repo_url)`: Clones the specified GitHub repository.

- `extract_code_snippets(path)`: Walks through the cloned repository and extracts code snippets from relevant files.

- `create_dataset(snippets)`: Creates a dataset from the extracted snippets, formatted as input-output pairs.


## Dataset Format
The resulting training_data.json file will contain a list of JSON objects, each with the following structure:
   ```json
   [
       {
           "input": "code snippet here",
           "output": "your expected response"
       }
   ]
```



## Contributing
Contributions are welcome! Feel free to submit issues or pull requests for improvements or new features.

## License
This project is licensed under the MIT License. See the LICENSE file for more details.

## Contact
For any questions or inquiries, please contact Your ayanshakil17@gmail.com.




