<%*
	let zettelID = tp.date.now("YYYYMMDDHHmmss");
	let dateShorthand = tp.date.now("YYYY-MM");
	let prettifiedDate = tp.date.now("MMMM YYYY");
_%>
---
id: <% `${zettelID}` %>
title: "<% `${prettifiedDate}` %>"
desc: "<% `Monthly Note for ${prettifiedDate}` %>"
updated: 
created: <% tp.file.creation_date("X") %>
month: <% `${dateShorthand}` %>
---

# <% `${prettifiedDate}` %>