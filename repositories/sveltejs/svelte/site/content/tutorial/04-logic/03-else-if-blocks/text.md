---
title: Blok else-if
---

Banyak kondisi dapat 'dirangkai' secara bersamaan dengan `else if`:

```html
{#if x > 10}
	<p>{x} is greater than 10</p>
{:else if 5 > x}
	<p>{x} is less than 5</p>
{:else}
	<p>{x} is between 5 and 10</p>
{/if}
```
