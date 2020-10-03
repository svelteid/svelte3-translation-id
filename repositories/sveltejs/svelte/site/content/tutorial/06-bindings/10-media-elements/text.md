---
title: Elemen media
---

Element `<audio>` dan `<video>` memiliki beberapa properti yang bisa kamu *bind* juga. Contoh berikut mendemonstrasikan beberapa properti itu.

Pada baris 116, tambahkan *bindings* `currentTime={time}`, `duration` dan `paused`:

```html
<video
	poster="https://sveltejs.github.io/assets/caminandes-llamigos.jpg"
	src="https://sveltejs.github.io/assets/caminandes-llamigos.mp4"
	on:mousemove={handleMousemove}
	on:mousedown={handleMousedown}
	bind:currentTime={time}
	bind:duration
	bind:paused
></video>
```

> `bind:duration` itu sama dengan `bind:duration={duration}`

Sekarang, saat kamu melakukan klik pada video, itu akan memperbarui `time`, `duration` dan `pauseda` sewajarnya. Ini berarti kita bisa menggunakannya untuk membangun kontrol khusus.

> Pada web umunya, kamu akan melacak `currentTime` dengan cara me*listening* event `timeupdate`. Tapi event itu terlalu jarang terjadi, menghasilkan UI yang kurang halus. Svelte melaukannya lebih baik - dengan memeriksa `currentTime` menggunakan `requestAnimationFrame`.

The complete set of bindings for `<audio>` and `<video>` is as follows — six *readonly* bindings...
*Binding* lengkap untuk `<audio>` dan `<video>` adalah sebagai berikut - enam *binding readonly*(hanya bisa dibaca)...

* `duration` (readonly) — total durasi dari video, dalam detik
* `buffered` (readonly) — sebuah *array* dari objek `{start, end}`
* `seekable` (readonly) — ditto
* `played` (readonly) — ditto
* `seeking` (readonly) — boolean
* `ended` (readonly) — boolean

...dan empat *binding* *dua-arah*:

* `currentTime` — titik saat ini dalam video, dalam detik
* `playbackRate` — seberapa cepat video dimainkan, dimana `1` adalah 'normal'
* `paused` — yang satu ini harusnya kamu sendiri sudah tau
* `volume` — volume antara 0 dan 1

Video memliliki *readonly* `videoWidth` dan `videoHeight` sebagai *bindings* tambahan.
