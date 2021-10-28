<%*
const fileName = await tp.system.prompt("File name")
const templateName = await tp.system.suggester(["Create New Task", "Create New Call Note"], ["adge-task", "call-note"])
tp.file.create_new(tp.file.find_tfile(templateName), fileName, "task-notes")
%>
