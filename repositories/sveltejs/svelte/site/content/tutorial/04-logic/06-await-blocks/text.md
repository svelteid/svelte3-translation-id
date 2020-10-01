---
title: Blok await
---

Kebanyakan aplikasi web harus berurusan dengan `asynchronous` data secara bersamaan. Svelte mempermudah untuk melakukan *await* nilai dari sebuah [*promise*](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Guide/Using_promises) secara langsung di markupmu:

```html
{#await promise}
	<p>...waiting</p>
{:then number}
	<p>The number is {number}</p>
{:catch error}
	<p style="color: red">{error.message}</p>
{/await}
```

> Hanya `promise` terbaru yang dipertimbangkan, artinya kamu tidak perlu khawatir dengan *race conditions*.

Jika kamu tau *promise* mu tidak bisa di *reject*, kamu bisa menghilangan blok `catch`. Kamu juga bisa menghilangan blok pertama jika kamu tidak ingin menampilkan apapun sampai *promise* nya terselesaikan:

```html
{#await promise then value}
	<p>the value is {value}</p>
{/await}
```
