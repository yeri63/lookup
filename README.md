# lookup

![Screenshot of Lookup](https://github.com/yeri63/lookup/blob/master/lookup.png)

<p>This project was created to solve a problem, that writing notes down in a Moleskin notebook couldn't quite solve. The paper solution was very compact and convenient, drop resistant, and free from batteries or having to recharge. I used the following  method to record information for latter retrieval, described below...</p>

* Reserved pages at the beginning to create a Table of Contents. Actual notes were recorded between 3-5 pages in.
* Wrote page numbers at the bottom of every page, to help quickly locate those pages with the data I needed to recall.
* Updated the Table of Contents for every project, one line per project, noting the individual pages with that information.
  
<p>This method worked, but was slow. When the notebook was full, another had to be purchased, requiring more notebooks to be scanned. This would take longer as the number of notebooks increased. Another issue was recording multiple commands, results, procedures, or troubleshooting steps. Writing these by hand was painfully slow, inefficient, and error prone. There had to be a quicker way, both to record and retrieve.</p>
<p>The next evolution came as I become more proficient in Linux, using vi for creating scripts and keeping notes. Typing was much faster, letting me easily record scripts, command output, develop and record procedures, etc. using cut&paste. I was able to collect reports, take meeting notes, record names and contact information, etc. Basically all the stuff I used to record before, but now at a much faster rate and larger scale. The best part, was that it was all easily searchable, using basic linux commands like grep, sed, more, less, and awk for more complex tasks.</p>
<p>Now that I found a way to quickly search through a text file, the next step was considering how to organize it. Putting everything into one increasingly large file seemed risky, especially if the file got corrupted or accidentally deleted. I needed to break this down into smaller, manageable pieces, but not so small as to generate thousands of files. I wanted to keep track of when the notes were made, so thought of keeping a monthly log, with daily markers to identify the date of each entry. Using this method, only 12 files would be needed to record a years worth of data, which seemed like a reasonable trade off.</p>
<p>The last step was designing an easy way to lookup my information, without resorting linux searches and filters every time. It had to be quick, and easy to use, much like Google, when searching through vast troves if information, generating results in less than a second. This was the key which lead to creation a text version of Google, where each search would accept multiple terms, and present results to the user, in a format similar to Google, a list of links, each followed by a brief excerpt, in reverse date order. Instead of webpages, the results brought back my data, visible in a scrolling text window on the terminal screen.</p>

## File Structure

* Create a folder titled Dailylog in the Documents folder. This will contain all of the files with the data to be saved and searched. Create a file for the current month, using the format "dailylog-yyyy--mm.txt".
* This will be a Linux, not Windows ASCII text file, using LF instead of CR/LF at the end of every line. Content is stored and retrieved as articles, and article sections. An article can contain multiple sections, or none. All date, article and section markers should be entered between 2 blank lines, to help the search engine parse content.
* The first line in the file should contain the date of the first entry, using the format "Www, dd-Mmm-yyyy. Separate articles on the same date with a line beginning with 2 dashes, ie. "--". Separate sections within the same article with a line beginning with 3 dashes, ie. "---". Before adding articles on a new day, add a date marker. The last article of the month must end with a line with beginning with 2 dashes, ie. "--".

dailylog-2026-10.txt

    Mon, 05-Oct-2026

    Article 1 content
    line 2
    line 3

    ---

    Article 1 content, Section 2
    line 2
    line 3

    Tue, 06-Oct-2026
    
    Article 2 content
    line 2
    line 3
    ...

    --
  
## How to Search

<p>To use lookup, just enter one or more keywords after the lookup command. Use more keywords to narrow down the search to fewer hits. Otherwise, you'll end up with a large list to review. The order of keywords is critical, ie. the results will be all articles containing keyword1, and from those results, all articles containing keyword2, etc. You also have the option to search for all articles not containing a keyword by attaching a "-" in front of that word.</p>

## Reviewing Hits and Selecting Article to Open

<p>The hits are displayed as a list of numbered results. Each hit will show the date, filename, line number, and a short 2-3 line excerpt containing the keyword(s). Below this list, on the bottom edge of the screen is the list of pages of hit results. The height of the terminal window determines how many results are shown per page, which then determines the number if pages. To advance to the next pages of hits, press the <spacebar>, press the letter "b" to go back, or "q" to quit and exit.</p>
<p>To open up a result for review, enter the number next to it. Once inside, press the letter "n" to go to the next keyword instance within the article, or "p" to go back to the previous one. Use the up and down arrow to move one line up or down, and "q" to quit and return to the current page of search results.</p>
<div align="center">

Location | Key | Action
:-- | :-- | :--
Search Results | <space> | Next Page
Search Results | "p" | Prev Page
Search Results | "q" | Quit and Exit
Viewing Article | "n" | Next Keyword Hit
Viewing Article | "p" | Prev Keyword Hit
Viewing Article | "q" | Quit and Return
</div>
