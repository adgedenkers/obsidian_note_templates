<%*
	 let title = tp.file.title
	 let tags = '#call-note'

	const templateName = await tp.system.suggester(["Add Comment","Add Task","Add Something"], ["dated-note","add-task","add-something"])
%>