<%*
	let zettelID = tp.date.now("YYYYMMDDHHmmss");
	let dateShorthand = tp.date.now("YYYY-MM-DD");
	let prettifiedDate = tp.date.now("dddd, Do MMMM YYYY");
_%>
---
id: <% `${zettelID}` %>
title: "<% `${prettifiedDate}` %>"
desc: "<% `Daily Note for ${prettifiedDate}` %>"
updated: 
created: <% tp.file.creation_date("X") %>
day: <% `${dateShorthand}` %>
---

# <% `${prettifiedDate}` %>