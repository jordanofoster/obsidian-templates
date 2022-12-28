<%*
	let zettelID = tp.date.now("YYYYMMDDHHmmss");
	let noteTitle = await tp.system.prompt("Title",tp.file.title,true);
	let noteDesc = await tp.system.prompt("Description",null,true);
	await tp.file.rename(zettelID);
_%>
---
id: <% zettelID %>
title: "<% noteTitle %>"
desc: "<% noteDesc %>"
updated: 
created: <% tp.file.creation_date("X") %>
---

# <% noteTitle %>