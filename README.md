DESKRIPSI:
Repository PR 16 Modul 18 ini adalah membuat tugas khusus Gradle dan add libraries

PERINTAH / TUGAS :
Kriteria:
- buat tugas Gradle sederhana untuk menerima parameter CLI dan mencetaknya dengan pesan ucapan
- Proyek skrip Gradle harus dibuat di repositori yang berbeda dan dorong ke GitHub
Berikut adalah langkah-langkah untuk membuat tugas khusus Gradle dan menambahkan pustaka:

Buat proyek Gradle baru dengan menjalankan perintah "gradle init --type java-library". Ini akan membuat proyek Gradle baru dengan struktur direktori dan file build.gradle awal.

Buka file build.gradle di direktori root proyek dan tambahkan kode berikut untuk menentukan tugas khusus:

task greetingTask() {
    doLast {
        String nama = project.hasProperty('nama') ? project.property('nama') : 'Gradle User'
        println "Hello, $nama! Welcome to Gradle World!"
    }
}

CARA MENJALANKAN:
"./gradlew greetingTask -Pname=YourName"

