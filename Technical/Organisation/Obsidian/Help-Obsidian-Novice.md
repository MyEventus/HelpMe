---  
last_update: 2023Apr16  
share: true    
---  
  
#help #org-micromacro   
  
  
# Overview  
  
 [Obsidian](http://obsidian.md)   
Download for free.  
Online version is not free.  
But you can host on your own shared or cloud service e.g. MS Office365.  
  
  
<b>Tags</b>  
  
Whilst there are so many advantages to Obsidian Notes over most other Note taking apps, "Tags" are one of the main ones.  
  
No need for Folders or Directors... "AT ALL".  
No more directories within sub-directories within sub-directories etc  
  
Exception: To keep related images or attachments together in an auto created sub-directory.   
See Settings > Files and Links > Default location for new attachments > I suggest use "in subfolder under current folder".  
  
<b>Ignore / Hide</b>  
Enter text between 2 percentage signs e.g. %% hide this %%  
  
<b>Mobile App</b>  
  
Yes, Android and Apple.  
  
<b>Strongly Suggest!</b>  
  
Store all you files in the top level. Flat or No hierarchically!  
Just add one or more tags e.g. "#dept-sales" and "#os-windows"  
  
  
<b>Future proof</b>   
  
Future proof is another i.e. all doc's are simply text files with .md extension stored on you local drive or shared drive, git repository (private or public), cloud storage (share with your team).  
  
The one and only downside of Obsidian is that no intended for teams use.  
i.e. No permissions or authentication to restrict others from viewing or editing (perhaps someone will make an app / docker / system in the future)  
  
<b>Graph View</b>  
  
See how your notes are related to one another.  
  
Select "More Options" (top right vertical ellipse, 3 dots) of each page > Open local graph.  
  
<b>Fast Find</b>  
  
Incredibly fast search and filter capabilities.  
Note: Not sure how it scales to millions of docs yet?  
  
<b>DRY</b>  
  
Don't Repeat Yourself.  
There is now no reason to duplicate any data / info.  
Use reciprocal links from one Master doc, can link to another sub doc's (and back again with Backlinks)  
  
<b>Back Links</b>  
  
You can now see where a link came from i.e. the source or what other documents have been linked to this current one.  
Right menu > Left arrow / chevron > link icon ("Backlinks")  
  
<b>Templates</b>  
  
Create templates (with pre entered meta data) for statndardisation of common tasks / knowledge.  
  
<b>Side By Side Editing and Viewing</b>  
  
Work on 4 or more pages at the same time.  
Great for copy / paste.  
  
<b>Encrypt Whole Vault, Page Or Text</b>   
  
Note: I'm still testing.  
Using community plugin. "Meld Encrypt".  
The following is encrypted test. Hint: password is "password"  
  
%%🔐α 💡No hint here💡g97uIX5cyexmEzWynQ/Acdv/fgAO8ky9ReMX7oNcqLyJ0pZF5uRr1pnsouoyrqlyFyFvrsvb 🔐%%  
  
To decrypt: Highlight from %% to %% then press ctrl + p on keyboard > search for "Meld Encrypt".  
  
# Tags  
Think of tags as meta data or labels (Confluence terminology)  
```  
To create a tag:  
Begin with a # e.g. #myTag1 (and no space).  
You can add anywhere within any document.  
  
To view all tags:  
1. Display the far right menu (left pointing arrow / chevron) near top right.  
2. Then select the # icon (Tag pane).  
  
The more meaning full tags you add to your documents, the easier it will be to filter / find.  
  
```  
Strongly suggest If working as a team this is Imperative that a system or format be discussed and agreed upon first!!!  
  
```  
  
Another approach is "Frontmatter" especially if need to later action calculations (e.g. hours worked on), JavaScript functionality (smarts) or SQL sort / filter / calculate logic  
  
See plugin called "DataView" community plugin.  
https://github.com/blacksmithgu/obsidian-dataview  
  
```  
  
  
  
# View and edit mode:  
Press "ctrl + e" to switch between edit and view mode.  
	Settings (cog wheel, bottom left) > Default editing mode > Change to "source mode" to simplify.  
  
  
  
  
  
# Commands:  
ctrl + p to open functions menu i.e. search for plugins already installed locally.  
  
  
  
  
# I want to see raw text (verbatim)  
Place your text between start and end of \``` 3 back ticks (Left of 1 on keyboard i.e. same as ~ key) e.g.   
  
e.g. \``` my Raw text \```  
  
  
Or for one character or a word simple proceed with the escape char backslash. \  
  
  
  
  
# Markdown:  
Think of markdown as an over simplified HTML for fast data entry (formatting)  
  
## Largest Heading.  
  
Start of new line use one hash / pound then a space then your actual text heading i.e.  
```  
# My Heading (Largest) e.g..  
## Second Largest.  
### Third largest.  
#### Fourth.  
##### Fifth.  
```  
# My Heading (Largest)  
## Second Largest.  
### Third Largest.  
#### Fourth.  
##### Fifth.  
  
  
  
```  
The more preceding hashes / pound signes the smaller the heading (to a limit of 5)  
```  
  
More Markdown help here:  
https://help.obsidian.md/How+to/Format+your+notes  
  
  
  
  
  
  
# Bullet Points  
Enter a - "hyphen" at start of new line then a space then your text.  
```  
- Point 1  
- Point 2  
```  
Will only show as bullet points in "View" mode (Ctrl + e).  
- Point 1  
- Point 2  
  
  
  
  
  
# Horizontal Line.  
Enter 3 "hyphens" at start of new line.  
Hard to see in "Black / Night" mode.   
```  
--- Horizontal line is here.  
```  
  
---  
  
  
  
  
  
# To do list.  
There are 2 main types..  
## Type 1: Simple:  
  
Must be at start of line (far left)  
```  
- [ ] Not done. (One space between [ ])  
- [ ] Sub actions to do with link [link to another doc here](link%20to%20another%20doc%20here.md)  
- [x] Done.  
  
```  
- [ ] Not done.  
	- [ ] Sub actions to do with link [link to another doc here](link%20to%20another%20doc%20here.md)  
- [x] Done.  
  
##	Type 2: Plug In Kanban board:  
Example: [To Do List. Kanban](To%20Do%20List.%20Kanban.md)  
Settings > community plugins > community plugins > Browse > search for .. "Kanban"  
  
  
  
  
  
  
# Links  
### Internal (To other Obsidian Doc's)  
```  
Anywhere on page just use [ page name ](page%20name.md) i.e. Two square brackes [ ](.md)  
  
If you're creating for the first time, soon as anyone clicks on the new link it will create a new blank page with the title as the link.  
  
Test link [this is a test link](this%20is%20a%20test%20link.md)  
```  
[ this is a test link](this%20is%20a%20test%20link.md)  
  
  
  
### To external:  
```  
[Obsidian](http://obsidian.md) if want a different title showing.  
  
or simply enter..  
  
www.google.com  
```  
[Obsidian](http://obsidian.md)  
www.google.com  
  
Press ctl+e to see in View mode.  
  
  
  
  
  
  
## Drag And Drop Images:  
Copy paste images to any doc.  
  
  
  
  
## Calendar:  
See plug ins.  
  
  
  
## Add On's or Plug Ins.  
2 Types.  
  
- Official (Part of main Obsidian install, created by Obsidian team).  
	- Settings > Core Plugins.  
- Unofficial (created by the community, most / all are free, donations accepted).  
	- Settings > Community plugins > Community plugins.  
	- You will have to disable "Restricted Mode" first.  
  
  
  
  
  
## More Help:  
https://help.obsidian.md/How+to/Format+your+notes  
  
  
  
  
  
## Suggestion:  
Before you add too many doc's best to familiarise yourself and test each global settings first. (and play with some plug ins).  
Watch a few YouTube videos on Obsidian Notes" or Obsidian.md"  
  
e.g.   
See plugin called "DataView" community plugin.  
https://github.com/blacksmithgu/obsidian-dataview