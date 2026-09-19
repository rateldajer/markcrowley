# Files Recently

## Edited Today

```dataview 
TABLE 
	choice(Description,"`Desc:` " + Description + " ","") + choice(Question,"`Q:` " + Question + " ","") + choice(Next,"`Next:` " + Next + " ", "") as Info,
	dateformat(file.mtime, "cccc  yyyy-dd-MM (t)") AS "Modified"
FROM "" 
WHERE file.name != this.file.name 
WHERE date(now) - file.mtime <= (date(now) - date(today))
SORT file.mtime DESC 
LIMIT 100
```

 
## Fixing Duplicates
 > I fixed the problem by updating the query to the below syntax:
>
> `TABLE WITHOUT ID rows.FlattenedNames[0] As "Names", rows.marriageDate[0] As "Marriage Date", rows.AnniversaryCalc[0] AS "Anniversary" FROM #person WHERE marriageDate.month = 03 AND marriageDate.day = 11 FLATTEN join(sort(list(row.file.link,partneredWith)), ", ") AS "FlattenedNames" FLATTEN truncate(string(date(today) - marriageDate),2, "") AS "AnniversaryCalc" GROUP BY FlattenedNames`
>
> This now correctly only displays one anniversary per couple.

## Files Modified Between *1* and *14* days ago
```dataview 
TABLE 
	choice(Question,"==Q:== " + Question + " ","") + choice(Next,"==Next:== " + Next + " ", "") as tags,
	dateformat(file.mtime, "ccc MMM d") AS "Modified"
FROM "" 
WHERE file.name != this.file.name 
WHERE (this.file.mtime - file.mtime) >= this.file.mtime - today
WHERE (this.file.mtime - file.mtime) <= dur(14 days)
SORT file.mtime DESC 
```


---

**