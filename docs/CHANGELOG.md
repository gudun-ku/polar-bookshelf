
# 1.0.0-beta110

- 

- Went through and ugpraded all apps to make sure electron-log was enable and 
  working properly.

- now using electron-log as our logger by default.  We now log to .polar/logs 
  and consolidate all the window log lines into one location.  This way users
  can debug their problems easier.

- big refactor of the main app into smaller components. Code is much more 
  manageable now.
  
- update electron-log version      

# 1.0.0-beta103

- deleted some of the pdf.js nav links as they were broken for the most part.

- Removed errant link to jquery-ui which was being fetched and probably slowing
  down the initial page load.

# 1.0.0-beta102

- Fixed Windows builds to have proper files for the .exe. Setup tested and it 
  works properly now. 

# 1.0.0-beta100

- Capture now using webview by default for captured content. Should be much much
  more reliable and usable. Prevents crashes on Linux.
  
- Windows builds now dramatically smaller.  From 300MB down to 75MB.  

- Migrated to ASAR builds which should significantly improve performance on Windows
 
- 64bit and 32bit Windows builds now available.

- Capturing now more reliable if it is aborted by the user.  Electron used to
  lock up.   

- Initial Anki sync working

- Flashcard input now fully working.  

- Ability to set titles for a document

- Initial support for pagemarks that can be 'ignored' and have a state so that
  you can say that you're ignoring a whole section of a doc and not that it's 
  been 'read'.

- Image sync works for Anki and we properly handle media files.

- Better integration with your primary browser. If you click on a link in a 
  captured page it opens in your browser.

- Started work on a video implementation to create notes+flashcards while watching
  a youtube video and keeping track of progress while watching it.  Will take a 
  while to have an implementation of this feature ready. 

# 1.0.0-beta10

- ability to easily toggle the devtools.

- --enable-dev-tools command line arg for starting with the dev tools already running

# 1.0.0-beta9

- reworked command line handling so that PDFs that are opened from the command
  line are opened in a new window.

- new "Open in New Window" menu option so that we can work with multiple PDF
  files.

# 1.0.0-beta8

- New windows were always maximized which was difficult to work with.

- Support opening multiple windows now.  We were constrained to just one window
  before.

# 1.0.0-beta7

- All PDF files are served via HTTP and webapp served via HTTP too which avoids
  some pdf.js bugs.