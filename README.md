# Run Commands View

```javascript
"run-commands-view.commands": {
	// Place commands here
}
```

## The easiest example (string):

```javascript
"💤 Toggle Status Bar": "workbench.action.toggleStatusbarVisibility",
```

## Specifying arguments (object):

```javascript
"🔶 Insert text": {
	"command": "editor.action.insertSnippet",
	"args": { "snippet": "text" }
},
```

## Running multiple commands in sequence (array of strings)

```javascript
"📒 Toggle Minimap & Status Bar": [
	"editor.action.toggleMinimap",
	"workbench.action.toggleStatusbarVisibility"
],
```

## Specifying the delay

```javascript
"⏳ Delay": [
	"workbench.action.toggleSidebarVisibility",
	{
		"command": "workbench.action.toggleSidebarVisibility",
		"delayBefore": 1000,
	}
],
```

## Register command to invoke it with a keybinding

```javascript
"📜 Toggle sidebar and minimap": {
	"registerId": "toggleSidebarMinimap",
	"sequence": [
		"workbench.action.toggleSidebarVisibility",
		"editor.action.toggleMinimap"
	]
}
```

# Additional commands

## Open Folder

```javascript
"📁 Open Folder": {
	"command": "vscode.openFolder",
	"args": "C:\\Users"
},
```

## Open File

```javascript
"📝 Open File": {
	"command": "vscode.openFolder",
	"args": "C:\\inbox.md"
},
```

## Toggle Settings

```javascript
"🔢 Toggle Line Numbers": {
	"command": "run-commands-view.toggleSetting",
	"args": {
		"setting": "editor.lineNumbers",
		"value": "on,off"
	}
},
```

## TODO

- [x] Run multiple commands
- [x] Delay
- [x] Register command to invoke it with a keybinding
- [ ] Register command without showing it in the tree view
- [ ] Hierarchy (group commands by folders)
- [ ] Create a command to bookmark current file
- [x] Create a minimalistic command to toggle global settings (strings, bool, number)
