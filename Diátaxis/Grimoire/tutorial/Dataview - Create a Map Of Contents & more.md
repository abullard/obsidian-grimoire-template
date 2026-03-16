#diataxis/grimoire/tutorial #dataview
### [[MoC - Grimoire|← Parent]]

> [!Tip] Dynamic Notes
> Use the Dataview plugin to reflect over metadata in your vault, and build dynamic views within your notes. This is the engine behind the [[What is a Map of Contents?|Map of Contents]].
> 
> 📖  For more information, read the "Dataview" plugin's [documentation](https://blacksmithgu.github.io/obsidian-dataview/)
## Build a Map of Contents (MoC)
### Create an Inbox
1. Create a new note, named `MoC - Animals`
2. Fill it with this *Dataview* markdown syntax:
![[map-of-contents-dataview-query.png]]

> [!example] Syntax Explained
> ```
> SELECT file.link FROM ObsidianVault
> WHERE 
> otherFile contains backlink to thisFile 
> AND
> thisFile does NOT contain backlink to otherFile
> ```
> 

3. When you click off the component, it should render as:
![[empty-moc-inbox-dataview.png]]
4. Voila, an *inbox* 📫
### Add a Backlink to your Map of Contents
1. You're ready to put [[What is a Map of Contents?|backlinks]] into your notes, to populate this inbox
2. Create a new note, named `Bunny Rabbits`
3. Use this syntax: `[[MoC - Animals]]` (drop the backticks), to link from `Bunny Rabbits` to `Animals`
4. Now, when you go to `MoC - Animals`, you'll see:
![[moc-inbox-with-message-dataview.png]]
### Clear your Inbox Notifications
1. Your inbox has a *notification*!
2. You can clear it up, or leave it–but beware...

> [!Warning]  An Inbox is a dynamic list
> It's rendered through the Dataview plugin, if that connection breaks, your lists will disappear. 
> 
> *It's better to sort the data & hardcode it.*

3. If you choose to clear the notification:
	- Add a *backlink* to `Bunny Rabbit` in your `MoC - Animals`
	- Now, you'll see:
	![[moc-inbox-cleared-dataview.png]]
4. If you choose to leave the notification, you're done!

> [!Success] Done!
> Nice! You built your first MoC! 
> 
> Have fun building non-linear, topological notes!

---
## Dataview with Javascript
*Dataview* supports JavaScript queries, see [[ALL TAGS]], and expand the query:
![[view-source-btn-dataview.png]]
![[viewing-source-dataview.png]]
I'm going to leave comprehension of this as an exercise for the reader. 
Read the [docs](https://blacksmithgu.github.io/obsidian-dataview/queries/dql-js-inline/#dataview-js) if you want to know more.

---
## Conclusion
There's so much to talk about with Dataview, that I'm going to wrap up here. 
Other things Dataview can handle: 
- You can filter for [[Create & Operate Tags|tags]] across files in your vault
- Automatically collect links to books in your notes, and render them all sorted by rating.
- Surface a dynamic list of the last month's worth of meeting notes
- and on & on
Enjoy the power of reflection over your Grimoire!