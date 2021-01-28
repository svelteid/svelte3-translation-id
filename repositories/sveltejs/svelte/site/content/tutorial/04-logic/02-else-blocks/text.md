---
title: Blok else
---

Adanya dua kondisi - `if user.loggedIn` dan `if !user.loggedIn` - dimana itu eksklusif, kita bisa menyederhanakan komponen dengan menggunakan `else` blok:

```html
{#if user.loggedIn}
	<button on:click={toggle}>
		Log out
	</button>
{:else}
	<button on:click={toggle}>
		Log in
	</button>
{/if}
```

> Karakter `#` selalu menunjukkan sebuah tag *pembukaan blok*. Karakter `/` selalu menunjukan sebuah tag *penutup blok*. Karakter `:`, dalam `{:else}`, menunjukkan sebuah tag *lanjutan blok*. Jangan khawatir - kamu sudah mempelajari hampir semua sintak yang Svelte tambahkan ke HTML.
