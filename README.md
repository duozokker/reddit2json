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


## Example Calls

To use the `reddit2json.py` script, you need to pass the method you want to use for processing text. The script supports two methods: `translate` and `chat`.

Here are some example calls:

1. To process Reddit posts using the `translate` method:

```sh
python reddit2json.py --method translate
```

This will translate the content of Reddit posts to german using DeepL.

2. To process Reddit posts using the `chat` method:

```sh
python reddit2json.py --method chat
```

This will modify the content of Reddit posts using OpenAI GPT-3.5 Turbo.

3. To translate the content of Reddit posts to a specific language using the `translate` method:

```sh
python reddit2json.py --method translate --lang ES
```

This will translate the content of Reddit posts to Spanish using DeepL.

Note: The script reads Reddit post URLs from the `reddit-post.txt` file and generates a single JSON file (`video.json`) containing the processed content of all the posts.

## Example Files

- `example-reddit-post.txt`: This file contains an example of a Reddit post that can be processed by the script.
- `example-video.json`: This file shows the JSON output format of the script.

## License

This project is licensed under the terms of the [LICENSE](LICENSE) file.

## Contributing

Contributions are welcome! Please feel free to submit a Pull Request.