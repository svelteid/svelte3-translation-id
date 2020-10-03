---
title: Binding contenteditable 
---

Elemen dengan atribut `contenteditable="true"` mendukung `textContent` and `innerHTML` *bindings*:

```html
<div
	contenteditable="true"
	bind:innerHTML={html}
></div>
```
