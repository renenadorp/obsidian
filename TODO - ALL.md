# TODO 

 ```dataview


TABLE WITHOUT ID  
 regexreplace(file.folder, ".*/", "") as Project
, td AS "ToDo"

, "[Link]("+replace(file.path, " ", "%20")+")" as "Link"
, file.folder as Folder

FROM "Work/HSO" 
WHERE length(td)>0
SORT file.folder


```
```dataviewjs  
dv.header(2, 'TASKS');  
dv.taskList(dv.pages().file.tasks.where(t => !t.completed));  
```
# DONE
```dataview


TABLE WITHOUT ID  
 regexreplace(file.folder, ".*/", "") as Project
, DN AS "Done"

, "[Link]("+replace(file.path, " ", "%20")+")" as "Link"
, file.folder as Folder

FROM "Work/HSO" 
WHERE length(DN)>0
SORT file.folder


```


# Dataview Snippets
 
 ```
 elink(("obsidian://open?vault=myBrain&file=" + replace(file.path, " ", "%20"))) as "Link"
 TABLE WITHOUT ID
 ```






