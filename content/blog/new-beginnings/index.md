---
title: Spotify-Downloader
date: "2020-11-11"
description: A simple Breakdown of how I made my Spotify-Downloader using simple Python Scripting.
---

##About the Project

Spotify Downloader is a script that I made using Python that takes Spotify URLs as input and provide the mp3 of a particular song

On a side note:
It is only for personal use and not to be used commercially
I'm not responsible for any non-ethical use of this application.

####<a href="https://github.com/hidimpu/Spotify-Downloader"> Look the code at original GitHub Repo <u> Here! </u> </a>

> Preparation

We all know that Spotify Officially streams the song to client with their own proprietary encryption methods which is nearly impossible as well illegal to decode or download.

##So how do we extract the mp3?

Well there is a sneaky way to ethically fetch the mp3 of pretty much any distributed song.
Were going to take help of YouTube.Chances are way less if its not published on youtube or have different keywords as the name

###Step 1 : Fetching the Names of the Song!

Here the Parsed the spotify URL to fetch the Title of song and the name of the artists involved in order to get the most accurate results out of YouTube such that the result index of the searches gives the desired song at the first position.

###Step 2: Looking through YouTube!

Here, I replaced the spaces in the song Title and the Artist names with the "+" sign in order to concatinate with the base youtube search URL that gives the indexing of the results on the web page.

Youtube Base URL: 'https://www.youtube.com/results?search_query='
Song Name to input : 'ncs alan walker faded'

The resultant string URL to be fetched by our program: 'https://www.youtube.com/results?search_query=ncs+alan+walker+faded'

###Step 3: Getting the Song

Since the keywords we are searching on youtube are the most accurate of the desired song, there is a great probability that the song is going to show up on the first result of the youtube.

Furthermore, we take the video ID from the first result and again added into a base YouTube URL, similarly we did above.
Final video URL: 'https://www.youtube.com/watch?v=bM7SZ5SBzyY'

###Step 4: Extracting the mp3

Since we have the webpage of the data we have fetched of the song, we can take help of FFMPEG or youtube-dl to download and convert that song into highest mp3 size possible.
In this case, I have used FFMPEG that converts the web video format into mp3 and the download starts into the computer.

## Conclusion

This was a simple breakdown and the thought process that went behind making this script and project.
I did explained the core logic here and the whole code is open source as well as available on Github. Feel free to contribute and test this cool script :)
