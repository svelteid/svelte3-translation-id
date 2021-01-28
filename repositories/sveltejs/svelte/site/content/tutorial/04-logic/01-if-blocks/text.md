---
title: Blok if
---

HTML tidak mempunyai cara untuk mengekspresikan *logika*, seperti kondisi dan perulangan. Svelte punya.

Untuk mengkondisikan *render* markup, kita membungkusnya dengan `if` blok:

```html
{#if user.loggedIn}
	<button on:click={toggle}>
		Log out
	</button>
{/if}

{#if !user.loggedIn}
	<button on:click={toggle}>
		Log in
	</button>
{/if}
```

Cobalah - perbarui komponen, dan klik tombolnya.
