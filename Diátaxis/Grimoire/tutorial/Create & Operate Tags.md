---
tags:
  - diataxis/grimoire/tutorial
  - tags
---
### [[MoC - Grimoire|← Parent]]

> [!Tip] Tag your files
> Use tags as metadata for the files in your vault. Use reflection to query your files for that metadata. 
> 
> You're building a grimoire of knowledge–cross-referencing topics will pay off in the future.
## Tag your files
1. It's super easy, #tag you're it.
	- That's an inline tag
2. OR, Supply them in a Frontmatter YAML header, as defined in the top of this page. Here's the syntax:
```YAML
# you can put a lot more properties here
---
tags:
  - diataxis/grimoire/tutorial
  - tags
---
```
3. This will render into an intractable component in Obsidian

---
## Build a Dataview List
0. Read up on [[Dataview - Create a Map Of Contents & more|Dataview]] if you haven't already
1. Insert this syntax anywhere in your files:
![[Pasted image 20260315225844.png]]
2. Click off this component and it'll render into a live list:
![[Pasted image 20260315225943.png]]

> [!Success] Title
> Nice! Another powerhouse of dataview demonstrated. 
> 
> Go modify the query in the `dataview` markdown block, and reflect on your notes!

---
## Wrangle your Tags with Tag Wrangler!

> [!Warning] Destructive Action
> This is a destructive action, so be cautious.

Imagine you have the tag #dawg, and you really want it to say #dog.

Tag Wrangler makes it easy:
1. Open the Tag Wrangler panel
2. Enter text to search for the offending tag
3. Right Click the offending tag & Select "Rename"
![[Pasted image 20260315230759.png]]
4. Enter a new tag and Confirm

---
## Search for Tags
1. Search everywhere for the tag you want to find
![[Pasted image 20260315230728.png]]
2. Skim the [[ALL TAGS]] file
3. Search from the Tag Wrangler panel

---
