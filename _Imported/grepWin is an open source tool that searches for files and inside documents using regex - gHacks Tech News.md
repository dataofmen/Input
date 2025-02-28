
What's your preferred desktop search engine program? The answer is likely [Everything](https://www.ghacks.net/2017/06/07/everything-desktop-search-review/), by Void Tools. I agree with you, it is a fantastic application.

![](Assets/grepWin-is-an-open-source-tool-that-searches-for-files-and-inside-documents-using-regex.jpg)
GrepWin is an [open source](https://github.com/stefankueng/grepWin/) program that specializes in finding text in documents; it supports advanced regular expression filters, and you may want to give it a try for that purpose.

The program's interface is not the most user-friendly, but that's probably an impression caused by the various options on the screen.

![](Assets/grepWin-example.jpg)
Select the folder that you want to search by clicking the three-dot button at the top. Enter your query in the box that's labeled "Search For". For a more advanced approach, you may opt for the Regex search mode. GrepWin even has a test regex option for checking if your regular expression works or not. Hit F1 to view the help file, it has a list of all supported regex syntax.

![](Assets/grepWin-regex-commands.jpg)
Hit the enter key or click on the search button to make the query and grepWin will list the results on the pane at the bottom. The information is split into various columns, such as file name, size, path, extension, encoding, and date modified. Double-click on a file to open it in its default app, e.g. TXT files in Notepad, audio files in your music player, and so on. Right-click on a result to access the Explorer shell menu.

GrepWin could list a ton of files, and if you have trouble finding the one you wanted, I recommend playing around with the Limit Search settings to restrict the process by file size, date, hidden, system or binary files, disabling recursive search (subfolders). This also shortens the time taken for the search to complete by a considerable duration.

![](Assets/grepWin-regex-search.jpg)
You can blacklist specific folders from searches using the exclude dirs box, the syntax is ^(FOLDERNAME)$. To include file types, use wildcards like *.TXT, and to exclude types, add a - before it. You may add | to separate multiple items. Speaking of regular expressions, you can add the ones you use to the presets, which will help you add them quickly the next time. Don't feel intimidated by these options, you don't need to know regex commands to use the program for simple searches, though by doing so you'll be missing out on some of its strongest filters.

Switch between the Files search mode and the Content finder by toggling the option in the bottom right corner of the window. This changes the columns in the search results pane, to display the relevant information. The Files mode lists the name, path of the documents which contain the search term.

GrepWin's content mode can search inside documents and list every instance the phrase was found in each document along with the line name and a preview of the text. The application supports case-sensitive search, which can be handy if there are a lot of matches, and you want to filter them based on the case. The application can be used to replace content in documents directly, to use this option enter the words in the replace with box, and click on the Replace button. You may want to enable the create backup file option, before using the replace function.

The Search button in grepWin has a few additional options including an inverted lookup, i.e. find files that don't match the entered query. You can also use it to run a search within the found results.

GrepWin is available for 32-bit and 64-bit computers, and comes in portable versions. If you're using the installer version, you can access the program from the Windows Explorer context menu.

[DnGrep](https://www.ghacks.net/2020/01/22/dngrep-is-an-open-source-tool-that-can-search-for-text-inside-documents/) is a similar software, in fact it is nearly identical to grepWin. I'm not sure if one of them is a fork of the other.

Advertisement
[grepWin is an open source tool that searches for files and inside documents using regex - gHacks Tech News](https://www.ghacks.net/2021/04/09/grepwin-is-an-open-source-tool-that-searches-for-files-and-inside-documents-using-regex/)