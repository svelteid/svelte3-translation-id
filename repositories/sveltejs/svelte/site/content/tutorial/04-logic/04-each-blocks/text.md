---
title: Blok each
---

Jika kamu perlu melakukan perulangan dari sebuah *list* data, gunakanlah `each` blok:

```html
<ul>
	{#each cats as cat}
		<li><a target="_blank" href="https://www.youtube.com/watch?v={cat.id}">
			{cat.name}
		</a></li>
	{/each}
</ul>
```

> Ekspresi (`cats`, dalam hal ini) bisa berbentuk sebuah *array* atau *array-like object* (i.e. memiliki properti `length`). Kamu bisa mengulang *generic iterable* dengan `each [...iterable]`.

You can get the current *index* as a second argument, like so:
Kamu bisa mendapatkan *index* saat ini sebagai argumen, seperti:

```html
{#each cats as cat, i}
	<li><a target="_blank" href="https://www.youtube.com/watch?v={cat.id}">
		{i + 1}: {cat.name}
	</a></li>
{/each}
```

Jika kamu lebih suka, kamu bisa menggunakan *destructuring* - `each cats as { id, name }` - dan mengganti `cat.id` dan `cat.name` dengan `id` dan `name` saja.
