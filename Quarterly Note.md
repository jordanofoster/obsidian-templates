<%*
	let classificationList = [
        "PUBLIC",
        "PERSONAL",
        "PRIVATE",
        "SECRET"
    ];
 
    let zettelID = tp.date.now("YYYYMMDDHHmmss");
	let dateShorthand = tp.date.now("YYYY-[Q]Q");
	let prettifiedDate = tp.date.now("Qo [Quarter of] YYYY");
	await tp.file.rename(dateShorthand);
_%>
---
id: <% zettelID %>
title: "<% prettifiedDate %>"
desc: "<% `Quarterly Note for the ${prettifiedDate}` %>"
classification: <% `"[[${await tp.system.suggester(classificationList,classificationList,true,"CLASSIFICATION")}]]"` %>
updated: 
created: <% tp.file.creation_date("X") %>
quarter: <% dateShorthand %>
up: "<% `[[${tp.date.now("YYYY")}]]` %>"
prev: "<% `[[${moment().subtract(1,"Q").format("YYYY-[Q]Q")}]]` %>"
next: "<% `[[${moment().add(1,"Q").format("YYYY-[Q]Q")}]]` %>"
tags:
- journal
---

# <% prettifiedDate %>

