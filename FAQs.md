# Overview
## What's this repository all about?
Ebooks and DRM. That is, providing free tools to remove DRM from most ebooks.

## What's DRM?
DRM ("Digital Rights Management") is a way of using encryption to tie the books you've bought to a specific device or to a particular piece of software.

## Why would I want to remove DRM from my ebooks?
When your ebooks have DRM you are unable to convert the ebook from one format to another (e.g. Kindle KF8 to Kobo ePub), so you are restricted in the range of ebook stores you can use. DRM also allows publishers to restrict what you can do with the ebook you've bought, e.g. preventing the use of text-to-speech software. Longer term, you can never be sure that you'll be able to come back and re-read your ebooks if they have DRM, even if you save back-up copies.

## So how can I remove DRM from my ebooks?
Just download and use these tools, that's all! Uh, almost. There are a few, uh, provisos, a, a couple of quid pro quos. 
* The tools don't work on all ebooks. For example, they don't work on any ebooks from Apple's iBooks store.
* You must own the ebook - the tools won't work on library ebooks or rented ebooks or books from a friend.
* You must not use these tools to give your ebooks to a hundred of your closest friends. Or to a million strangers. Authors need to sell books to be able to write more books. Don't be mean to the authors.
* Do NOT use Adobe Digital Editions 3.0 or later to download your ePubs. ADE 3.0 and later can use a new encryption scheme that the tools can't handle. While major ebook stores aren't using the new scheme yet, using ADE 2.0.1 will ensure that your ebooks are downloaded using the old scheme. Once a book has been downloaded with the new scheme, it's IMPOSSIBLE to re-download using the old scheme (without buying it again).

But otherwise, if your ebook is from Amazon, Kobo, Barnes & Noble or any of the ebook stores selling ebooks compatible with Adobe Digital Editions 2.0.1, you should be able to free your books from DRM. 

## Where can I get the latest version of these free DRM removal tools?
Right here at github. Just go to the [releases page](https://github.com/apprenticeharper/DeDRM_tools/releases) and download the latest zip archive of the tools, named DeDRM\_tools\_X.X.X.zip, where X.X.X is the version number. You do not need to download the source code archive.

## I've downloaded the tools archive. Now what?
First, unzip the archive. You should now have a DeDRM folder containing several other folders and a ReadMe\_First.txt file. Please read the ReadMe\_First file! That will explain what the folders are, and you'll be able to work out which of the tools you need.

## That's a big complicated ReadMe file! Isn't there a quick guide?
Install calibre. Install the DeDRM\_plugin in calibre. Install the Obok\_plugin in calibre. Restart calibre. In the DeDRM_plugin customisation dialog add in any E-Ink Kindle serial numbers and your B&N account email address and password. Remember that the plugin only tries to remove DRM when ebooks are imported, not at any other time.

# Breaking News
### The recent (September 2016) Kobo Desktop update to version 4.0.x has added encryption to the database of ebooks. A test version of the obok plugin can be downloaded directly from the repository here: https://github.com/apprenticeharper/DeDRM_tools/tree/master/Obok_calibre_plugin
 
# Installing the Tools
## The calibre plugin
### I am trying to install the calibre plugin, but calibre says "ERROR: Unhandled exception: InvalidPlugin: The plugin in u’[path]DeDRM\_tools\_6.4.3.zip’ is invalid. It does not contain a top-level \_\_init\_\_.py file"
You are trying to add the tools archive (e.g. DeDRM\_tools\_6.4.3.zip) instead of the plugin. The tools archive is not the plugin. It is a collection of DRM removal tools which includes the plugin. You must unzip the archive, and install the calibre plugin (DeDRM\_plugin.zip) from a folder called “DeDRM\_calibre_plugin” in the unzipped archive.

### I’ve unzipped the tools archive, but I can’t find the calibre plugin when I try to add them to calibre. I use Windows.
You should select the zip file that is in the “DeDRM\_calibre\_plugin” folder, not any files inside the plugin’s zip archive. Make sure you are selecting from the folder that you created when you unzipped the tools archive and not selecting a file inside the still-zipped tools archive.

(The problem is that Windows will allow apps to browse inside zip archives without needing to unzip them first. If there are zip archives inside the main zip archives, Windows will show them as unzipped as well. So what happens is people will unzip the DeDRM\_tools\_X.X.X.zip to a folder, but when using calibre they will actually navigate to the still zipped file by mistake and cannot tell they have done so because they do not have file extensions showing. So to the unwary Windows user, it appears that the zip archive was unzipped and that everything inside it was unzipped as well so there is no way to install the plugins.

We strongly recommend renaming the DeDRM\_tools\_X.X.X.zip archive (after extracting its contents) to DeDRM\_tools\_X.X.X_archive.zip. If you do that, you are less likely to navigate to the wrong location from inside calibre.)

## The Windows Application
### I've installed ActiveState Python and PyCrypto, but the Windows application won't run. What have I done wrong?
Nothing. There's a bug in the current ActiveState Python Windows installer that puts the Tcl code in the wrong place. See [this comment of mine at ActiveState community](https://community.activestate.com/node/19090). Just move the Tcl code and the Windows app should run.

## The Macintosh Application
### I can't open the Macintosh Application. Some message about it not being signed or something.
Try right-clicking and select open. That might give you the option to open it anyway. Otherwise you'll need to change your security settings to allow unsigned applications to run. You can probably change these back after running it for the first time.

# Using the Tools
## I can’t get the tools to work on my rented or library ebooks.
Support for removing DRM from rented or library ebooks is not provided.

## I've unzipped the tools, but what are all the different files, and how do I use them?
Read the ReadMe_First.txt file and the ReadMe files included in the tools folder. That's what they're for.

## I have installed the calibre plugin, but my books still have DRM. When I try to view or convert my books, calibre says they have DRM.
The DRM only gets removed when the ebook is imported into calibre. If the book is already in calibre, by default calibre will discard the newly imported file. You can change this in calibre's Adding books preferences page (Automerge..../Overwrite....), so that newly imported files overwrite existing ebook formats. Then just re-import your books and the DRM-free versions will overwrite the DRMed versions while retaining your books' metadata.

## I have installed the calibre plugin or I am trying to use one of the other tools, but I don’t know where my ebooks are stored.
Your ebooks are stored on your computer or on your ebook reader. You need to find them to be able to remove the DRM. If they are on your reader, you should be able to locate them easily. On your computer it’s not so obvious. Here are the default locations.

### Macintosh
Navigating from your home folder,

Kindle for Mac ebooks are in either Library/Application Support/Kindle/My Kindle Content or Documents/My Kindle Content or Library/Containers/com.amazon.Kindle/Data/Library/Application Support/Kindle/My Kindle Content, depending on your version of Kindle for Mac.

Adobe Digital Editions ebooks are in Documents/Digital Editions

### Windows
Navigating from your My Documents folder

Kindle for PC ebooks are in My Kindle Content

Adobe Digital Editions ebooks are in My Digital Editions


## I have installed the calibre plugin, and the book is not already in calibre, but the DRM does not get removed.
You must use the exact file that is used by your ebook reading software or hardware. See the previous question on where to find your ebook files. Do not use an old copy you have that you can no longer read.
If you cannot read the ebook on your current device or installed software, the tools will certainly not be able to remove the DRM. Download a fresh copy that does work with your current device or installed software.

## I have installed the calibre plugin, and the book is not already in calibre, but the DRM does not get removed. It is a Kindle book.
If you are on Windows 8 and using the Windows 8 AppStore Kindle app, you must download and install the Kindle for PC application directly from the Amazon website. The tools do not work with the Windows 8 AppStore Kindle app.

If you are on Windows, using the Kindle for PC application, and your windows user name has accented or other non-ASCII characters in it, this might cause the plugin to fail. Create a new user account with an ASCII-only username. Install and register Kindle for PC there, and see if things work running calibre and the plugin in that user account.

If this book is from an eInk Kindle, you must enter the serial number into the configuration dialog. The serial number is sixteen characters long, and is case-sensitive.

If this book is from Kindle for Mac or Kindle for PC, you must have the Kindle Software installed on the same computer as your copy of calibre.

If the book is from Kindle for PC or Kindle for Mac and you think you are doing everything right, and you are getting this message, it is possible that the files containing the encryption key aren’t quite in the format the tools expect. To try to fix this:

1. Deregister Kindle for PC(Mac) from your Amazon account.
1. Uninstall Kindle for PC(Mac)
1. Delete the Kindle for PC(Mac) preferences
    * PC: Delete the directory [home folder]\AppData\Local\Amazon (it might be hidden) and [home folder]\My Documents\My Kindle Content
    * Mac: Delete the directory [home folder]/Library/Application Support/Kindle/and/or [home folder]/Library/Containers/com.amazon.Kindle/Data/Library/Application Support/Kindle/ (one or both may be present and should be deleted)
1. Reinstall Kindle for PC(Mac)
1. Re-register Kindle for PC(Mac) with your Amazon account
1. Download the ebook again. Do not use the files you have downloaded previously.

## Some of my books had their DRM removed, but some still say that they have DRM and will not convert.
There are several possible reasons why only some books get their DRM removed.
* You still don’t have the DRM removal tools working correctly, but some of your books didn’t have DRM in the first place.
* You added your books to calibre in large batches. For some unknown reason, sometimes calibre stops using the plugin after a while on a single import. Delete the books that still have DRM and import them into calibre in batches of twenty.
* Kindle only: It is a Topaz format book and contains some coding that the tools do not understand. You will need to get a log of the deDRM attempt, and then send the book and the PID (shown in the log) for the book to Apprentice Alf, so that the tools can be updated.

If you are still having problems with particular books, you will need to create a log of the DRM removal attempt for one of the problem books, and post that in a comment at Apprentice Alf's blog or in a new issue at Apprentice Harper's github repository.

## My Kindle book has imported and the DRM has been removed, but all the pictures are gone.
Most likely, this is a book downloaded from Amazon directly to an eInk Kindle (e.g. Paperwhite). Unfortunately, the pictures are probably in a .azw6 file that the tools don't understand. You must download the book manually from Amazon's web site "For transfer via USB" to your Kindle. When you download the eboook in this manner, Amazon will package the pictures in the with text in a single file that the tools will be able to import successfully.

## My Kindle book has imported, but it's showing up as an AZW4 format. Conversions take a long time and/or are very poor.
You have found a Print Replica Kindle ebook. This is a PDF in a Kindle wrapper. Now the DRM has been removed, you can extract the PDF from the wrapper using the KindleUnpack plugin. Conversion of PDFs rarely gives good results.

## The tools can't see an ebook that was downloaded directly to my eInk kindle, although it's definitely there, and I can read it on the Kindle. I can't even try to import it.
Mostly likely, this is a book downloaded from Amazon directly to one of the newer eInk Kindles (e.g. Paperwhite). Unfortunately, it is probably in a new multi-file KFX format that the tools don't understand. You must download the book manually from Amazon's web site "For transfer via USB" to your Kindle. When you download the ebook in this manner, Amazon will send a single KF8-format file that the tools will be able to import successfully.

## Do the tools work on books from Kobo?
If you use the Kobo desktop application for Mac or PC, install the obok plugin. This will import and remove the DRM from your Kobo books, and is the easiest method for Kobo ebooks.

## I registered Adobe Digital Editions with an Adobe ID before downloading, but my epub or PDF still has DRM.
Adobe introduced a new DRM scheme with ADE 3.0 and later. Install ADE 2.0.1 and register with the same Adobe ID. If you can't open your book in ADE 2.01, then you have a book with the new DRM scheme. These tools can't help. You can avoid the new DRM scheme by always downloading your ebooks with ADE 2.0.1. Some retailers will require ADE 3.0+, in which case you won't be able to download with ADE 2.0.1.

## The DRM wasn't removed and the log says "Failed to decrypt with error: Cannot decode library or rented ebooks." What now?
You're trying to remove the DRM from an ebook that's only on loan to you. No help will be given to remove DRM from such ebooks. If you think that you have received this message for a book you own, please create an issue at github, or comment at the blog.

## I cannot solve my problem with the DeDRM plugin, and now I need to ‘post a log’. How do I do that?
Remove the DRMed book from calibre. Click the Preferences drop-down menu and choose 'Restart in debug mode'. Once calibre has re-started, import the problem ebook. Now close calibre. A log will appear that you can copy and paste into a comment at Apprentice Alf's blog, or into a new issue at Apprentice Harper's github repository.

## I cannot solve my problem with the Macintosh DeDRM application, and now I need to ‘post a log’. How do I do that?
The Macintosh DeDRM application creates a log file on your desktop every time it is run. After unsuccessfully removing DRM from one ebook, copy the contents of the log file (it is a simple text file) and paste it into your comment at Apprentice Alf's blog or in a new issue at Apprentice Harper's github repository.

## I cannot solve my problem with the Windows DeDRM application, and now I need to ‘post a log’. How do I do that?
The Windows DeDRM application creates a log file in your home directory (C:\Users\[username]) every time it is run. After unsuccessfully removing DRM from one ebook, copy the contents of the log file (it is a simple text file) and paste it into your comment at Apprentice Alf's blog or in a new issue at Apprentice Harper's github repository.


# General Questions

## Once the DRM has been removed, is there any trace of my personal identity left in the ebook?
The tools only remove the DRM. No attempt is made to remove any personally identifying information.

## What do some of my Kindle ebooks import as HTMLZ format in calibre?
Most Amazon Kindle ebooks are Mobipocket format ebooks, or the new KF8 format. However, some are in a format known as Topaz. The Topaz format is only used by Amazon. A Topaz ebook is a collections of glyphs and their positions on each page tagged with some additional information from that page including OCRed text (Optical Character Recognition generated Text) to allow searching, and some additional layout information. Each page of a Topaz ebook is effectively a description of an image of that page. To convert a Topaz ebook to another format is not easy as there is not a one-to-one mapping between glyphs and characters/fonts. To account for this, two different formats are generated by the DRM removal software. The first is an html description built from the OCRtext and images stored in the Topaz file (HTMLZ). This format is easily reflowed but may suffer from typical OCRtext errors including typos, garbled text, missing italics, missing bolds, etc. The second format uses the glyph and position information to create an accurate scalable vector graphics (SVG) image of each page of the book that can be viewed in web browsers that support svg images (Safari, Firefox 4 or later, etc). Additional conversion software can be used to convert these SVG images to an image only PDF file. The DeDRM and Kindlebooks tools from this site provide both versions of the Topaz ebook so that the user can choose which one to use. The K4MobiDeDRM plugin only produces the html version of the ebook. The html version can be manually cleaned up and spell checked and then converted using Sigil/calibre to epubs, mobi ebooks, and etc.

## Are the tools open source? How can I be sure they are safe and not a trojan horse?
All the DRM removal tools hosted here are almost entirely scripts of one kind or another: Python, Applescript or Windows Batch files. So they are inherently open source, and open to inspection by everyone who downloads them. The source for any compiled pieces are provided right inside the tools themselves.

## What ebooks do these tools work on?
The tools linked from this blog remove DRM from PDF, ePub, kePub (Kobo), eReader, Kindle (Mobipocket, KF8, Print Replica and Topaz) format ebooks using Adobe Adept, Barnes & Noble, Amazon, Kobo and eReader DRM schemes.

Note these tools do NOT ‘crack’ the DRM. They simply allow the book’s owner (and only the book’s owner) to use the encryption key information already stored someplace on their computer or device to decrypt the ebook in the same manner the official ebook reading software uses.

## Why don’t the tools work with Kindle Fire ebooks?
Because no-one's found out how to remove the DRM from ebooks from Kindle Fire devices yet. The workaround is to install Kindle for PC or Kindle for Mac and use books from there instead.

## Why don't the tools work with Kindle for iOS ebooks?
Amazon changed the way the key was generated for Kindle for iOS books, and the tools can no longer find the key. The workaround is to install Kindle for PC or Kindle for Mac and use books from there instead.

## Why don't the tools work with Kindle for Android ebooks?
Amazon turned off backup for Kindle for Android, so the tools can no longer find the key. The workaround is to install Kindle for PC or Kindle for Mac and use books from there instead.

## Why don't the tools work on books from the Apple iBooks Store?
Apple regularly change the details of their DRM and so the tools in the main tools archive will not work with these ebooks. Apple’s Fairplay DRM scheme can be removed using Requiem if the appropriate version of iTunes can still be installed and used. See the post Apple and ebooks: iBookstore DRM and how to remove it at Apprentice Alf's blog for more details and links.

## I’ve got the tools archive and I’ve read all the FAQs but I still can’t install the tools and/or the DRM removal doesn’t work
* Read the ReadMe_First.txt file in the top level of the tools archive
* Read the ReadMe file in the folder of the tools you want to use.
* If you still can’t remove the DRM, ask in the comments section of Apprentice Alf's blog, reporting the error as precisely as you can, what platform you use, what tool you have tried, what errors you get, and what versions you are using. If the problem happens when running one of the tools, post a log (see previous questions on how to do this).

## Who wrote these scripts?
The authors tend to identify themselves only by pseudonyms:
* The Adobe Adept and Barnes & Noble scripts were created by i♥cabbages
* The Amazon Mobipocket and eReader scripts were created by The Dark Reverser
* The Amazon K4PC DRM/format was further decoded by Bart Simpson aka Skindle
* The Amazon K4 Mobi tool was created by by some_updates, mdlnx and others
* The Amazon Topaz DRM removal script was created by CMBDTC
* The Amazon Topaz format conversion was created by some_updates, clarknova, and Bart Simpson
* The DeDRM all-in-one AppleScript application was created by Apprentice Alf
* The DeDRM all-in-one Python application was created by some_updates
* The DeDRM all-in-one calibre plugins was created by Apprentice Alf
* The Scuolabooks tool was created by Hex
* The Microsoft code was created by drs
* The Apple DRM removal tool was created by Brahms

Since the original versions of the scripts and programs were released, various people have helped to maintain and improve them.
