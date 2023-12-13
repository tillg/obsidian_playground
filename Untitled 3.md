
---
creation date: 2022-03-31 17:40 
modification date: Thursday 31st March 2022 17:40:26
dateCreated: 2022-03-31T17:40

---

<% let title = tp.file.title;
	if (title.startsWith("Untitled")) 
		{ 
		title = await tp.system.prompt("Title"); 
		await tp.file.rename(`${title}`)  }  %>