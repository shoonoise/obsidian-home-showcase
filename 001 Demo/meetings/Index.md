## Meetings

```dataview
   TABLE WITHOUT ID link(file.link, title) AS "File",
   file.ctime AS "Date", length(filter(file.tasks, (r) => !r.completed)) AS ToDo FROM #mm
```
