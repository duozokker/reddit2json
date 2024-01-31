# reddit2json

reddit2json is a Python script designed to process a list of Reddit post URLs, converting them into a JSON format. The script offers additional functionalities, including the ability to translate the content of Reddit posts using DeepL, and the capability to modify the content through custom OpenAI GPT calls.

## Table of Contents

- [Installation](#installation)
- [Usage](#usage)
- [License](#license)

## Installation

1. Clone the repository:
```sh
git clone https://github.com/duozokker/reddit2json.git
```
2. Navigate to the project directory:
```sh
cd reddit2json
```
3. Install the required Python packages:
```sh
pip install -r requirements.txt
```
4. Rename `example.env` to `.env` and fill in your API keys and other settings.

## Usage

Run the script with a list of Reddit post URLs as arguments:
```sh
python reddit2json.py url1 url2 url3
```
The script will process the posts and output a JSON file for each post.

## Example Files

- `example-reddit-post.txt`: This file contains an example of a Reddit post that can be processed by the script.
- `example-video.json`: This file shows the JSON output format of the script.

## License

This project is licensed under the terms of the [LICENSE](LICENSE) file.

## Contributing

Contributions are welcome! Please feel free to submit a Pull Request.