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

auth secrets are stored in the secrets.py file, consult the tweepy documentation

also included a sample service file for running the bot as a systemd service - 
make sure to use absolute paths where indicated, then:
```
sudo cp bronnerbot.service /etc/systemd/system/
sudo systemctl daemon-reload
sudo systemctl start bronnerbot.service
sudo systemctl enable bronnerbot.service
```
