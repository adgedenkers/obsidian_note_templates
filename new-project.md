<%*
	tR += "---"
	
	// create a title for the project
	let title = tp.file.title
	if(title.startsWith("Untitled")) {
		title = await tp.system.prompt("Project Title");
	}
	await tp.file.rename(title)
	
	let type = "project note"
	
	let display_title = "Project - "
	display_title += title
	
	// set the tags
	let tags = "#project"
	let project_tag = await tp.system.prompt("Project Tag")
	tags += " "
	tags += project_tag
	
	// set date variables
	let dt = tp.date.now("YYYY-MM-DD")
	let df = tp.date.now("DD MMM YYYY")
	let project_status = "open"
%>
<%* tR %>title: 			"<% display_title %>"
type:			"<% type %>"
tags:			"<% tags %>"
date-created: 	"<% dt %>"
project-status: 	"<% project_status %>"

---
# <% title %>