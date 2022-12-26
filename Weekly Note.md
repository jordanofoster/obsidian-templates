<%*
	let zettelID = tp.date.now("YYYYMMDDHHmmss");
	let dateShorthand = tp.date.now("GGGG-[W]WW");
	let prettifiedDate = tp.date.now("wo [Week of] YYYY");
_%>
---
id: <% `${zettelID}` %>
title: "<% `${prettifiedDate}` %>"
desc: "<% `Weekly Note for the ${prettifiedDate}` %>"
updated: 
created: <% tp.file.creation_date("X") %>
week: <% `${dateShorthand}` %>
---

# <% `${prettifiedDate}` %>