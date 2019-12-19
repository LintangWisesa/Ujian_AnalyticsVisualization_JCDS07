# Soal Ujian Data Science - Analytics & Visualization

![Lintang_Purwadhika](https://static.wixstatic.com/media/2e6af2_f69a4271c3534ae1869a7ed63e278b2b~mv2.png/v1/fill/w_246,h_39,al_c,usm_0.66_1.00_0.01/2e6af2_f69a4271c3534ae1869a7ed63e278b2b~mv2.png)

#

### **Soal 1 - 💃 Panggung Sandiwara**

MySQL secara default menyertakan database ```sakila``` yang dapat digunakan oleh user untuk mempelajari teknik penggunaan database di MySQL. Database ```sakila``` merupakan sample dummy database yang menyimpan informasi seputar toko rental DVD.

*__Soal :__* Aktifkan server MySQL Anda, lalu gunakan database ```sakila``` dan tuliskan langkah-langkah/query MySQL untuk menyelesaikan perintah berikut. Anda dilarang membuat database baru, merubah struktur table, membuat view atau segala bentuk tindakan yang mengubah struktur database.

1. Tampilkan daftar __10 film komedi dengan durasi tersingkat__. Urutkan data berdasarkan film dengan durasi terpendek. Kolom yang diwajibkan tampil adalah __title__, __category__ dan __length__. Output yang diharapkan:

    ```bash
    +------------------+----------+--------+
    | title            | category | length |
    +------------------+----------+--------+
    | DOWNHILL ENOUGH  | Comedy   |     47 |
    | HEAVEN FREEDOM   | Comedy   |     48 |
    | PARADISE SABRINA | Comedy   |     48 |
    | HURRICANE AFFAIR | Comedy   |     49 |
    | LION UNCUT       | Comedy   |     50 |
    | ZORRO ARK        | Comedy   |     50 |
    | CLOSER BANG      | Comedy   |     58 |
    | AIRPLANE SIERRA  | Comedy   |     62 |
    | LONELY ELEPHANT  | Comedy   |     67 |
    | DOOM DANCING     | Comedy   |     68 |
    +------------------+----------+--------+
    ```

2. Tampilkan daftar lengkap __kategori film beserta jumlah film tiap kategori & rata-rata harga sewa DVD film tiap kategori__. Urutkan data dari kategori dengan jumlah film terbanyak. Kolom yang diwajibkan ada minimal adalah __kategori__, __jumlah film__ dan __rata-rata harga sewa__. Output yang diharapkan:

    ```bash
    +-------------+-------------+---------------+
    | kategori    | jumlahMovie | rataHargaSewa |
    +-------------+-------------+---------------+
    | Foreign     |          73 |      3.099589 |
    | Sports      |          73 |      3.099589 |
    | Family      |          69 |      2.758116 |
    | Documentary |          68 |      2.666471 |
    | Animation   |          66 |      2.808182 |
    | Action      |          64 |      2.646250 |
    | New         |          63 |      3.116984 |
    | Drama       |          61 |      2.990000 |
    | Games       |          61 |      3.252295 |
    | Sci-Fi      |          61 |      3.219508 |
    | Children    |          60 |      2.890000 |
    | Comedy      |          58 |      3.162414 |
    | Classics    |          57 |      2.744386 |
    | Horror      |          56 |      3.025714 |
    | Travel      |          56 |      3.275714 |
    | Music       |          51 |      2.950784 |
    +-------------+-------------+---------------+
    ```

3. [Motion Picture Association of America](https://en.wikipedia.org/wiki/Motion_Picture_Association_of_America_film_rating_system) memiliki sistem rating untuk film berdasarkan konten & target penontonnya dengan klasifikasi sebagai berikut:

    - **G** : General Audiences
    - **PG** : Parental Guidance Suggested
    - **PG-13** : Parental Guidances for Children Under 13
    - **R** : Restricted
    - **NC-17** : No Children Under 17 Admitted

    Tampilkan daftar lengkap __rating film beserta keterangan arti rating & jumlah film tiap rating__. Kolom yang diwajibkan ada minimal adalah __rating__, __keterangan rating__ dan __jumlah film__. Output yang diharapkan:

    ```bash
    +--------+---------------------------------+--------------+
    | rating | keterangan                      | jumlahMovie  |
    +--------+---------------------------------+--------------+
    | G      | General Audiences               |          178 |
    | PG     | Parental Guidance Suggested     |          194 |
    | PG-13  | Parental Guidances for Under 13 |          223 |
    | R      | Restricted                      |          195 |
    | NC-17  | No Children Under 17 Admitted   |          210 |
    +--------+---------------------------------+--------------+
    ```

4. Tampilkan daftar __10 aktor/aktris yang paling banyak membintangi film__. Kolom yang ditampilkan minimal: __id aktor__, __nama depan__, __nama belakang__ dan __jumlah film yang dibintangi__ kemudian urutkan dari aktor/aktris yang membintangi film terbanyak. Output yang diharapkan:

    ```bash
    +----------+------------+-------------+--------------+
    | actor_id | first_name | last_name   | jumlah_Movie |
    +----------+------------+-------------+--------------+
    |      107 | GINA       | DEGENERES   |           42 |
    |      102 | WALTER     | TORN        |           41 |
    |      198 | MARY       | KEITEL      |           40 |
    |      181 | MATTHEW    | CARREY      |           39 |
    |       23 | SANDRA     | KILMER      |           37 |
    |       81 | SCARLETT   | DAMON       |           36 |
    |      158 | VIVIEN     | BASINGER    |           35 |
    |      144 | ANGELA     | WITHERSPOON |           35 |
    |      106 | GROUCHO    | DUNST       |           35 |
    |       60 | HENRY      | BERRY       |           35 |
    +----------+------------+-------------+--------------+
    ```

5. Dari soal sebelumnya diketahui ```Gina Degeneres``` merupakan aktris yang paling banyak membintangi film, dengan total **42** judul film. Kategori film apakah yang paling banyak dibintanginya? Untuk mengetahuinya, tampilkan daftar __kategori film beserta jumlah film yang pernah dibintangi oleh ```Gina Degeneres```__. Kolom yang diwajibkan ada yaitu __kategori film__ dan __jumlah film yang dibintangi__. Output yang diharapkan:

    ```bash
    +-------------+--------------+
    | category    | jumlah_Movie |
    +-------------+--------------+
    | Documentary |            3 |
    | Foreign     |            2 |
    | Music       |            4 |
    | New         |            1 |
    | Sci-Fi      |            7 |
    | Action      |            3 |
    | Drama       |            2 |
    | Animation   |            4 |
    | Horror      |            1 |
    | Family      |            4 |
    | Comedy      |            3 |
    | Children    |            2 |
    | Classics    |            2 |
    | Sports      |            2 |
    | Games       |            1 |
    | Travel      |            1 |
    +-------------+--------------+
    ```

6. Dari soal sebelumnya diketahui ```Gina Degeneres``` paling banyak membintangi film bergenre science-fiction, dengan total **7** judul film. Tampilkan daftar __judul film sci-fi yang pernah dibintangi oleh ```Gina Degeneres```__. Kolom yang diwajibkan ada yaitu __judul film__ dan __kategorinya__. Output yang diharapkan:

    ```bash
    +---------------------+----------+
    | title               | category |
    +---------------------+----------+
    | CHARIOTS CONSPIRACY | Sci-Fi   |
    | COLDBLOODED DARLING | Sci-Fi   |
    | FRISCO FORREST      | Sci-Fi   |
    | GOODFELLAS SALUTE   | Sci-Fi   |
    | LICENSE WEEKEND     | Sci-Fi   |
    | OPEN AFRICAN        | Sci-Fi   |
    | SPIRITED CASUALTIES | Sci-Fi   |
    +---------------------+----------+
    ```

7. Tampilkan daftar __10 aktor/aktris yang paling banyak membintangi film horror__. Kolom yang ditampilkan minimal: __id aktor__, __nama depan__, __nama belakang__ dan __jumlah film horror yang dibintangi__ kemudian urutkan dari aktor/aktris yang membintangi film horror terbanyak. Output yang diharapkan:

    ```bash
    +----------+------------+-----------+--------------+
    | actor_id | first_name | last_name | jumlah_Movie |
    +----------+------------+-----------+--------------+
    |       27 | JULIA      | MCQUEEN   |            7 |
    |       42 | TOM        | MIRANDA   |            6 |
    |       60 | HENRY      | BERRY     |            5 |
    |       14 | VIVIEN     | BERGEN    |            5 |
    |       94 | KENNETH    | TORN      |            4 |
    |       75 | BURT       | POSEY     |            4 |
    |       54 | PENELOPE   | PINKETT   |            4 |
    |      102 | WALTER     | TORN      |            4 |
    |       12 | KARL       | BERRY     |            4 |
    |       40 | JOHNNY     | CAGE      |            4 |
    +----------+------------+-----------+--------------+
    ```

8. Dari soal sebelumnya diketahui ```Julia McQueen``` merupakan aktris yang paling banyak membintangi film horror, dengan total **7** judul film. Tampilkan daftar __judul film horror yang pernah dibintangi oleh ```Julia McQueen```__. Kolom yang diwajibkan ada yaitu __judul film__ dan __kategorinya__. Output yang diharapkan:

    ```bash
    +--------------------+----------+
    | title              | category |
    +--------------------+----------+
    | ARABIA DOGMA       | Horror   |
    | FREDDY STORM       | Horror   |
    | HIGH ENCINO        | Horror   |
    | MONTEREY LABYRINTH | Horror   |
    | SPIRIT FLINTSTONES | Horror   |
    | STRANGERS GRAFFITI | Horror   |
    | TRAIN BUNCH        | Horror   |
    +--------------------+----------+
    ```

    ✅ _Lampirkan jawaban berupa daftar query MySQL dalam bentuk file __.txt__ (atau format text file lainnya) dan kirimkan via email ke _lintang@purwadhika.com_!_

#

### **Soal 2 - 👨‍🎓 Kerja Kerja Kerja**

Disediakan sebuah dataset yang berisi daftar profesi beberapa responder, unduh: [profesi.csv](https://raw.githubusercontent.com/LintangWisesa/Ujian_AnalyticsVisualization_JCDS07/master/profesi.csv). Buatlah sebuah file python (__.py__) atau notebook (__.ipynb__) yang dapat menyelesaikan perintah berikut.

1. __Ada berapa jenis profesi yang ada dalam dataset tersebut? Sebutkan!__
    
    Output yang diharapkan:
    
    ```bash
    21

    ['technician', 'other', 'writer', 'executive', 'administrator', 'student', 'lawyer', 'educator', 'scientist', 'entertainment', 'programmer', 'librarian', 'homemaker', 'artist', 'engineer', 'marketing', 'none', 'healthcare', 'retired', 'salesman', 'doctor']
    ```

2. __Buatlah sebuah dataframe yang menunjukkan data usia maksimal, minimal & rata-ratanya, kemudian dikelompokkan berdasarkan profesi & gender!__

    Output yang diharapkan:

    <img src='./soal2b.png' width='40%' height='40%'>

3. __Buatlah sebuah dataframe yang menunjukkan persentase pria & wanita tiap profesi!__

    Output yang diharapkan:

    <img src='./soal2c.png' width='40%' height='40%'>

✅ *Commit & push source code jawaban soal ini ke __Github__ Anda, buatlah repo dengan nama __Daftar_Profesi__, kemudian lampirkan __url link repo Github__ Anda via email ke _lintang@purwadhika.com!_*

#

🚧🚧🚧🚧🚧🚧🚧🚧🚧🚧🚧🚧🚧🚧🚧🚧🚧🚧🚧🚧🚧🚧🚧🚧🚧🚧🚧🚧🚧🚧

## <marquee><b>The last question will be published after lunch</b></marquee>

🚧🚧🚧🚧🚧🚧🚧🚧🚧🚧🚧🚧🚧🚧🚧🚧🚧🚧🚧🚧🚧🚧🚧🚧🚧🚧🚧🚧🚧🚧

#

### *__#HappyCoding__* :relaxed:

#### Lintang Wisesa :love_letter: _lintangwisesa@ymail.com_

[Facebook](https://www.facebook.com/lintangbagus) | 
[Twitter](https://twitter.com/Lintang_Wisesa) |
[Google+](https://plus.google.com/u/0/+LintangWisesa1) |
[Youtube](https://www.youtube.com/user/lintangbagus) | 
:octocat: [GitHub](https://github.com/LintangWisesa) |
[Hackster](https://www.hackster.io/lintangwisesa)