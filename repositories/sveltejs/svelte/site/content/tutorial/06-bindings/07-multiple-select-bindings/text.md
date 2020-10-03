---
title: Banyak pilihan
---

Pilihan bisa memiliki atribut `multiple`, dalam kasus ini akan membentuk sebuah *array* daripada memilih satu nilai.

Kembali ke [contoh es krim diawal](tutorial/group-inputs), kita bisa mengganti kotak centang dengan `<select multiple>`:

```html
<h2>Flavours</h2>

<select multiple bind:value={flavours}>
	{#each menu as flavour}
		<option value={flavour}>
			{flavour}
		</option>
	{/each}
</select>
```
