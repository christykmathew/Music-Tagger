
<img src="https://img.shields.io/badge/Build-Unstable-blue"> <img src="https://img.shields.io/badge/Version-v1.2-green"> 
# Music-Tagger

<!-- [![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/christykmathew/Music-Tagger/] -->

An Mp3 file tag for obsessive-compulsive music geeks. Tags like Artist, Album, Genre, Lyrics etc. can be added to your audio metadata and can be automated to certain level. Shazam API is used to fetch the list and meta data of the mp3 file. Synced lyrics that are available is fetched from megalobiz. Mutagen library is used at tha core to edit the meta data.

## TODO ##
  - [] Add SYLT ID3v2.4 frame (Synced Lyrics Tag) to Mp3 files.
  - [] Stable version for Windows

## Dependencies ##
API key is required to access Shazam database. Get API Key by signing up in this <a href='https://rapidapi.com/apidojo/api/shazam?endpoint=apiendpoint_e5620280-234d-409b-a0cf-eb618f1f687d'>link</a> and paste it in the API_KEY variable
``` python
API_KEY = "" #Enter you API Key
```

## Usage ##
Self-explanatory prompts and outputs are generated while running the python cels. _music_list_, _music_search_, _Meta_Retrieve_, _synced_lyric_ are the main functions that are used in this program
