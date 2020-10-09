# **D**ark **Oran**ge Theme for **VS**Code
## Description
Dark orange based theme which colors were chosen to my liking.

* A colorful Dark Theme, inspired by other themes such as [FireFly](https://github.com/ankitmlive/firefly-theme), [Molokai](https://github.com/nonylene/vscode-dark-molokai-theme), [VSCode Dark Theme](https://github.com/Microsoft/vscode).
* The colors were *accurately picked* from a random color generator.
	*	![#FF9507](https://via.placeholder.com/15/FF9507/000000?text=+) `#FF9507` 
	*	![#179AFF](https://via.placeholder.com/15/179AFF/000000?text=+) `#179AFF`
* This was _not_ supposed to be a halloween-inspired theme. _spooky_.
	* No pumpkins were harmed in the making of this theme!


## Recommended settings
I have nothing to recommend in particular, it is just a theme... or is it?

I'd just suggest to use at least a monospaced character font, such as [FiraCode](https://github.com/tonsky/FiraCode) if you like ligatures or [Mononoki](https://github.com/madmalik/mononoki) if you do not.

```json
// pick your favorite
"editor.fontFamily" : "chosen#font",
"editor.fontLigatures": true/false,
```

## My settings

### **UI Scale**
I do not like `Activity Bar` icon sizes, in fact I wish there was a simpler way to scale them down rather than *scaling the whole editor UI down*.
```
// Original size is 0
// Go negative for downscaling
// Go positive for upscaling

"window.zoomLevel": -0.75,
```

### **Font**
I tend to prefer a smaller font-size with just _barely_ line-height.
(font-size also depends on the scale of the editor)
```json

"editor.fontSize": 16,
"editor.lineHeight": 15,
"editor.fontWeight": "normal",
"editor.letterSpacing": 0,
```

Every action has its consequences, if you are going to grab my settings, expect some _minor inconvenience_: the gutter size is not big enough to display both the code folding symbol and the git decorations.

### **Fixing decorations in the gutter**
Willing to update this section if somehow _they_ will let custom-sized glyphs to be a thing. 
```json
// Either
// a. disable codeFolding decorations
"editor.folding": false,

// b. disable git decorations
"scm.diffDecorations": "none"

// c. workaround-ish, set the width for git decorations 
// and let it display only on hover
"scm.diffDecorationsGutterWidth": 1,
"scm.diffDecorationsGutterVisibility": "hover",
```

### **Tabulation and Rulers**
I use tabs `⇆` for indentation with a small tabulator, typically 2 or 4.
```json
"editor.detectIndentation": false,
"editor.insertSpaces": false,
"editor.useTabStops": true,
"editor.tabSize": 2,
``` 

I kind of like the look that `"editor.rulers": [0]` gives, so give it a go!

### **Extension: Activitus Bar**
I also complete the interface of VSCode by having [Activitus Bar](https://github.com/Gruntfuggly/activitusbar) extension which adds configurable commands in the status bar. Colors of the items `codicons` are customizable. I'd suggest different, bright colors such as:

* ![#FF004D](https://via.placeholder.com/15/FF004D/000000?text=+) `#FF004D` _active_\
  ![#C2003B](https://via.placeholder.com/15/C2003B/000000?text=+) `#C2003B` _inactive_

* ![#00F5CC](https://via.placeholder.com/15/00F5CC/000000?text=+) `#00F5CC` _active_\
	![#00B295](https://via.placeholder.com/15/00B295/000000?text=+) `#00B295` _inactive_

```json
// To be inserted in the settings.json of VSCode
// Custom extension themes are not supported (yet).

"activitusbar.activeColour": "#color"
"activitusbar.inactiveColour": "#color",
```

### **Icons**
Finally, I prefer simple icons in the explorer, so I'd rather stick with `Minimal` or [Chalice Icon Theme](https://github.com/artlaman/chalice-icon-theme).

## Feedback
If you find any issue with my theme, or you feel like something should be added, let me know on [github issue](https://github.com/DrKGD/darkorange-theme-vscode/issues). 

I'd suggest to be as specific as possible to *help me help you*: `Developer: Inspect Editor Tokens and Scopes` is a good start, for example. 



## Contribution
If you like this theme, you can clone the repository.

```
git clone https://github.com/drkgd/dorange
```

## Customization
*Of course* you are also allowed to customize the entire theme or to build one based off mine by yourself, that is what the license says. If you want a *fast hack*, `settings.json` is here to help.

UI:
```json
"workbench.colorCustomizations": {
	"[dorange]": {
		"editorLineNumber.activeForeground: "#FF004D"
		// ...
	}
}
```

Tokens:
```json
"editor.tokenColorCustomizations": {
	"textMateRules": [
		{
			"scope":"comment",
			"settings": { "foreground": "#CD2277", "fontStyle": "italic" }
		},
		// ...
	]
}
```

## Author
Theme created by -- Ciro Amato @DrKGD\
Repository @ [darkorange-theme-vscode](https://github/DrKGD/darkorange-theme-vscode)
