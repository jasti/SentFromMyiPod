---
title: Programmatically Downloading Legal Music 
description: Programmatically Downloading Legal Music  
date: 2014-08-31
layout: layouts/post.njk
---

For me, there are very few solo activities that don’t involve music playing in the background. Programming, writing, reading, working out and more recently, cooking. Although most of my music listening has moved online to a combination of Spotify, 8tracks and Pandora, there are a couple of reasons I still like to own my music offline. 
</br>
First, if I am at a park or a place without Wi-Fi, I don’t want to be stranded without the music of my choice. Add to that the stupid data limits placed by phone networks which restrict your ability to stream music. Second, a lot of unique music is made by artists that don’t <a href="http://goo.gl/QFaaZ1">sell</a> their music, and therefore not available through Spotify type services.

A friend recently recommended <a href = "http://musicforprogramming.net">MusicforProgramming.net</a>, and it is fantastic. The problem was that the music I wanted was sprawled across 27 pages on the site. I didn’t want to click on each link and download it manually. Moments like these are when I am truly thankful that I can code my way out such scenarios.

I wrote this little Python script that takes a website and downloads any mp3 files found on the site. Additionally, it will go to any links it finds on the given site, navigate to the pages and download all those mp3 files that it finds on each page as well. Since the files being downloaded are quite large, the script also prints the status of each download. 

I’ve abstracted out the methods in such a way that the script can be reused for any website that hosts music, with minor changes. The primary functions in the script are:

1. Given a page, find all the links in the page iteratively and collect all the mp3 file links 
2. Given a mp3 file link, download it

<h2>Functions</h2>
The function <i>findUrls</i> uses <a href = "http://www.crummy.com/software/BeautifulSoup/">BeautifulSoup</a> to find all links on a page. This function is reused to grab all the URLs on a page and a second time to grab all the URLs on a page that end with the file extension ‘.mp3.’ You can obviously extend this to support any audio formats you like.

<center><img src="/images/blog/beats/findUrl.png"/></center> 

The function <i>downloadMusic</i> takes an mp3 file as an argument and downloads the file to the folder from where the script is invoked. The file size is obtained from the header and the file is downloaded in chunks. The progress is output to the console in a while loop as the download progresses.

<center><img src="/images/blog/beats/dlMusic.png"/></center> 

Last but not least is the main part of the script that ties it all together. The variable main_url is the URL where you want to download the music from and it function makes use of the other two functions above to fetch all the music.

<center><img src="/images/blog/beats/main.png"/></center> 

<h2>Running It</h2>
You can find the full script in this <a href ="https://gist.github.com/jasti/cf5188b411d185a4f27a">gist</a>. Run this from the command line by simply typing 'python Beats.py'. You will see the files getting downloaded to the same location you ran it from on the disk.

<center><img src="/images/blog/beats/running.png"/></center> 


 Feel free to copy, download, share or distribute. You should be able to reuse this by simply editing some variables. For e.g., I programmatically download some of my favourite audio podcasts from KEXP’s <a href ="http://feeds.kexp.org/kexp/musicthatmatters">‘Music That Matters’</a>  that I often use for my long runs.
</br>
 HUGE time-saver. More time for watching those cat videos, you know.

---
