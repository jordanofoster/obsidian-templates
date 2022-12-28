<%*
	let tagList = await Object.keys(app.metadataCache.getTags());
	let chosenTag = await tp.system.suggester(tagList,tagList);
	let filename = await chosenTag.substr(1);
	let noteDesc = await tp.system.prompt("Description",`Tag Note - ${chosenTag}`,true);
	await tp.file.rename(filename);
_%>
---
BC-tag-note: "<% chosenTag %>"
BC-tag-note-field: down
title: "<% chosenTag %>"
updated: 
created: <% tp.file.creation_date("X") %>
---

# \<% chosenTag %>

```dataview
TABLE title as "Title", desc as "Description", file.ctime as "Created", file.mtime as "Modified" FROM <% chosenTag %>
WHERE file.name != "<% filename %>"
SORT file.name DESC
```