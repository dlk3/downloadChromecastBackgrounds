# Download Chromecast Home Background Images

## Tampermonkey.js

This is a Javascript script used in the Tampermonkey extension inside the Google
Chrome browser.  It will download each image file as it appears on the
http://google.com/cast/chromecast/home web page.  That web page automatically
cycles through a collection of images over a period of time.  The downloaded
images will be saved in the downloads directory cofigured in the browser,
typically ~/Downloads.  The files will be named with the Javascript timestamp
(seconds since the epoch) for the time when they were downloaded.  Each
downloaded file contains EXIF information which includes a text description and
the name of the artist/photographer.

## deldupes

This Python script will delete duplicate files.  It compares the MD5 hashes of
the files to identify duplicates.

Usage:

  `deldupes /path/to/files` - list duplicate files<br />
  `deldupes -d /path/to/files` - delete duplicate files

## store-new

This Python script moves new, unique files from the downloads directory
to their destination directory.  These directories are set at the top of
the script.  Files in the downloads directory which duplicate files in
the destination directory are deleted.  MD5 hases are used to detect
duplicate files.
