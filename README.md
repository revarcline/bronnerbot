# bronnerbot
personal fork of [markovbot](https://github.com/esdalmaijer/markovbot) 
with some minor tweaks to operate [alloneallbot](https://twitter.com/alloneallbot)


## Instructions

from the project root, with pipenv installed:
```python
python3 -m venv venv
source venv/bin/activate
pipenv install
python3 bot.py
```

auth secrets are stored in the secrets.py file, consult the [tweepy documentation](https://docs.tweepy.org/en/stable/index.html)

I've also included a sample service file for running the bot as a systemd service. I recommend creating a dedicated `markovbot` user as referenced in the service file, but you can change that line to use whichever user you'd like.

While editing the file, make sure to use absolute paths where indicated, then:
```
sudo cp bronnerbot.service /etc/systemd/system/
sudo systemctl daemon-reload
sudo systemctl start bronnerbot.service
sudo systemctl enable bronnerbot.service
```
