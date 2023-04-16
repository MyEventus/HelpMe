---  
last_update: 2023Apr16  
share: true    
---  
  
## Advanced Users:  
  
## Prerequisite:   
You must install "dataview" community plugin.  
  
  
## TO_DO_2022  
```dataview  
task  
where file.name = "!To_Do_2022"  
```  
  
  
## TABLE OF CONTENTS (TOC)  
Show all notes with #moc (Table Of Content) tag.  
```dataview  
table duration from #moc  
sort name desc  
```  
  
Tagged by org-micromacro  
```dataview  
table Status, Duration, No_Control  
from #org-micromacro  
sort name desc  
```  
  
## ISSUES. ALL  
Must have a frontmatter wth "Doc_Type: issue"  
```dataview  
table Status, Duration, doc_type  
where doc_type = "issue"  
sort Created_At asc  
```  
  
  
## HOW_TO. ALL  
```dataview  
table duration   
from #doc_type = how_to  
sort name desc  
```  
  
  
```dataview  
table file.name, tags, duration, file.size, file.mtime, aliases.data, alias, tags  
from "!To_Do_2022"  
```  
  
%%  
```dataview  
  
table file.outlinks('[_help](_help.md)`)  
```  
%%  
This will display all pages with a tag of "#test3".  
  
%%  
```dataview  
  
table file.outlinks, tag, file.ctime, file.mtime  
from ""  
where [Test3](Test3.md)  
sort file.mtime desc, file.ctime.month desc  
  
```  
%%  
  
  
%%  
---  
# Show notes with the work "Test1"  
```dataview  
  
table file.name, tag  
from ""  
where file.name = "Test1"  
sort file.mtime desc, file.ctime.month desc  
  
```  
  
%%