---
judul: Membuat aplikasi
---

Tutorial ini dirancang agar Kamu terbiasa dengan proses penulisan komponen. Tetapi pada titik tertentu, Kamu ingin mulai menulis komponen dalam kenyamanan editor teks Anda sendiri.

Pertama, Kamu harus mengintegrasikan Svelte dengan alat pembuat. Ada plugin resmi yang dikelola untuk [Rollup] (https://rollupjs.org) dan [webpack] (https://webpack.js.org/) ...

* [rollup-plugin-svelte](https://github.com/sveltejs/rollup-plugin-svelte)
* [svelte-loader](https://github.com/sveltejs/svelte-loader)

...dan berbagai [community-maintained ones](https://github.com/sveltejs/integrations#bundler-plugins).

Jangan khawatir jika Kamu relatif baru dalam pengembangan web dan belum pernah menggunakan alat ini sebelumnya. Kami telah menyiapkan panduan langkah demi langkah sederhana, [Svelte untuk pengembang baru (blog / svelte-untuk-pengembang-baru), yang memandu Kamu melalui proses tersebut.

Kamu juga ingin mengkonfigurasi editor teks Kamu untuk memperlakukan file `.svelte` sama dengan` .html` demi penyorotan sintaks. [Baca panduan ini untuk mempelajari caranya](blog / pengaturan-editor-Anda).

Kemudian, setelah Kamu menyiapkan proyek, menggunakan komponen Svelte itu mudah. Kompilator mengubah setiap komponen menjadi kelas JavaScript biasa - cukup impor dan buat instance dengan `baru`:

```js
import App from './App.svelte';

const app = new App({
	target: document.body,
	props: {
		// we'll learn about props later
		answer: 42
	}
});
```

Kamu kemudian dapat berinteraksi dengan `app` menggunakan [API komponen] (dokumen#Client-side_component_API) jika perlu.
