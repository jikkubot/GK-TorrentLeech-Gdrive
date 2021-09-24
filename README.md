# for support join here [TorrentLeech-Gdrive](https://telegram.dog/GBotStore) [![Hits](https://hits.seeyoufarm.com/api/count/incr/badge.svg?url=https%3A%2F%2Fgithub.com%2Fgautamajay52%2FTorrentLeech-Gdrive&count_bg=%2379C83D&title_bg=%23555555&icon=&icon_color=%23E7E7E7&title=hits&edge_flat=false)](https://github.com/gautamajay52/TorrentLeech-Gdrive)
# working example group [Leech Here](https://telegram.dog/GBotStore)

# Telegram Torrent Leecher 🔥🤖

A Telegram Torrent (and youtube-dl) Leecher based on [Pyrogram](https://github.com/pyrogram/pyrogram)

# Benefits :-
    ✓ Google Drive link cloning using gclone.(wip)
    ✓ Telegram File mirrorring to cloud along with its unzipping, unrar and untar
    ✓ Drive/Teamdrive support/All other cloud services rclone.org supports
    ✓ Unzip
    ✓ Unrar
    ✓ Untar
    ✓ Custom file name
    ✓ Custom commands
    ✓ Get total size of your working cloud directory
    ✓ You can also upload files downloaded from /ytdl command to gdrive using `/ytdl gdrive` command.
    ✓ You can also deploy this on your VPS
    ✓ Option to select either video will be uploaded as document or streamable
    ✓ Added /renewme command to clear the downloads which are not deleted automatically.
    ✓ Added support for youtube playlist 😐
    ✓ Renaming of Telegram files support added. 😐
    ✓ Changing rclone destination config on fly (By using `/rlcone` in private mode)
    ✓
    
# TO-DO
-   ~Gdrive file clonning using Gclone~ `DONE ✓`
-   [ ] Adding mp3 files support while playlist downloading.
-   [ ] Password support while Unarchiving the files.
-   [ ] Selection of required files during leeching the big files using aria(/leech command)

## installing...

### The Easy Way

#### STEPS (I did this to avoid the use of same button multiple times)

a)You have to fork this repo at first(Don't know how to🤔, Then google it😐)

b)Find `app.jso`. 🧐

c)Tap on that. 😬

d)Tap to edit and just add `n` at last of name (Don't touch code🤦). ✍️

e)It should look like `app.json`. 🎉

f)Then tap 👇👇

 Heroku is not supported now 😕 #Dead

Better buy a vps 😐 and follow [this](https://github.com/gautamajay52/TorrentLeech-Gdrive#process-to-run-this-bot-on-vps)

## Process to run this BOT on VPS

- Clone this repo:
```
git clone https://github.com/gautamajay52/TorrentLeech-Gdrive torrentleech-gdrive
cd torrentleech-gdrive
```

- Install requirements
For Debian based distros
```
sudo snap install docker
```
Install Docker by following the [official docker docs](https://docs.docker.com/engine/install/debian/)

## Setting up config file
```
cp sample_config.env config.env
```
After this step you will see a new file named ```config.env``` in root directory.

Fill those compulsory variables.

If you need more explanation about any variable then read [app.jso](https://github.com/gautamajay52/TorrentLeech-Gdrive/blob/master/app.jso)

##### Set Rclone

1. Set Rclone locally by following the official repo : https://rclone.org/docs/
2. Get your `rclone.conf` file.
will look like this
```
[NAME]
type = 
scope =
token =
client_id = 
client_secret = 

```
2 Copy `rclone.conf` file in the root directory (Where `Dockerfile` exists).

3 Your config can contains multiple drive entries.(Default: First one and change using `/rclone` command)

## Deploying

- Start docker daemon (skip if already running):
```
sudo dockerd
```
- Build Docker image:
```
sudo docker build . -t torrentleech-gdrive
```
- Run the image:
```
sudo docker run torrentleech-gdrive
```
Follow this [Video Tutorial](https://youtu.be/J3tMbngA9DE)
### The Legacy Way
Simply clone the repository and run the main file:

```sh
git clone https://github.com/gautamajay52/TorrentLeech-Gdrive
cd TorrentLeech-Gdrive
python3 -m venv venv
. ./venv/bin/activate
pip install -r requirements.txt
# <Create config.env appropriately>
python3 -m tobrot
```
### Variable Explanations

##### Mandatory Variables

* `TG_BOT_TOKEN`: Create a bot using [@BotFather](https://telegram.dog/BotFather), and get the Telegram API token.

* `APP_ID`
* `API_HASH`: Get these two values from [my.telegram.org/apps](https://my.telegram.org/apps).
  * N.B.: if Telegram is blocked by your ISP, try our [Telegram bot](https://telegram.dog/UseTGXBot) to get the IDs.

* `AUTH_CHANNEL`: Create a Super Group in Telegram, add `@GoogleIMGBot` to the group, and send /id in the chat, to get this value.

* `OWNER_ID`: ID of the bot owner, He/she can be abled to access bot in bot only mode too(private mode).

## FAQ

##### Optional Configuration Variables

* `DOWNLOAD_LOCATION`

* `MAX_FILE_SIZE`

* `TG_MAX_FILE_SIZE`

* `FREE_USER_MAX_FILE_SIZE`

* `MAX_TG_SPLIT_FILE_SIZE`

* `CHUNK_SIZE`

* `MAX_MESSAGE_LENGTH`

* `PROCESS_MAX_TIMEOUT`

* `ARIA_TWO_STARTED_PORT`

* `EDIT_SLEEP_TIME_OUT`

* `MAX_TIME_TO_WAIT_FOR_TORRENTS_TO_START`

* `FINISHED_PROGRESS_STR`

* `UN_FINISHED_PROGRESS_STR`

* `TG_OFFENSIVE_API`

* `CUSTOM_FILE_NAME`

* `LEECH_COMMAND`

* `YTDL_COMMAND`

* `GYTDL_COMMAND`

* `GLEECH_COMMAND`

* `TELEGRAM_LEECH_COMMAND`

* `TELEGRAM_LEECH_UNZIP_COMMAND`

* `PYTDL_COMMAND`

* `CLONE_COMMAND_G`

* `UPLOAD_COMMAND`

* `RENEWME_COMMAND`

* `SAVE_THUMBNAIL`

* `CLEAR_THUMBNAIL`

* `GET_SIZE_G`

* `RENAME_COMMAND`

* `UPLOAD_AS_DOC`: Takes two option True or False. If True file will be uploaded as document. This is for people who wants video files as document instead of streamable.

* `INDEX_LINK`: (Without `/` at last of the link, otherwise u will get error) During creating index, plz fill `Default Root ID` with the id of your `DESTINATION_FOLDER` after creating. Otherwise index will not work properly.

* `DESTINATION_FOLDER`: Name of your folder in ur respective drive where you want to upload the files using the bot.

## Available Commands

* `/rclone`: This will change your drive config on fly.(First one will be default)

* `/gclone`: This command is used to clone gdrive files or folder using gclone.
       
       Syntax:- `[ID of the file or folder][one space][name of your folder only(If the id is of file, don't put anything)]` and then reply /gclone to it.
       
* `/log`: This will send you a txt file of the logs.

* `/ytdl`: This command should be used as reply to a [supported link](https://ytdl-org.github.io/youtube-dl/supportedsites.html)

* `/pytdl`: This command will download videos from youtube playlist link and will upload to telegram.

* `/gytdl`: This will download and upload to your cloud.

* `/gpytdl`: This download youtube playlist and upload to your cloud.

* `/leech`: This command should be used as reply to a magnetic link, a torrent link, or a direct link. [this command will SPAM the chat and send the downloads a seperate files, if there is more than one file, in the specified torrent]

* `/leechzip`: This command should be used as reply to a magnetic link, a torrent link, or a direct link. [This command will create a .tar.gz file of the output directory, and send the files in the chat, splited into PARTS of 1024MiB each, due to Telegram limitations]

* `/gleech`: This command should be used as reply to a magnetic link, a torrent link, or a direct link. And this will download the files from the given link or torrent and will upload to the cloud using rclone.

* `/gleechzip` This command will compress the folder/file and will upload to your cloud.

* `/leechunzip`: This will unarchive file and dupload to telegram.

* `/gleechunzip`: This will unarchive file and upload to cloud.

* `/tleech`: This will mirror the telegram files to ur respective cloud cloud.

* `/tleechunzip`: This will unarchive telegram file and upload to cloud.

* `/getsize`: This will give you total size of your destination folder in cloud.

* `/renewme`: This will clear the remains of downloads which are not getting deleted after upload of the file or after /cancel command.

* `/rename`: To rename the telegram files.


* ~Only work with direct link and youtube link for now~It is like u can add custom name as prefix of the original file name.
Like if your file name is `gk.txt` uploaded will be what u add in `CUSTOM_FILE_NAME` + `gk.txt`

~Only works with direct link/youtube link.No magnet or torrent.~

And also added custom name like...

You have to pass link as 
`www.download.me/gk.txt | new.txt`

the file will be uploaded as `new.txt`.


## How to Use?

* send any one of the available command, as a reply to a valid link/magnet/torrent. 👊


## Credits, and Thanks to
* [GautamKumar(me)](https://github.com/gautamajay52/TorrentLeech-Gdrive) 😬
* [SpEcHiDe](https://github.com/SpEcHiDe/PublicLeech) for his wonderful code😚
* [Rclone Team](https://rclone.org) for theirs awesome tool☁️
* [Dan Tès](https://telegram.dog/haskell) for his [Pyrogram Library](https://github.com/pyrogram/pyrogram)
* [Robots](https://telegram.dog/Robots) for their [@UploadBot](https://telegram.dog/UploadBot)
* [@AjeeshNair](https://telegram.dog/AjeeshNait) for his [torrent.ajee.sh](https://torrent.ajee.sh)
* [@gotstc](https://telegram.dog/gotstc), @aryanvikash, [@HasibulKabir](https://telegram.dog/HasibulKabir) for their TORRENT groups
* [![CopyLeft](https://telegra.ph/file/b514ed14d994557a724cb.jpg)](https://telegra.ph/file/fab1017e21c42a5c1e613.mp4 "CopyLeft Credit Video")
