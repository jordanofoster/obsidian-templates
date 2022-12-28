<%*
	let zettelID = tp.date.now("YYYYMMDDHHmmss");
	let dateShorthand = tp.date.now("YYYY-MM-DD");
	let prettifiedDate = tp.date.now("dddd, Do MMMM YYYY");
	await tp.file.rename(dateShorthand);
_%>
---
id: <% zettelID %>
title: "<% prettifiedDate %>"
desc: "<% `Daily Note for ${prettifiedDate}` %>"
updated: 
created: <% tp.file.creation_date("X") %>
day: <% dateShorthand %>
up: "<% `[[${tp.date.now("GGGG-[W]WW")}]]` %>"
prev: "<% `[[${tp.date.yesterday("YYYY-MM-DD")}]]` %>"
next: "<% `[[${tp.date.tomorrow("YYYY-MM-DD")}]]` %>"
tags:
- journal
---

# <% prettifiedDate %>