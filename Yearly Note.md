<%*
	let zettelID = tp.date.now("YYYYMMDDHHmmss");
	let dateShorthand = tp.date.now("YYYY");
	let prettifiedDate = tp.date.now("YYYY");
	await tp.file.rename(dateShorthand);
_%>
---
id: <% zettelID %>
title: "<% prettifiedDate %>"
desc: "<% `Yearly Note for ${prettifiedDate}` %>"
updated: 
created: <% tp.file.creation_date("X") %>
year: <% dateShorthand %>
prev: "<% `[[${moment().subtract(1,"y").format("YYYY")}]]` %>"
next: "<% `[[${moment().add(1,"y").format("YYYY")}]]` %>"
tags:
	- journal
---

# <% prettifiedDate %>