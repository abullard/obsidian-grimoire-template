### [[Table of Contents|← Parent]]

```dataviewjs
let items = dv.pages('')
let count = items.length
let tags = [] 

for (let tag of items.file.tags) { 
	if (tags.indexOf(tag) == -1) { 
	tags.push(tag)
	}
}

dv.paragraph(`Total items: ${count}`)

dv.list(tags) 
```
