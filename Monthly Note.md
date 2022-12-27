<%*
	let zettelID = tp.date.now("YYYYMMDDHHmmss");
	let dateShorthand = tp.date.now("YYYY-MM");
	let prettifiedDate = tp.date.now("MMMM YYYY");
	await tp.file.rename(dateShorthand);
_%>
---
id: <% zettelID %>
title: "<% prettifiedDate %>"
desc: "<% `Monthly Note for ${prettifiedDate}` %>"
updated: 
created: <% tp.file.creation_date("X") %>
month: <% dateShorthand %>
up: "<% `[[${tp.date.now("YYYY-[Q]Q")}]]` %>"
prev: "<% `[[${moment().subtract(1,"M").format("YYYY-MM")}]]` %>"
next: "<% `[[${moment().add(1,"M").format("YYYY-MM")}]]`%>"
tags:
  - journal
---

# <% prettifiedDate %>