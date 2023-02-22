---
date created: Saturday, February 11th 2023, 2:21:17 pm
date modified: Monday, February 13th 2023, 3:19:43 pm
title: Entry Point
cssClass: wide-page
banner: "https://mir-s3-cdn-cf.behance.net/project_modules/fs/7e3d5e81488145.5d050548d72a7.jpg"
banner_x: 0.5
banner_y: 0.34
banner_lock: true
---

# 001


> [!multi-column]
>
>> [!tip] Work  
>> - [[Company Page]]
>> - [[Index| Meetings]]
>> ```button
>> name Add meeting
>> type link
>> action shortcuts://run-shortcut?name=Create Meeting Minutes
>> ```
>
>> [!Info] Personal  
>> - [[Info]]
>> - [[Films]]
>> - [[Books]]
>> - [[Projects]]
>

---

> [!multi-column]
>> [!blank-container]
>> ## Backlog 🚧
>> ```dataview
>>  TABLE WITHOUT ID link(file.link, title) AS "File",
>>    bar AS "Status" FROM #todo OR #backlog AND !#dailynote AND -"templates" SORT file.ctime LIMIT 10
>> ```
>
>> [!blank-container]
>> ## Recently Created 🐣
>> ```dataview
>>  TABLE WITHOUT ID link(file.link, title) as "File", length(file.inlinks) AS "Mentions"
>>  FROM "" SORT file.ctime DESC LIMIT 10
>> ```
>
>> [!blank-container]
>> ## Review ⬅️
>> ```dataview
>>  TABLE WITHOUT ID link(file.link, title) AS "File", sr-due as "Due" FROM #review WHERE sr-due <= date(today) SORT sr-due LIMIT 10
>> ```
