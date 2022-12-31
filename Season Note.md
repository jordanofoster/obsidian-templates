<%*
	let seasonName = await tp.system.prompt("This is the season of... ", null, true);
	let noteTitle = await tp.system.prompt("Title",`Season of ${seasonName}`,true);
	let noteDesc = await tp.system.prompt("Description",`Note for season - ${seasonName}`,true);
	await tp.file.rename(`season-of-${seasonName.toLowerCase()}`);
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




