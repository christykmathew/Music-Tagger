<img src="https://img.shields.io/badge/Version-v1.2-green"> <img src="https://img.shields.io/badge/build-unstable-orange"> 

# Music-Tagger

## Table of Contents

* [Introduction](#Introduction)
* [Features](#Features)
* [TODO](#TODO)
* [Dependencies](#Dependencies)
* [Usage](#Usage)

## Introduction
An Mp3 file tagger for obsessive-compulsive music geeks. Tags like Artwork, Artist, Album, Genre, Lyrics etc. can be added to your audio metadata and can be automated to certain level. Shazam API is used to fetch the list and meta data of the mp3 file. Synced lyrics that are available is fetched from megalobiz. Mutagen library is used at tha core to edit the meta data.

## Features
- List down probable music titles from the Mp3 filename
- Get accurate metadata about the music like Artist, Album, Genre, Lyrics, Label, Year, Artwork and save these in the Mp3 file.
- Get synced Lyrics of the music.
- User-Friendly interface.

## TODO
  - [x] Get Synced Lyrics of the music
  - [ ] Add SYLT ID3v2.4 frame (Synced Lyrics Tag) to Mp3 files.
  - [ ] Stable version for Windows

## Dependencies
API key is required to access Shazam database. Get API Key by signing up in this <a href='https://rapidapi.com/apidojo/api/shazam?endpoint=apiendpoint_e5620280-234d-409b-a0cf-eb618f1f687d'>link</a> and paste it in the API_KEY variable
``` python
API_KEY = "" #Enter you API Key
```
Dependencies like _mutagen_, _wget_, _music-tag_ etc. are already installed while running the cells. 

## Usage
Self-explanatory prompts and outputs are generated while running the python cells. _music_list_, _music_search_, _Meta_Retrieve_,_Tags_Save_, _synced_lyric_ are the main functions that are used in this program. These functions can be used individually as well.  


  1. *music_list*  takes two arguments term and API_KEY where term is the term to be searched. The response from the database in json format is returned
```python
def music_search(term, API_KEY):
  '
  '
  return response
```  

2.  _music_search_ takes three arguments _file_, _mode_ and _api_ where _file_ is the mp3 file or the term to be searched and _mode_ that can be either 0(Auto selects probable options) or 1(mannual selection (preferred)) and api is the API_KEY. A list of probable music titles based on the file/term will be displayed and its music key will be returned which will be used by _Meta_Retrieve_.
```python
def music_list(file, mode, api):
  '
  '
  return music['tracks']['hits'][int(option)]['track']['key']
```  

  3.  _Meta_Retrieve_ takes three arguments _key_, _file_, _API_KEY_ where key is the key retrieved from  _music_search_, _file_ is the name of the Mp3 file. The available tags will be displayed in output. Some tags might not be available and prompt to enter those tags manually will be given. All the tags in a dictionary and the image file will be returned by this function.
```python
def Meta_Retrieve(key, file, API_KEY):
 '
 '
 return tag, Image
```  


4.  _Tags_Save_ takes three argument _Tags_, _Image_, _file_path_ where _Tags_ are the python dictionary cantaining the tags, _Image_ is the artwork/Image file for Mp3 and _file_path_ is the path location of the image file. This function is used to save the meta tags to the Mp3 file and doesn't return anything.
 ```python
def Tags_Save(Tags, Image, file_path):
```  


  5.  _synced_lyric_ takes two argument _file_path_ which is the path location of Mp3 and _term_ is the filename/term to be searched for synced lyrics. Synced Lyrics will be saved as _.lrc_ file in Lyrics folder in the _file_path_ specified.
```python
def synced_lyric(file_path, term):
```  
