---
title: Event komponen
---

Komponen juga bisa mengirim event. Untuk melakukannya, mereka harus membuat sebuah pengirim event. Perbarui `Inner.svelte`:

```html
<script>
	import { createEventDispatcher } from 'svelte';

	const dispatch = createEventDispatcher();

	function sayHello() {
		dispatch('message', {
			text: 'Hello!'
		});
	}
</script>
```

> `createEventDispatcher` harus dipanggil saat komponen pertama kali dibuat - kamu tidak bisa melakukannya nanti contoh: dengan *callback* `setTimeout`. Ini akan menghubungkan `dispatch` ke instance komponen.
