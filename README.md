# Restaurant-Chatbot
Installation
Create an environment
Whatever you prefer (e.g. conda or venv)

mkdir myproject
$ cd myproject
$ python3 -m venv venv
Activate it
Mac / Linux:

. venv/bin/activate
Windows:

venv\Scripts\activate
Install PyTorch and dependencies
For Installation of PyTorch see official website.

You also need nltk:

pip install nltk
If you get an error during the first run, you also need to install nltk.tokenize.punkt: Run this once in your terminal:

$ python
>>> import nltk
>>> nltk.download('punkt')
Usage
Run

python train.py
This will dump data.pth file. And then run

python chat.py
Customize
Have a look at intents.json. You can customize it according to your own use case. Just define a new tag, possible patterns, and possible responses for the chat bot. You have to re-run the training whenever this file is modified.

{
  "intents": [
    {
      "tag": "greeting",
      "patterns": [
        "Hi",
        "Hey",
        "How are you",
        "Is anyone there?",
        "Hello",
        "Good day"
      ],
      "responses": [
        "Hey :-)",
        "Hello, thanks for visiting",
        "Hi there, what can I do for you?",
        "Hi there, how can I help?"
      ]
    },
    ...
  ]
}
