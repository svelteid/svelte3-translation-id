---
title: Mengunci blok each
---

Secara default, saat kamu mengubah value dari blok `each`, itu akan menambah dan menghapus item di *akhir* blok, dan memperbarui nilai apapun yg berubah. Itu mungkin bukan apa yang kamu inginkan.

Ini akan lebih mudah untuk ditunjukkan ketimbang dijelaskan. Klik tombol 'Remove first thing' beberapa kali, dan perhatikan itu menghapus komponen `<Thing>` dari bawah dan memperbarui `warna` dari sisanya. Sedangkan, kita ingin menghapus komponen `<Thing>` pertama dan membiarkan sisanya tidak terdampak.

Untuk melakukan itu, kita spesifikasikan sebuah identitas unik untuk blok `each`:

```html
{#each things as thing (thing.id)}
	<Thing current={thing.color}/>
{/each}
```

`(thing.id)` memberi tau Svelte bagaimana mencari apa yang berubah.

> Kamu bisa mengunakan objek sebagai sebuah kunci, karena Svelte menggunakan `Map` secara internal - dengan kata lain kamu bisa menggunakan `(thing)` dari pada `(thing.id)`. Mengunakan sebuah string atau angka lebih aman, namun, karena itu merupakan sebuah identitas yang bertahan tanpa persamaan referensial, misalnya saat kita memperbarui dengan data baru dari API *server*.
