<p>
  <img src="https://scrutinizer-ci.com/g/MatviiB/telegram-logger/badges/build.png?b=master" alt="build passed">
  <img src="https://scrutinizer-ci.com/g/MatviiB/telegram-logger/badges/code-intelligence.svg?b=master" alt="code-intelligence">
  <!-- <img src="https://scrutinizer-ci.com/g/MatviiB/telegram-logger/badges/quality-score.png?b=master" alt="quality-score"> -->
  <img src="https://poser.pugx.org/matviib/telegram-logger/downloads" alt="downloads">
  <img src="https://poser.pugx.org/matviib/telegram-logger/license" alt="license">
</p>

## Logging your application problems(achievements) to Telegram
### Ultralight package

## Usage
```
  \Log::telegram('Hey, i am your application, and i have a problem');
```
![laravel telegram logger](https://gitlab.com/MatviiB/assets/raw/master/download%20(2).png)

# Instalation
```
composer require matviib/telegram-logger
```
Add to your .env file:
```
TELEGRAM_LOGGER_TOKEN=<YOUR_BOT_TOKEN>
TELEGRAM_LOGGER_CHAT_ID=XXX,YYY
#developer1 - XXX
#developer2 - YYY
```
Add to your config/services.php file:
```
'telegram_logger' => [
     'token' => env('TELEGRAM_LOGGER_TOKEN'),
     'chat_id' => env('TELEGRAM_LOGGER_CHAT_ID'),
],
```

# Bonus
### Creating telegram bot tutorial
1. Find BotFather. 
2. Send `/newbot`. 
3. Set up name and bot-name for your bot. 
4. Get token and add it to your .env file.
5. Find your bot (BotFather already generate link to it in last message). 
6. Send one or few messages to him.
7. Open next url `https://api.telegram.org/bot<YOUR_BOT_TOKEN>/getUpdates` and find `chat_id`.

Steps #6,#7 needed for adding EACH developer to listeners of the bot.

![laravel telegram logger](https://gitlab.com/MatviiB/assets/raw/master/download%20(1).png)
