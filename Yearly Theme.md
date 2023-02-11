<%*
    let themeName = await tp.system.prompt(`This is the Year of... `, null, true);
	let noteTitle = await tp.system.prompt("Title",`${seasonType} of ${seasonName}`,true);
	let noteDesc = await tp.system.prompt("Description",`Note for the ${seasonType} of ${seasonName}`,true);
	await tp.file.rename(`${tp.date.now("YYYY")}_Year_of_${themeName}`);
_%>
---
title: "<% noteTitle %>"
desc: "<% noteDesc %>"
updated: 
created: <% tp.file.creation_date("X") %>
tags:
- theme/seasonal
---

# The Season of <% seasonName %>

## Description



## Ideal Outcomes




