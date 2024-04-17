# Automa-tumblr-poll-creator
An importable file that can be used in Automa to automatically generate tumblr polls. If you’ve ever wanted to run a tumblr tournament but don’t love the idea of manually creating 100+ posts, this Automa workflow is for you! 

## General process overview
This workflow uses the following steps using Automa's built-in tools:
1. Opens up a new tumblr tab and create a text post
2. Changes to the correct blog
3. Imports images based off info in a Google Sheet
4. Fills out a poll based off info in that same Google Sheet
5. Changes the duration of the poll to seven days
6. Adds tags based off info in the Google Sheet
7. Queues the post
8. Closes the tab
9. Repeats for all rows in the Google Sheet

## Usage
### Things You’ll Need: 
* An account on tumblr and a blog to publish to
* The browser extension “Automa” (available in both Chrome and Firefox)
* The .json Automa import file included in this repo
* A Google Sheet spreadsheet with some specific column headers ([template here](https://docs.google.com/spreadsheets/d/1eF-1u3MfXCt0riDgh28uxfJu2iNxu607RwY-6fyWi4M/edit?usp=sharing))
### Steps: 
1. If you haven’t already, download the Automa extension. ([Firefox link](https://addons.mozilla.org/en-US/firefox/addon/automa/)) ([Chrome link](https://chromewebstore.google.com/detail/automa/infppggnoaenmfagbfknfkancpbljcca?pli=1))
2. Fill out the Google Sheet with your contestant names, image urls, and fandom names according to the template. (Note: for the image URLs, don’t use any random URL you find on the internet, instead download and then upload the image to Google Drive or other hosting site of your choice and link it from there. This is to both protect your image from breaking if the URL goes dead at any point, and also just to avoid straining a random site’s servers.)
3. Make your Google Sheet publicly accessible, or otherwise share it with the Automa service email ([instructions here](https://docs.automa.site/blocks/google-sheets.html)). 
2. If you haven’t already, download the attached Automa .json file from this repo. Open it in your no-frills text editor of choice (like Notepad). Using Find and Replace (Ctrl + H for most apps) replace the text “TOURNAMENT-BLOG-NAME-HERE” with the name of the blog you want these polls posted to, and “YOUR-SPREADSHEET-ID-HERE” with your Google Sheet’s spreadsheet ID (this is the long id found in the URL of your spreadsheet). 
3. Open up the Automa dashboard (you can access this by finding the extension in your browser + opening up the small pop-up dialogue, which then has a button in the top right corner).
4. Import the workflow. (Note: If you want to test this with a single poll first, open up the workflow in Automa's editor and unlink the “Loop Breakpoint” block by double clicking on the line that connects it to the previous block).
6. Open up the workflow, hit “Save”, and then click the play button. (Make sure you're logged into tumblr in your browser so Automa can successfully open up the "create post" dialogue.)
7. Wait until your poll(s) are finished generating. This will take a few seconds per poll, so you may want to walk away and leave your computer alone for a while.
8. Go to your queue and verify that the polls were generated as expected.
9. Profit!
### Limitations and other notes
* As is, this workflow currently only supports polls with 2 choices. But if you're willing to mess around in Automa, it likely shouldn’t be too hard to modify the workflow to handle more than 2 contestants. You would just need to add a new column to your spreadsheet and then duplicate a few steps in the workflow.
* Likewise, it does not support more than 2 images.
* This workflow is currently set up such that it will set the polls to run for 7 days and then add them to your tournament blog's queue. If this isn't what you're looking for, this can be modified by deleting or editing the appropriate blocks in the Automa editor.
