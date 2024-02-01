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

## Setting up the .env file

### 1. Setting up the Reddit app

1.1. First, you will need to get some credentials from Reddit. These values are:

- REDDIT_CLIENT_ID 
- REDDIT_CLIENT_SECRET 
- REDDIT_USERNAME 

You can get these values from [here](https://www.reddit.com/prefs/apps).

1.2. Note that you need to be logged in to your Reddit account. This account cannot be a Google account or any other social login. It must be a Reddit account with a username and password. The next step will be the most essential in this entire section. Avoid any errors here!

1.3. Head over to [this page](https://www.reddit.com/prefs/apps). Once you are here, you should scroll down and click a button saying create another app... (it could be different if it's your first app). Once you click it, you should see:

![Create Application](https://reddit-video-maker-bot.netlify.app/assets/images/create-application-928c440fc080838a593ca150b97c79ea.png)

- Name: you can put in any name, for example: reddit-bot
- Radio Buttons: where it shows you the three radio buttons, pick the third one (script).
- Description: put in anything, it does not matter.
- About URL: link any webpage like https://google.com.
- Redirect URI: link any webpage like https://google.com.

1.4. Great, you created the app! Now you need to give the values to the bot.

![App Credentials](https://user-images.githubusercontent.com/66544866/173240642-af00257e-4414-4a57-a3be-24443ee7c29f.png)

The text under "personal use script" is your REDDIT_CLIENT_ID, the text right next to SECRET is your REDDIT_CLIENT_SECRET (DO NOT SHARE THIS WITH ANYONE).

The text where it says developers is your REDDIT_USERNAME, and REDDIT_PASSWORD is your Reddit account's password. Your information is not logged.

Once you got all your values fill them in into the .env file that should now be looking like the following:

```
REDDIT_USER_AGENT= value ✅
REDDIT_CLIENT_ID= value ✅
REDDIT_CLIENT_SECRET= value ✅

DEEPL_AUTH_KEY=

OPENAI_API_KEY=
```

> Content adapted from [Reddit Video Maker Bot Documentation](https://reddit-video-maker-bot.netlify.app/docs/configuring)


### 2. Setting up the OpenAI Key

2.1. To get your OpenAI key, you need to sign up on the [OpenAI website](https://beta.openai.com/signup/). After signing up, you can find your API key in the API section of the OpenAI Dashboard.

2.2. Once you have your OpenAI API key, enter it into the .env file:

```
REDDIT_USER_AGENT= value ✅
REDDIT_CLIENT_ID= value ✅
REDDIT_CLIENT_SECRET= value ✅

DEEPL_AUTH_KEY= 

OPENAI_API_KEY= value ✅
```
### 3. Setting up the DeepL Key

3.1. To get your DeepL key, you need to create a free account on the [DeepL website](https://www.deepl.com/pro#developer). After creating an account, you can find your API key in your account settings under the "Plan & API" section.

3.2. Once you have your DeepL API key, enter it into the .env file:
```
REDDIT_USER_AGENT= value ✅
REDDIT_CLIENT_ID= value ✅
REDDIT_CLIENT_SECRET= value ✅

DEEPL_AUTH_KEY= value ✅

OPENAI_API_KEY= value ✅
```
Replace `value ✅` with the respective values you received from Reddit, OpenAI and DeepL respectively.

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