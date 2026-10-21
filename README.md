# Me

When I listen to music on Youtube, if I am interested in the song, I will use some web page like y2... to download it to local under mp3 type. Then play it on Apple Music or Spotify. This will make sync songs all devices. And I can play them when I drive car. But web page always have advertise and pop up something which I don't like. 
Another thing, web page allows converting one by one. It takes time.

I ask claude to create script to do that and it can download, convert playlist :D

# Get started

## Install `yt-dlp` and `ffmpeg`

> NOTE: check and up to date `yt-dlp`

```sh
brew install yt-dlp ffmpeg
```

## Use `ytaudio`

### Change mode to exec script

```sh
chmod +x ytaudio
```

### NOTE:
- Change directory or default at `~/Downloads/music/YouTube` in script by editting it
- Usage
```sh
#   ytaudio <url> [url...]          # download mp3 (default)
#   ytaudio -f best <url>           # keep orginal audio, don't encode
#   ytaudio -f flac <url>           # output FLAC
#   ytaudio -p <playlist_url>       # download playlist
#   ytaudio                         # dont have URL -> get link from clipboard
#
# Option:
#   -f FORMAT   mp3 | m4a | opus | flac | wav | best   (default: mp3)
#   -o DIR      directory store (Default: ~/Music/YouTube)
#   -p          allow download playlist
#   -h          help
```

### Download one url

```sh
./ytaudio -f best "https://youtu.be/xxx..."
```

### Download playlist

```sh
./ytaudio -f m4a -p "https://youtube.com/playlist\?list\=xxx.."
```