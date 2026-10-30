# lookup.sh

![Screenshot of Lookup](https://github.com/yeri63/lookup/blob/master/lookup.png)

<p>This project was created to solve a problem, that writing notes down in a moleskin notebook couldn't quite solve. The paper solution was very compact and convenient, not taking up much room, drop resistant, and free from batteries or having to recharge. I tried multiple methods of recording information for latter retrieval, including the following...</p>

* Purchase a compact, college ruled notebook, with flexible cover that was waterproof, ie. Moleskin Notebook.
* Reserving pages at the beginning for creating a Table of Contents. Actual notes were recorded between 3-5 pages in.
* Writing page numbers at the bottom of every page, to quickly locate pages with information I was looking to retrieve.
* Updating the Table of Contents for every project, one line each, noting the individual pages with that information.
  
<p>This method worked, but it was slow, and when the notebook was full, and another was purchased, I would have to scan multiple notebooks to locate what I was looking for, provided that information was recorded. When this involved research online, or recording sequences of commands, learned procedures, or impromptu written scripts, handwriting these was painfully slow and inefficient. There had to be a quicker way, both to record and retrieve.</p>
<p>The next evolution came as I become more proficient in Linux using vi for creating scripts or keeping notes. It was fast, and let me easily record lengthy scripts, step by step procedures, troubleshooting notes, command results and reports, meeting notes, names and contact information of technicians and engineers, etc. Basically all the stuff I used to record before, but at a much faster rate and larger scale. The best part of all was that it was searchable, using basic linux commands like grep, sed, more, less, and awk for more complex tasks.</p>
<p>Now that I found a way to quickly search through a text file, the next step was considering how to organize this information. Putting everything into one increasingly large file seemed risky, especially if this file got corrupted or accidentally deleted. I need to figure out how to break this down into smaller, manageable pieces, but not so small as to generate thousands of files. I wanted to keep track of when the notes were made, so thought of keeping a monthly log, with daily markers to separate into daily notes. Using this method, only 12 files would be needed to record a years worth of data, which seemed like a reasonable trade off.</p>
<p>The last step was designing an easy way to lookup information, without resorting linux searches and filters every time. This led to the idea to create a text version of Google, where the search would accept multiple terms, and present results to the user in much the same manner as Google did, displaying a list of links, followed by a brief excerpt, in reverse date order. Instead of webpages, the results brought back my notes for review in a scrolling text window on the terminal screen.</p>


