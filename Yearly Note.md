<%*
	let zettelID = tp.date.now("YYYYMMDDHHmmss");
	let dateShorthand = tp.date.now("YYYY");
	let prettifiedDate = tp.date.now("YYYY");
_%>
---
id: <% `${zettelID}` %>
title: "<% `${prettifiedDate}` %>"
desc: "<% `Yearly Note for ${prettifiedDate}` %>"
updated: 
created: <% tp.file.creation_date("X") %>
year: <% `${dateShorthand}` %>
---

# <% `${prettifiedDate}` %>