<%*
    let classificationList = [
        "PUBLIC",
        "PERSONAL",
        "PRIVATE",
        "SECRET"
    ];
    
	let zettelID = tp.date.now("YYYYMMDDHHmmss");
	let noteTitle = await tp.system.prompt("Title",tp.file.title,true);
	let noteDesc = await tp.system.prompt("Description",null,true);
	await tp.file.rename(zettelID);
_%>
---
id: <% zettelID %>
title: "<% noteTitle %>"
desc: "<% noteDesc %>"
classification: <% `"[[${await tp.system.suggester(classificationList,classificationList,true,"CLASSIFICATION")}]]"` %>
updated: 
created: <% tp.file.creation_date("X") %>
---

# <% noteTitle %>

