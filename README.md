<div align="center">

# NETFLIX-APP-SENTIMEN

*Transform Feedback into Actionable Viewer Insights*

[![Last Commit](https://img.shields.io/github/last-commit/richalfajril/netflix-app-sentimen)](https://github.com/richalfajril/netflix-app-sentimen/commits/main)
![Jupyter Notebook](https://img.shields.io/badge/jupyter%20notebook-100.0%25-orange)
![Languages](https://img.shields.io/github/languages/count/richalfajril/netflix-app-sentimen)

Built with the tools and technologies:

![Markdown](https://img.shields.io/badge/Markdown-000000?style=for-the-badge&logo=markdown&logoColor=white)

</div>

---

## Table of Contents

* [Overview](#overview)
* [Getting Started](#getting-started)
    * [Prerequisites](#prerequisites)
    * [Installation](#installation)
    * [Usage](#usage)
    * [Testing](#testing)
* [Struktur Proyek](#struktur-proyek)
* [Lisensi](#lisensi)
* [Kontribusi](#kontribusi)

---

## Overview

Proyek ini bertujuan untuk menganalisis sentimen (positif, negatif, netral) dari ulasan pengguna aplikasi Netflix. Analisis ini dilakukan dengan menggunakan teknik pemrosesan bahasa alami (NLP) pada data ulasan yang dikumpulkan. Output dari proyek ini dapat berupa wawasan mengenai opini publik terhadap aplikasi Netflix, yang dapat digunakan untuk memahami persepsi pengguna dan mengidentifikasi area peningkatan.

## Getting Started

Untuk memulai dan menjalankan proyek ini di mesin lokal Anda, ikuti petunjuk di bawah ini.

### Prerequisites

Untuk menjalankan proyek ini, Anda memerlukan lingkungan Python dengan pustaka-pustaka yang tercantum dalam `requirments.txt`.

Pastikan Anda memiliki:
* **Python 3.x**: Unduh dari [python.org](https://www.python.org/).
* **Git**: Untuk mengkloning repositori. Unduh dari [git-scm.com](https://git-scm.com/downloads).
* **Jupyter Notebook**: Biasanya terinstal bersama Anaconda atau dapat diinstal via pip.

### Installation

1.  **Kloning repositori:**
    Buka terminal atau command prompt Anda dan jalankan perintah berikut untuk mengkloning repositori ini ke mesin lokal Anda:
    ```bash
    git clone [https://github.com/richalfajril/netflix-app-sentimen.git](https://github.com/richalfajril/netflix-app-sentimen.git)
    cd netflix-app-sentimen
    ```

2.  **Buat dan aktifkan lingkungan virtual (opsional, tapi sangat disarankan):**
    Lingkungan virtual membantu mengelola dependensi proyek secara terisolasi.
    ```bash
    python -m venv venv
    ```
    * **Di Windows:**
        ```bash
        venv\Scripts\activate
        ```
    * **Di macOS/Linux:**
        ```bash
        source venv/bin/activate
        ```

3.  **Instal dependensi:**
    Dengan lingkungan virtual aktif, instal semua pustaka Python yang diperlukan dari `requirments.txt`:
    ```bash
    pip install -r requirments.txt
    ```

### Usage

Setelah instalasi selesai, Anda dapat menjalankan analisis sentimen dengan mengikuti langkah-langkah di bawah ini:

1.  **Pengambilan Data (Scraping):**
    Buka dan jalankan notebook `netflix_scraping_data.ipynb`. Notebook ini berisi kode untuk mengumpulkan (scraping) data ulasan aplikasi Netflix dari sumber yang relevan (misalnya, Google Play Store, App Store, atau sumber data lainnya). Notebook ini diharapkan akan menghasilkan berkas `ulasan_netflix.csv` yang berisi data ulasan mentah.
    ```bash
    jupyter notebook netflix_scraping_data.ipynb
    ```

2.  **Analisis Sentimen:**
    Setelah data ulasan terkumpul, buka dan jalankan notebook `netflix_sentimen_analysis.ipynb`. Notebook ini akan melakukan langkah-langkah berikut:
    * Memuat data ulasan dari `ulasan_netflix.csv`.
    * Melakukan pra-pemrosesan teks (seperti tokenisasi, penghapusan stop-words, stemming/lemmatisasi).
    * Menerapkan model analisis sentimen (misalnya, VADER, TextBlob, atau model kustom) untuk mengklasifikasikan sentimen setiap ulasan (positif, negatif, netral).
    * Menyajikan hasil analisis, yang mungkin termasuk visualisasi data (grafik distribusi sentimen, kata-kata kunci) atau ringkasan statistik.
    ```bash
    jupyter notebook netflix_sentimen_analysis.ipynb
    ```

## Struktur Proyek

Repositori ini diorganisir sebagai berikut:

* `README.md`: Berkas dokumentasi utama yang sedang Anda baca ini, menjelaskan proyek secara keseluruhan.
* `netflix_scraping_data.ipynb`: Notebook Jupyter yang didedikasikan untuk proses pengambilan data ulasan.
* `netflix_sentimen_analysis.ipynb`: Notebook Jupyter inti yang berisi logika untuk analisis sentimen, mulai dari pra-pemrosesan hingga klasifikasi dan presentasi hasil.
* `requirments.txt`: Berkas teks yang mencantumkan semua pustaka Python dan versi spesifik yang diperlukan untuk menjalankan kedua notebook di atas.
* `ulasan_netflix.csv`: Berkas data dalam format CSV yang akan menyimpan atau sudah menyimpan ulasan aplikasi Netflix yang digunakan sebagai input untuk analisis sentimen.
