---
judul: Pernyataan
---

Kami tidak membatasi pada pendeklarasian *nilai* reaktif - kami juga dapat menjalankan *pernyataan* secara sewenang-wenang. Misalnya, kita dapat mencatat nilai `count` setiap kali berubah:

```js
$: console.log(`the count is ${count}`);
```

kamu dapat dengan mudah mengelompokkan pernyataan bersama dengan satu blok:

```js
$: {
	console.log(`the count is ${count}`);
	alert(`I SAID THE COUNT IS ${count}`);
}
```

Kamu bahkan dapat meletakkan `$:` di depan hal-hal seperti blok `if`:

```js
$: if (count >= 10) {
	alert(`count is dangerously high!`);
	count = 9;
}
```