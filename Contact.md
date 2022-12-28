<%*
	let zettelID = tp.date.now("YYYYMMDDHHmmss");
	let noteTitle = await tp.system.prompt("Title",tp.file.title,true);
	let noteDesc = await tp.system.prompt("Description",`Page for contact - ${noteTitle}`,true);
	await tp.file.rename(zettelID);

	let contactEmail = await tp.system.prompt("Email");
	if (contactEmail != null) {
		contactEmail = `\"[${contactEmail}](mailto://${contactEmail})\"`
	}

	let contactPhone = await tp.system.prompt("Phone");
	if (contactPhone != null) {
		contactPhone = `\"[${contactPhone}](tel://${contactPhone})\"`
	}

	let contactOrg = await tp.system.prompt("Organization");
	if (contactOrg != null) {
		contactOrg = `\"${contactOrg}\"`
	}
_%>
---
id: <% zettelID %>
title: "<% noteTitle %>"
desc: "<% noteDesc %>"
updated: 
created: <% tp.file.creation_date("X") %>
details:
  email: <% contactEmail %>
  phone: <% contactPhone %>
  organization: <% contactOrg %>
---

# <% noteTitle %>