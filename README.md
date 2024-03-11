# <h1 align="center">Laporan Praktikum Modul Tipe Data</h1>
<p align="center">Egi Rizkiyansyah</p>


## Dasar Teori

A.Tipe data berfungsi untuk mempresentasikan jenis dari sebuah nilai yang terdapat dalam program. Dalam bahasa C++, tipe data dibagi menjadi tiga bagian : 
- Tipe data primitif
- Tipe data abstrak
- Tipe data koleksi

1.Tipe Data Primitif

Tipe data primitif adalah tipe data yang sederhana dan sudah siap digunakan[2]. Tipe data primitif terdiri dari beberapa jenis, yaitu integer, float, char, dan boolean.
- integer = untuk menampung bilangan bulat
- float = untuk menampung bilangan desimal
- char = untuk menyimpan bentuk apapun seperti, huruf, simbol, ataupun karakter lain
- boolean = untuk menyimpan nilai logika benar atau salah   

2.Tipe Data Abstrak

Tipe data abstrak atau biasa disebut tipe data bentukan pengguna. Pada tipe data abstrak bisa berisi banyak tipe data, jadi nilainya bisa lebih dari satu dan beragam tipe data. Dalam pemrograman berorientasi objek, tipe data abstrak disebut sebagai kelas. Sebuah instance dari suatu kelas disebut objek. Tipe data abstrak adalah dasar untuk memahami dan menerapkan tipe data tertentu, asli atau ditentukan pengguna.

3.Tipe Data Koleksi

Tipe data koleksi adalah tipe data yang digunakan untuk mengelompokkakn dan menyimpan beberapa nilai atau objek secara bersamaan. Ada beberapa tipe data koleksi yang umum digunakan, diantaranya:

- Vektor = Disebut juga array dinamis, yaitu array yang memungkinkan proses insert dan delete elemen bagian tengah array dan seakan-akan terlihat seperti mengubah ukuran array tersebut. Vektor digunakan untuk menyimpan elemen dengan tipe data serupa.

- Array = tipe data array adalah tipe data yang digunakan untuk menyimpan banyak data dalam satu variabel dengan tipe data yang sama. Ciri-ciri bahwa tipe data itu menggunakan array tandanya adalah setelah variabel nya terdapat tanda [][1].

- Map = Mirip dengan array namun indeks nya memungkinkan berupa tipe data selain integer dan indeks tersebut diberi nama "key".
## Guided 

### 1. Tipe Data Primitif

```C++
#include <iostream>
using namespace std;
// Main program
main()
{
    char op;
    float num1, num2;
    // It allows user to enter operator i.e. +, -, *, /
    cout << "masukkan operator:";
    cin >> op;
    // It allow user to enter the operands
    cout << "masukkan angka1 & 2";
    cin >> num1 >> num2;
    //switch statment begins
    switch(op)
    {
    // if user enter +
    case '+':
        cout << num1 + num2;
        break;
     //if user enter -
     case '-':
        cout << num1 - num2;
        break;
    //if user enter *
    case '*':
        cout << num1 * num2;
        break;
    //if user enter /
    case '/':
        cout << num1 / num2;
        break;
    //if the operator is other than +, -, * or /,
    //eror massage will display
    default:
        cout << "eror! operator is not correct";
    }// switch statement ends
    return 0;
}

```

Pada program di atas, proses dimulai dari fungsi main(), di mana pengguna diminta untuk memasukkan operator dan dua angka. Inputan angka yang dimasukkan akan disimpan dalam variabel num1 dan num2. Melalui perintah cout, pengguna diminta untuk memasukkan operator dan angka, sementara cin akan membaca inputan tersebut.
Jika operator yang dimasukkan tidak sesuai, pesan error akan ditampilkan, dan program akan kembali ke awal. Namun, jika operator yang dimasukkan benar, maka hasil operasi akan dicetak. Sebagai contoh, pada kode di atas, operator / dimasukkan dengan angka pertama 20 dan angka kedua 2, menghasilkan output 10, yang menunjukkan bahwa program telah berjalan dengan baik..

#### Output:
![Screenshot 2024-03-11 163532](https://github.com/egirizkiyan/egi/assets/162097461/19426f8d-a019-4a4a-b4da-981507771863)

```C++
#include <stdio.h>
//Struct
struct Mahasiswa
{
    const char *name;
    const char *address;
    int age;
};
int main()
{
    //menggunaka struct
    struct Mahasiswa mhs1, mhs2;
    mhs1.name = "dian";
    mhs1.address = "mataram";
    mhs1.age = 22;
    mhs2.name = "bambang";
    mhs2.address = "surabaya";
    mhs2.age = 23;
    // mencetak isi struct
    printf("## mahasiswa 1 ##\n");
    printf("nama: %s\n", mhs1.name);
    printf("alamat:%s\n", mhs1.address);
    printf("umur: %d\n", mhs1.age);
    printf("## mahasiswa 2 ##\n");
    printf("nama: %s\n", mhs2.name);
    printf("alamat:%s\n", mhs2.address);
    printf("umur: %d\n", mhs2.age);
    return 0;
}

```

Pada kode di atas, digunakan sebuah struktur data bernama Mahasiswa yang memiliki tiga komponen: name dengan tipe data char, address dengan tipe data char, dan age dengan tipe data integer. Dengan menggunakan struktur ini, kita dapat menyimpan beberapa informasi mengenai seorang mahasiswa dalam satu variabel..

#### Output:
![Screenshot 2024-03-11 164759](https://github.com/egirizkiyan/egi/assets/162097461/239e73cd-ab8c-48f2-90d8-0e6d6fbe3144)

### 3. Tipe Data Koleksi

```C++
#include <iostream>
using namespace std;
int main()
{
    //deklarasi dan inisialisasi array
    int nilai[5];
    nilai[0] = 23;
    nilai[1] = 50;
    nilai[2] = 34;
    nilai[3] = 78;
    nilai[4] = 90;

    //mencetak array
    cout << "Isi array pertama :" << nilai[0] << endl;
    cout << "Isi array kedua :" << nilai[1] << endl;
    cout << "Isi array ketiga :" << nilai[2] << endl;
    cout << "Isi array keempat :" << nilai[3] << endl;
    cout << "Isi array kelima :" << nilai[4] << endl;
    return 0;
}
```
Pada kode diatas, nilai array di deklarasikan di inisialisasikan ke setiap elemen array. Seperti pada nilai array pertama di inisialisasikan dengan nilai 23. Setelah di inisialisasikan kode akan mencetak array menggunakan fungsi cout. Jika proses berhasil dijalankan kode akan mengembalikan nilai 0.
#### Output:
![Screenshot 2024-03-11 165447](https://github.com/egirizkiyan/egi/assets/162097461/8b789fc3-4b51-452f-aa4e-ccceec3f38be)

## Unguided 

### 1. Buatlah program menggunakan tipe data primitif minimal dua fungsi dan bebas. Menampilkan program, jelaskan program tersebut dan ambil kesimpulan dari materi tipe data primitif!

```C++
#include <iostream>

using namespace std;

int main() {
  // Deklarasi variabel
  int bilangan1, bilangan2, bilangan3;
  float rataRata;

  // Meminta input dari pengguna
  cout << "Masukkan bilangan 1: ";
  cin >> bilangan1;
  cout << "Masukkan bilangan 2: ";
  cin >> bilangan2;
  cout << "Masukkan bilangan 3: ";
  cin >> bilangan3;

  // Menghitung total dan rata-rata
  int total = bilangan1 + bilangan2 + bilangan3;
  rataRata = static_cast<float>(total) / 3; // Konversi integer ke float

  // Menampilkan hasil perhitungan
  cout << "Rata-rata dari " << bilangan1 << ", " << bilangan2 << ", dan " << bilangan3 << " adalah: " << rataRata << endl;

  return 0;
}

```
Program diatas digunakan untuk menghitung rata-rata dari 3 bilangan yang di masukkan. program tersebut menggunakan deklarasi variabel dengan tipe data float dan integer. Untuk meminta inputan dari user menggunakan fungsi cout untuk menampilkan pesan instruksi nya.Setelah inputan di masukkan fungsi cin akan membaca dan mengambil inputan tersebut dan menyimpannya ke variabel bilangan. Setelah semua angka dimasukkan maka program akan menghitung total rata-rata dari ketiga bilangan dengan menambahkan ketiga bilangan dan mengkonversi total nya ke dalam bentuk float. Setelah itu program akan menampilkan hasilnya menggunakan fungsi cout dan setelah program berakhir akan mengembalikan nilai 0.
#### Output:
<img width="347" alt="Screenshot 2024-03-09 112113" src="https://github.com/yasminealifta/Praktikum-Struktur-Data-Assignment/assets/161322990/45b5bbbd-dfee-4776-a028-87cc8c6109ee">

Penjelasan Program:

Program di atas memiliki dua fungsi, yaitu calculate_area() dan calculate_perimeter().
Fungsi calculate_area() mengambil dua parameter, yaitu length (panjang) dan width (lebar), kemudian menghitung luas persegi panjang dengan rumus luas = panjang * lebar.
Fungsi calculate_perimeter() juga mengambil dua parameter, yaitu length dan width, dan menghitung keliling persegi panjang dengan rumus keliling = 2 * (panjang + lebar).
Pengguna diminta untuk memasukkan nilai panjang dan lebar.
Nilai panjang dan lebar yang dimasukkan oleh pengguna kemudian digunakan sebagai argumen saat memanggil fungsi-fungsi calculate_area() dan calculate_perimeter().
Hasil perhitungan luas dan keliling persegi panjang kemudian dicetak ke layar.
Kesimpulan:

Tipe data primitif yang digunakan dalam program ini adalah bilangan floating-point (float) untuk merepresentasikan panjang dan lebar persegi panjang.
Program ini menunjukkan cara menggunakan tipe data primitif untuk melakukan perhitungan matematika sederhana dan interaksi dengan pengguna.
Penggunaan tipe data primitif memungkinkan kita untuk melakukan operasi matematika dan pemrosesan data dengan efisien.
Dalam pemrograman, pemilihan tipe data yang tepat penting untuk memastikan efisiensi dan keakuratan dalam penyimpanan dan pengolahan data.


### 2. Jelaskan fungsi dari class dan struct secara detail dan berikan contoh programnya

Fungsi class:

Class berfungsi untuk membuat tipe data kompleks dengan atribut dan metode yang dapat diakses melalui objek. Aksesibilitas anggota class adalah private, yang berarti jika objek anggota dari class itu sendiri ingin dipublikasikan, maka harus menggunakan publik.

Fungsi struct:

Struct digunakan untuk menyimpan data dengan struktur yang sederhana dan biasanya tidak memiliki metode atau fungsi terkait. Biasanya sering digunakan untuk keperluan ata sederhana dan kompleks, dan dapat diakses secara langsung tanpa pembuatan objek. Struct aksesibilitasnya adalah publik

```C++
#include <iostream>
#include <string>
using namespace std;

// Definisi class Mahasiswa
class Mahasiswa {
public:
    string nama;
    string jurusan;
    int umur;

    // Metode untuk menampilkan informasi mahasiswa
    void displayInfo() {
        cout << "Nama: " << nama << endl;
        cout << "Jurusan: " << jurusan << endl;
        cout << "Umur: " << umur << " tahun" << endl;
    }
};

int main() {
    // Membuat objek mahasiswa
    Mahasiswa mhs1;
    mhs1.nama = "egi rizkiyansyah";
    mhs1.jurusan = "Informatika";
    mhs1.umur = 20;

    // Memanggil metode untuk menampilkan informasi mahasiswa
    mhs1.displayInfo();
    return 0;
}
```
Kode program diatas memiliki 2 kelas yaitu Mahasiswa dan Asal. Kelas Mahasiswa memiliki 2 atribut yaitu nama dan ttl, Asal juga memiliki 2 atribut yaitu asal dan umur. Program tersebut menggunakan tipe data string dan integer. String digunakan untuk menyimpan nama mahasiswa , ttl dan asal. Integer digunakan untuk menyimpan umur. Semua program akan dicetak menggunakan fungsi cout dan akan menampilkan output seperti pada gambar dibawah. Ketika program telah berjalan dengan benar maka akan mengembalikan nilai 0.

#### Output:
![Screenshot 2024-03-11 183521](https://github.com/egirizkiyan/egi.r/assets/162097461/3e8da568-0eb5-42f4-abc0-fe2e4782b76d)


### 3. Buat dan jelaskan program menggunakan fungsi map dan jelaskan perbedaan dari array dengan map.
```C++
#include <iostream>
#include <map>

using namespace std;

int main() {
  // Membuat map
  map<string, int> buah;

  // Menambahkan data ke map
  buah["Apel"] = 20;
  buah["Jeruk"] = 21;
  buah["Mangga"] = 22;
  buah["Anggur"] = 25;
  buah["Melon"] = 10;

  // Menampilkan data map
  for (auto it = buah.begin(); it != buah.end(); ++it) {
    cout << it->first << " : " << it->second << endl;
  }

  // Mencari data di map
  auto it = buah.find("Apel");
  if (it != buah.end()) {
    cout << "Buah Apel : " << it->second << endl;
  } else {
    cout << "Buah Apel tidak ditemukan" << endl;
  }

  return 0;
}

```
Pada program di atas, objek map dengan nama "buah" dibuat dan diinisialisasi. Kemudian data buah ditambahkan ke dalam map menggunakan key-value pairs, di mana key adalah nama buah dan nilai adalah jumlah buah yang ada. Untuk menampilkan data buah, dilakukan perulangan for. Dalam pencarian data di map, fungsi find digunakan. Jika data tidak ditemukan, fungsi find akan mengembalikan nilai end, dan pesan "buah tidak ditemukan" akan dicetak menggunakan cout. Jika buah yang dicari ditemukan, jumlah buah yang tersedia akan dicetak menggunakan cout.
#### Output:
![Screenshot 2024-03-11 183950](https://github.com/egirizkiyan/egi.r/assets/162097461/84fddb88-6cf9-49a1-84ee-89b01ee8427a)

Perbedaan Array dan Map:

Array adalah struktur data yang statis yang menyimpan elemen-elemen dengan tipe data yang sama yang didefinisikan oleh pemilik array. Memiliki indeks yang berurutan dan harus berurutan, tidak mengandung elemen yang berbeda tipe data, didefinisikan menggunakan tanda [], dapat didefinisikan menggunakan konstanta dan nilai indeks. 

Map adalah sekumpulan elemen yang didefinisikan oleh key dan nilai yang dipetakan. Memiliki indeks yang berupa key yang dapat berupa tipe data selain integer, dapat mengandung elemen yang berbeda tipe data, memiliki key dan nilai yang berbeda tipe data, dapat didefinisikan menggunakan std::map.


## Kesimpulan
Pengetahuan tentang tipe data yang beragam, seperti integer, float, array, string, map, char, dan boolean, adalah elemen kunci dalam pengembangan program yang efektif. Setiap tipe data memiliki peran dan karakteristiknya sendiri dalam mengorganisir dan memproses informasi
## Referensi
[1] K. Loudon, C++ Pocket Reference. O’Reilly Media, (2006). Referebsi saku c++ Edisi pertama. O'reailly.

[2] S. Rao, Sams Teach yourself C++ in one hour a day. Samsublishing, (2017). C++ Dalam satu jam sehari,sams teach yourself edisi ke 8 . Penerbit sams.