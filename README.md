Music Catalog Bot
=================

This Telegram bot maintains a user generated catalog of music.

How does it work? You simply send an audio file (from Telegram Desktop, Web or OSX) to the bot and it's added to the public catalog. All tracks are indexed and available for everyone from any Telegram client.

Go ahead and [try it](https://telegram.me/MusicCatalogBot)!


**UPDATE**: The bot is blocked on iOS due to Apple complaints. Well, that was expected. Good luck Apple with your walled garden, I'm not buying iOS anymore.


![Screenshot](http://i.imgur.com/vRNxnDS.png)
![Screenshot](http://i.imgur.com/qmvht6v.png)

### Technical side

The bot doesn't store any media, instead it only stores track metadata, while files are hosted on Telegram servers.

It's written in Python 3, powered by [aiotg](https://github.com/szastupov/aiotg) framework and uses [MongoDB](https://www.mongodb.com) for index.

You can easily run your own instance with docker:
```
$ cp example-compose.yml docker-compose.yml
$ vi docker-compose.yml # set your API token
$ docker-compose build
$ docker-compose up -d # We are up and running!
```

You can also do it without Docker, the requirements are specified in requirements.txt, you know the rest.
