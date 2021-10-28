<%*
	let dt = tp.date.now("YYYY-MM-DD HH:mm:ss")
	let df = tp.date.now("D MMM YYYY")
	let head = " | Adge Denkers"

%>###### <% df %><% head %>

<% tp.file.cursor() %>