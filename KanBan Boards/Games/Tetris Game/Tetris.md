---

kanban-plugin: board

---

## Backlog

- [ ] ###### UI & Game Polish
	
	- [ ] Next Piece Queue & Hold Piece system
	- [ ] Ghost Piece Projection
	- [ ] Game Over & Main Menu
	- [ ] Add Pause / Unpause state
	- [ ] Maybe include some SFX & Audio Streams


## Todo

- [ ] ###### Piece Logic & Spawning
	
	- [ ] Tetromino Data & 7-Bag Generator
	- [ ] Piece Movement & Collision
	- [ ] Setup the Grid Renderer (TileMapLayer or Drawing)
	- [ ] Hard Drop (Instant) execution
	- [ ] Piece Rotation (SRS)
- [ ] ###### Game Loop & Animations
	
	- [ ] Gravity & Lock Delay (Also know by HitStop, Before locking the piece into the grid give it a brief time when it should still be able to move before locking it to grid)
	- [ ] Line Clears & Scoring
	- [ ] Tweens & Smooth Movement
	- [ ] Add Level-Based gravity speed scaling


## In Progress

- [ ] ###### Setup New Godot Project
	
	- [x] Create new project, setup it for C# use and setup the input map and other necessary project settings
	- [x] Create the assets that will be used in the game later
	- [ ] Setup the scene and folders structure
	
	![[Pasted image 20260813220821.png]]
- [ ] [[Some Tetris Task to Complete]]
	
	#Setup


## Done

**Complete**




%% kanban:settings
```
{"kanban-plugin":"board","list-collapse":[false,false,false,false],"new-note-template":"Templates/KanBan Card Template.md","new-note-folder":"KanBan Boards/Games/Tetris Game/Card Notes","new-line-trigger":"shift-enter","show-relative-date":true,"metadata-keys":[{"metadataKey":"Created At","label":"","shouldHideLabel":false,"containsMarkdown":false},{"metadataKey":"Due Date","label":"","shouldHideLabel":false,"containsMarkdown":false}],"tag-sort":[{"tag":"#Setup"}],"tag-colors":[{"tagKey":"#Setup","color":"rgba(22, 37, 58, 1)","backgroundColor":"rgba(121, 244, 129, 1)"}]}
```
%%