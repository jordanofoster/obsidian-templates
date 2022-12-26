<%*
	let zettelID = tp.date.now("YYYYMMDDHHmmss");
	let dateShorthand = tp.date.now("YYYY-[Q]Q");
	let prettifiedDate = tp.date.now("Qo [Quarter of] YYYY");
_%>
---
id: <% `${zettelID}` %>
title: "<% `${prettifiedDate}` %>"
desc: "<% `Quarterly Note for the ${prettifiedDate}` %>"
updated: 
created: <% tp.file.creation_date("X") %>
quarter: <% `${dateShorthand}` %>
---

# <% `${prettifiedDate}` %>