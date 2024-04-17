# Automa-tumblr-poll-creator
An importable file that can be used in Automa to automatically generate tumblr polls.

## Usage

If you’ve ever wanted to run a tournament but don’t love the idea of manually creating 100+ posts, this Automa workflow is for you! 

### Things You’ll Need: 
An account on tumblr and a blog to publish to
The browser extension “Automa” (available in both Chrome and Firefox)
This specific Automa workflow import file
A Google Sheet spreadsheet with some specific column headers ([template here](https://docs.google.com/spreadsheets/d/1eF-1u3MfXCt0riDgh28uxfJu2iNxu607RwY-6fyWi4M/edit?usp=sharing))
### Steps: 
1. If you haven’t already, download the Automa extension. ([Firefox link](https://addons.mozilla.org/en-US/firefox/addon/automa/)) ([Chrome link](https://chromewebstore.google.com/detail/automa/infppggnoaenmfagbfknfkancpbljcca?pli=1))
2. Fill out the Google Sheet with your contestant names, image urls, and fandom names according to the template. (Note: for the image URLs, don’t use any random URL you find on the internet, instead download and then upload the image to Google Drive or other hosting site of your choice and link it from there. This is to both protect your image from breaking if the URL goes dead at any point, and also just to avoid straining a random site’s servers.)
3. Make your Google Sheet publicly accessible, or otherwise share it with the Automa service email ([instructions here](https://docs.automa.site/blocks/google-sheets.html)). 
2. If you haven’t already, download the attached Automa script above. Open it in your no-frills text editor of choice (like Notepad). Using Find and Replace (Ctrl + H for most apps) replace the text “TOURNAMENT-BLOG-NAME-HERE” with the name of the blog you want these polls posted to, and “YOUR-SPREADSHEET-ID-HERE” with your Google Sheet’s spreadsheet ID (this is the long id found in the URL of your spreadsheet). 
3. Open up the Automa dashboard (you can access this by finding the extension in your browser + opening up the small pop-up dialogue, which then has a button in the top right corner).
4. Import the workflow. (Note: If you want to test this with a single poll first, open up the workflow in Automa's editor and unlink the “Loop Breakpoint” block by double clicking on the line that connects it to the previous block).
6. Hit “Save”, and then click the play button. (Make sure you're logged into tumblr in the browser so it can successfully open up the "create post" dialogue.)
7. Wait until your poll(s) are finished generating. This will take a few seconds per poll, so you may want to walk away and leave your computer alone for a while.
8. Go to your queue and verify that the polls were generated as expected.
9. Profit! 
### Other notes:
If you're willing to mess around in Automa, you can customize a lot of this depending on what exactly you want to do. It likely wouldn’t be too hard to modify the workflow to handle more than 2 contestants; you would just need to add a new column to your spreadsheet and then duplicate a few steps in the workflow. 
