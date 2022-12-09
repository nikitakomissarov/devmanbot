#  devmanbot #

## Summary
The script is a aimed to help Devman students with their routine of checking if their tasks are checked. It's generally based on https://dvmn.org/ API, modules are needed you're able to find in requirements.txt.
Cheers.

To use the code below you have to:
1. Check requirements.txt and be sure that your virtenv includes each from needed modules.
2. Take your own tokens from Telegram and Devman, then insert they into .env like:

DEVMAN_TOKEN = '****'

TELEGRAM_TOKEN = '****'.

But DO NOT FORGET to create .env on you local machine first.
Then write something to your bot. After it receive any message from you, it'll be able to retrieve your 'chat_id' and use it in the code automatically.


## Launch and deploying example from windows prompt:

``` C:\Users\big shot>git clone https://github.com/nikitakomissarov/devmanbot
C:\Users\big shot>cd devmanbot
C:\Users\big shot\devmanbot>python  -m venv env
C:\Users\big shot\devmanbot>env\Scripts\activate.bat
(env) C:\Users\big shot\devmanbot>pip install -r requirements.txt

Collecting python-telegram-bot~=13.14
  Using cached python_telegram_bot-13.15-py3-none-any.whl (519 kB)
Collecting python-dotenv~=0.21.0
  Using cached python_dotenv-0.21.0-py3-none-any.whl (18 kB)
Collecting requests~=2.28.1
  Using cached requests-2.28.1-py3-none-any.whl (62 kB)...
.........................................................
(env) C:\Users\big shot\devmanbot>python main.py

The bot's starting, your chat id 279851705
{'request_query': [], 'status': 'timeout', 'timestamp_to_request': 1670624725.8804193}
Your task is not checked yet, continue....
Your task is not checked yet, continue....
``` 


P. S.
If you see that traceback:
``` (env) C:\Users\big shot\devmanbot>python main.py
Traceback (most recent call last):
  File "C:\Users\big shot\devmanbot\main.py", line 8, in <module>
    DEVMAN_TOKEN = config['DEVMAN_TOKEN']
KeyError: 'DEVMAN_TOKEN' 
```

That means that you still forgot to create your own .env file for DEVMAN_TOKEN and TELEGRAM_TOKEN.

P. P. S.
If you see tracback that says that chat_id tupple index out of range - write something to your bot in Telegram and try again.