<%*
    switch(tp.date.now("Q")) {
        case "1":
            seasonType = "Spring";
            break;
        case "2":
            seasonType = "Summer";
            break;
        case "3":
            seasonType = "Autumn";
            break;
        case "4":
            seasonType = "Winter";
            break;
        default:
            seasonType = "Season";
    }
    
    let themeName = await tp.system.prompt(`This is the ${seasonType} of... `, null, true);
	let noteTitle = await tp.system.prompt("Title",`${seasonType} of ${themeName}`,true);
	let noteDesc = await tp.system.prompt("Description",`Note for the ${seasonType} of ${themeName}`,true);
	await tp.file.rename(`${tp.date.now("YYYY-[Q]Q")}_${seasonType}_of_${themeName}`);
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




