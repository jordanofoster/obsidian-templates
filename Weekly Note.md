<%*
	let zettelID = tp.date.now("YYYYMMDDHHmmss");
	let dateShorthand = tp.date.now("GGGG-[W]WW");
	let prettifiedDate = tp.date.now("wo [Week of] YYYY");
	await tp.file.rename(dateShorthand);
_%>
---
id: <% zettelID %>
title: "<% prettifiedDate %>"
desc: "<% `Weekly Note for the ${prettifiedDate}` %>"
updated: 
created: <% tp.file.creation_date("X") %>
week: <% dateShorthand %>
up: "<% `[[${tp.date.now("YYYY-MM")}]]` %>"
prev: "<% `[[${moment().subtract(1,"w").format("GGGG-[W]WW")}]]` %>"
next:  "<% `[[${moment().add(1,"w").format("GGGG-[W]WW")}]]` %>"
tags:
	- journal
---

# <% prettifiedDate %>