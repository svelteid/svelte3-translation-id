---
title: Penerusan event
---

Tidak seperti event DOM, event komponen tidak *bubble*. Jika kamu ingin *listen* ke sebuah event dalam komponen yang bersarang sangat dalam, komponen perantara harus *meneruskan* event tersebut.

Dalam hal ini, kita mempunyai `App.svelte` dan `Inner.svelte` yang sama dengan [bab sebelumnya](tutorial/component-events), tapi sekarang ada `Outer.svelte` komponen yang berisi `<Inner/>`.

Salah satu cara untuk menyelesaikan masalah ini adalah dengan menambahkan `createEventDispatcher` ke `Outer.svelte`, mendengarkan event `message`, dan membuat *handler* untuk itu:

```html
<script>
	import Inner from './Inner.svelte';
	import { createEventDispatcher } from 'svelte';

	const dispatch = createEventDispatcher();

	function forward(event) {
		dispatch('message', event.detail);
	}
</script>

<Inner on:message={forward}/>
```

Tapi banyak kode yang harus ditulis, jadi Svelte memberikan kita sebuah steno(penulisan cepat) - dengan event direktif `on:message` tanpa sebuah nilai berarti 'meneruskan semua event `message`'.

```html
<script>
	import Inner from './Inner.svelte';
</script>

<Inner on:message/>
```
