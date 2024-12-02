# Reddit Image Scraper

## Description 

Reliably scrape multiple subreddits and users for multiple file formats. 

## Original

https://github.com/D3vd/Reddit_Image_Scraper


## New Features

This version well-supersedes the template created previously, with MANY new features. 

* Auto-blacklisting low-quality images
* Auto-blacklisting dead links
* User-defined query timeout (how long will you wait between each query?)
* User-defined API error timeout (this seems to help overall speed)
* User-defined query quantity (How many queries per category per sub?)
* User-defined minimum file size (to blacklist and delete after downloading)
* De-duplication of downloaded files (It will never download the same file twice)
* Puts files in respective folders
* Logging of progress, all files downloaded
* Logs the time it takes per sub, per category

And best of all, it's VERY EASY to setup. 

## Prerequisites / Packages Used

Make sure to have installed these libraries before executing the program.

* [PRAW](https://pypi.org/project/praw/)
* [ConfigParser](https://pypi.org/project/configparser/)
* [Urllib](https://docs.python.org/3.0/library/urllib.request.html)
* Blake3

These can be installed with the command
```python -m pip install -r requirements.txt```

## First time running

### Run it once

1. Run the program once. It will create the source files you need to get started. 

### Get an API key by "Creating an app"
2. Go to this [link](https://www.reddit.com/prefs/apps/)
3. Press the **Create an app** button on the bottom.
4. Give a name, and description for your app. 
5. Choose 'Script' in the app type section.

### Back in the program
6. Put the client ID and Secret in config.ini 
7. Add some subreddits to your subs.txt
8. run python3 reddit_image_scraper.py.
10. Check the ./result directory for your images!
11. Check the ./logs folder for history / troubleshooting on your recent runs. 

## Warnings
Write some warnings here soon for best practices. 
* Don't run more than one at a time. Your API key will get rate-limited and both may go even slower. 
* DO NOT SHARE your API keys, or upload them anywhere public! Don't upload them to github, either! Treat them like a username/password.

## Automating the script

**Crontab** entry for you if you like: 

Runs once a day at 00:00 UTC.  

```00 00 * * * cd /path/to/script/Reddit_Image_Scraper-master && python3 Reddit_image_scraper.py```


# Gif Demo

![](./howtoscrape.gif)









