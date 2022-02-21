# Talkative Bot

You can talk with very talkative bot. 
You can ask a question or say something and bot will answer you in talkative manner. 

There are three user's ranks: admin, moderator, and user.
There is using combination of Retrieval and Generative Q/A model.

MongoDB is used to store states in [FSM](https://en.wikipedia.org/wiki/Finite-state_machine/)

## Examples

![example](.github/images/1.png)

## FSM image

![FSM](.github/images/2.png)

## Run

0. Install [mongoDB](https://www.mongodb.com/)
1. Clone this repo
> `git clone https://github.com/Dalvikk/ExamBot`
2. Install dependencies
> `cd ExamBot/`  
> `pip3 install --no-cache-dir -r requirements.txt`
3. Set environment variables
> `set PYTHONPATH="." (on Windows)`  

Let Python know that the package is here, otherwise it raise a exception «module exam_bot not found»  
Now set up other environment variables or write them directly in config.py

```
set TOKEN="<Bot's token here>"
set OWNER_ID="<Admin id>"
set FILES_PATH="<Path to directory with questions>" # Ex: "./files"
set DB_NAME="aiogram"
set PORT ="27017"
set HOST="localhost"
set SEND_ERRORS="True" // "True" if you want that exceptions message will sent to you
```
4. Make sure Mongodb is running
5. Run  
>  `python ./exam_bot/bot.py`
> 
> 
## TODO list
* Add multi-language support
* New feature: users will be able to rate themselves, and the bot will collect statistics. The functions "give the question with the worst rating" will be added
* Reminder: ask a random question every `n` minutes
* Fix bugs related to race condition
* Optimize files sending by sending file_id which will be stored for each file
