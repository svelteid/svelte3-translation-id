---
title: Nilai default
---

Kita dapat dengan mudah menspesifikasikan nilai default pada properti:

```html
<script>
	export let answer = 'a mystery';
</script>
```

Jika kita menambahkan komponen lain *tanpa* sebuah `answer` properti, nilainya akan menggunakan nilai default:

```html
<Nested answer={42}/>
<Nested/>
```
