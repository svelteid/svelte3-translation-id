---
title: Penerusan event DOM
---

Penerusan event juga bisa digunakan untuk event DOM.

Kita ingin diberitahu tentang event klik dalam `<CustomButton>` kita - untuk melakukan itu, kita hanya perlu meneruskan event `click` ke dalam elemen `<button>` dalam `CustomButton.svelte`:

```html
<button on:click>
	Click me
</button>
```
