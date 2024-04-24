# Reflection
## Understanding subscriber and message broker.

1. **amqp** adalah singkatan dari _Advanced Message Queuing Protocol_. Protokol tersebut merupakan protokol terbuka yang digunakan untuk melakukan komunikasi secara asinkron. Protokol dirancang untuk dapat memastikan komunikasi asinkron antar aplikasi atau komponen aplikasi berjalan dengan aman. Protokol ini dapat berjalan di berbagai platform dan bahasa pemrograman
2. Guest pertama merupakan default yang sering digunakan untuk nama pengguna untuk melakukan autentikasi ke server AMQP. Guest kedua adalah password default yang sering digunakan dari nama pengguna yang telah disebutkan sebelumnya. localhost:5672 adalah kombinasi dari **hostname** (karena localhost berarti pada mesin lokal) dan 5672 yang merupakan **port** di mana AMQP server mendengarkan koneksi. Dengan demikian, link ini berarti bahwa siste akan melakukan koneksi ke server AMQP pada mesin lokal menggunakan port 5672 menggunakan pengguna `guest` dengan kata sandi `guest`

## Simulation slow subscriber
![image](https://github.com/bangjai123/modul8-subscriber/assets/120235144/39a45623-43e5-4810-a568-f476fbf76cd1)

Gambar di atas adalah interface RabbitMQ saat saya melakukan cargo run dua kali pada publisher. Dari gambar tersebut dapat dilihat bahwa queue yg dibuat adalah 6. Hal ini dapat terjadi karena adanya sleep pada subscriber yang menyebabkan message masuk lebih lambar dan harus menunggu dahulu.

## Reflection and Running at least three subscribers
![image](https://github.com/bangjai123/modul8-subscriber/assets/120235144/0f92c3fb-94ba-4cea-baba-b9cc54b64be0)
![image](https://github.com/bangjai123/modul8-subscriber/assets/120235144/6112b0d8-0686-488e-98e3-5f610d979e60)

Pada gambar di atas, saya menggunakan tiga _subsciber_ dan 6 _pubisher_. Dibandingkan gambar sebelumnya, di mana hanya ada 1 subscriber, kita dapat lihat bahwa tiga _subscriber_ membuat _message queue_ tidak setinggi dengan satu _subscriber_. Hal ini dapat terjadi karena proses dari _publisher_ saat ini ditangani oleh beberapa _subscriber_. Dengan demikian, _publisher_ dapat mengirimkan lebih banyak data secara lebih cepat pada tiga _subscriber_ satu _subscriber_. 
