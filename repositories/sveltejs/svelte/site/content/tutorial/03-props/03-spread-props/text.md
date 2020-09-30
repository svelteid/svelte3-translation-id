---
title: Properti tersebar
---

Jika kamu punya sebuah objek properti, kamu bisa 'menyebarkan' nya ke dalam sebuah komponen dibanding harus mendeklarasikannya satu per satu: 

```html
<Info {...pkg}/>
```

> Sebaliknya, jika kamu perlu merefrensikan semua properti yang diteruskan ke dalam sebuah komponen, termasuk yang tidak dideklarasikan dengan `export`, kamu bisa melakukannya dengan mengakses `$$props` secara langsung. Ini tidaklah direkomendasikan, karena akan sulit bagi Svelte untuk mengoptimasikannya, tapi ini berguna untuk kasus yang langka.
