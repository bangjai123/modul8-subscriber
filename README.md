# Reflection
## Understanding subscriber and message broker.

1. 1. **amqp** adalah singkatan dari _Advanced Message Queuing Protocol_. Protokol tersebut merupakan protokol terbuka yang digunakan untuk melakukan komunikasi secara asinkron. Protokol dirancang untuk dapat memastikan komunikasi asinkron antar aplikasi atau komponen aplikasi berjalan dengan aman. Protokol ini dapat berjalan di berbagai platform dan bahasa pemrograman
2. 2. Guest pertama merupakan default yang sering digunakan untuk nama pengguna untuk melakukan autentikasi ke server AMQP. Guest kedua adalah password default yang sering digunakan dari nama pengguna yang telah disebutkan sebelumnya. localhost:5672 adalah kombinasi dari **hostname** (karena localhost berarti pada mesin lokal) dan 5672 yang merupakan **port** di mana AMQP server mendengarkan koneksi. Dengan demikian, link ini berarti bahwa siste akan melakukan koneksi ke server AMQP pada mesin lokal menggunakan port 5672 menggunakan pengguna `guest` dengan kata sandi `guest`