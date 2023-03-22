
<%*
  let title = tp.file.title
  if (title.startsWith("Untitled")) {
    title = await tp.system.prompt("Title");
    await tp.file.rename(title);
  } 
  tR += "---"
%>
title:  <%* tR += title %>
created: <% tp.date.now("YYYY-MM-DD") %>
---

>[!info]- Note info
>created: <% tp.file.creation_date("YYYY-MM-DD") %>
>modified: <% tp.file.last_modified_date("YYYY-MM-DD") %>
>folder: <% tp.file.folder() %>

# <%* tR += title %>
