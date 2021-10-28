<%*
	let title = tp.file.title
	let tags = '#adge-tasks'
	let type = "individual task notes"
	tR   += "---";
	let scope = await tp.system.prompt("Scope: Home or VA?")
	if(scope == "VA") {
		tags += " #va-task"
	} else {
		tags += " #personal"
	}
	if(title.startsWith("Untitled")) {
		title = await tp.system.prompt("What is the title of the Task?");
	}
	let dt = tp.date.now("YYYY-MM-DD")
	let priority = await tp.system.prompt("If 'High Priority', type 'high', Otherwise press <Enter>")
	if (priority == "high") {
		tags += " #high-priority"
	}

	await tp.file.rename(title)

%>
<%* tR %>title: 			"<% title %>"
type:			"<% type %>"
tags:			"<% tags %>"
date-created: 	"<% dt %>"

---
# <% title %>

*<% dt %>*

*Adge Denkers | adge.denkers@gmail.com*

## Notes

<% tp.file.cursor() %>

## Contacts


