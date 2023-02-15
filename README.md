# InstagramAutomation
The goal of this repository is to create a script that fully automates all aspects of an Instagram Page. These include:
 - Finding the Content - VideoScraper
 - Produce Clips from the Videos - ClipFinder
 - Creation of Content - CreateReel
 - Marketing the Page - FollowBot
 
Combining to fully automate the page -> VideoScraper + ClipFinder (Not Uploaded) + Create Reel. The Videoscraper script creates a list of videos that have been uploaded. ClipFinder uses a trained AI model to find clips form these videos, which is then passed through the createReel script to create clips with subtitle overlays. These clips can be uploaded with further automation using a simple seleunium script or 3rd party application, however I choose to manually look through the clips.

Create Reels
------------------
The 'createReel Script' will take a clip from youtube and:
  1. convert that video into the correct dimensions for an instagram reel
  2. transcribe the audio of the clip and overlay it on top of the video
  3. use chatGPT to caption the video with hashtags for instagram using the transcript

Follow Bot
------------------
The Follow-Bot uses selenium automation to follow a list of random users.
The way it works is as follows:
  1. Finds your latest reel
  2. Clicks on a random hashtag on your reel
  3. Finds posts that have the same hashtag
  4. Looks at the likes of the reel to find users with similar interests
  5. Uses ActionChains from selenium to click on the follow button
  
 Note: in order for this to work you must have at least 1 reel uploaded with a hashtag in the caption of that reel.
 
 
 Video Scraper
------------------
This script uses YouTube API to scrape for the latest videos for channels
The output returns a list, from the dictionary of channels, containing the title and upload date of the video
The script allows for both scraping a single channel, or scraping multiple channels
