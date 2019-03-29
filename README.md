# TinyScraper
Scrape a web directory for files. Export the selected URLs to a text file.

##Project background 
Clicking through a web directory to find files can be tedious. There's some good applications out there that simplify the process, but I haven't found a good free one. So, I thought I'd build one. The app is totally free and just a hobby project.

Please feel free to download an try it out and message me with any bugs, feature requests or feedback.

##Installation 
This app only runs on Windows (sorry guys). I don't normally build Windows apps, so I went with the easiest deployment method, which is a Windows Click-Once Installer.

To install: 1. Download the Zip file from the link above. 2. Run the setup file. 3. Follow the prompts to install the application. The first time you run Setup it will install the application. Run Setup in future to launch it. I don't know why you have to run Setup each time, but I'll work on building a better installer in future.

##User Guide

###Scraping a Site

    Enter the HTTP/HTTPS address of the site in the URL box. Scraping will start from this location down.

    In the Depth field, select how many levels of sub-folder to scrape. 0 is default; it will only scrape the folder you entered in URL. Entering a depth of 1, will also scrape the next level of sub-folders. 2 or more, will continue to scrape the next levels of sub-folders.

    While the scrape is running, you can check the progress in the Status, right at the bottom of the window.

    Once the scrape has completed, results will appear in a table, in the large white box.

    Look through the results and click the Select Checkbox next to each file you'd like to download.

    Click the Export Selected URLs button. This will prompt you to enter a file name, and the URLs for each selected result will be written to this file. You can then use wget, with the -i flag to download all the files you selected.

###Saving/Loading a Scrape

Scraping can take some time, so you may wish to save the results of a scrape, to download the files later. To do this: 1. Follow steps 1 - 4 above, to complete a scrape.

    Click the Save Scrape File button and enter a file name. (A scrape file is just a serialized JSON string of the results).

You can then use the Load Scrape File button to reload these results at a future date. You could even send the scrape file to a friend and they could load the same scrape file into the app.

###Working with Results

After you've performed a scrape and have some results, you can use the following features to filter/refine the results. This is especially useful when you have thousands of results.

    In the File Types area, you can click the radio buttons to filter results to either Video or Audio formats.

    In the Refine Results area, you can click the Remove Duplicates button to remove any duplicate file names. This only works on exact matches.

    In the Refine Results area, you can also enter some text and click Find. This will filter the results to those with that exact text in the Name. (To reset this, click one of the File Types radio boxes; sorry, I haven't implemented a Clear Find button yet).

###My Testing

I've tested the app on 4 - 5 web directories and implemented workarounds for how some of the web servers display them. If you find any defects, please let me know and provide me with an example URL and the Depth value, so I can simulate it.

The app is pretty quick. My biggest scrape was 3 levels deep and only took a couple of minutes to return 4,600 files (on a 100MB internet connection).

Original thread posted here - 

* https://www.reddit.com/r/opendirectories/comments/b60ebp/ive_created_an_app_to_scrape_web_sites_for_files/

* https://web.archive.org/save/https://www.reddit.com/r/opendirectories/comments/b60ebp/ive_created_an_app_to_scrape_web_sites_for_files/

* http://archive.fo/nZMDA
