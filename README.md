# Final Project: NFL Attendance Dataset
## Teknik Sains Data dan Wrangling

---

## 👥 Kelompok 6

| NRP | Nama |
|-----|------|
| 5052241016 | M. Dafy Irwansyah |
| 5052241034 | Alycia Zada |
| 5052241038 | Annisa Maulida |
| 5052241039 | M. Kafanal Kafi |

---

## 📋 Deskripsi Proyek

Proyek ini menganalisis **NFL Attendance Dataset** yang terdiri dari tiga dataset berbeda:
- **attendance.csv**: Data kehadiran penonton di setiap pertandingan
- **standings.csv**: Track margin kemenangan sebuah tim
- **games.csv**: Detail setiap pertandingan (kapan, siapa, dan hasil)

### Tujuan Analisis
1. Mengidentifikasi tren kehadiran penonton NFL dari tahun 2000-2019
2. Memahami hubungan antara performa tim dan loyalitas penggemar
3. Memberikan insight untuk optimalisasi strategi marketing dan operasional tim
4. Mengungkap faktor-faktor kunci yang mendorong atau menghambat kehadiran penonton

---

## 📁 Struktur File

```
finalproject/
│
├── README.md                    # Dokumentasi proyek
├── requirements.txt             # Dependencies Python
│
├── data/
│   ├── raw/                     # Dataset mentah
│   │   ├── attendance.csv
│   │   ├── standings.csv
│   │   └── games.csv
│   │
│   └── processed/               # Dataset yang sudah diproses
│
└── notebooks/
    └── final_project.ipynb      # Jupyter notebook analisis utama
```

---

## 🚀 Cara Menjalankan Ulang Proyek

### 1. Prerequisites
Pastikan Anda telah menginstall:
- Python 3.8 atau lebih baru
- pip (Python package manager)
- Jupyter Notebook atau Positron/VS Code dengan ekstensi Jupyter

### 2. Clone Repository
```bash
git clone <repository-url>
cd finalproject
```

### 3. Setup Environment

#### Opsi A: Menggunakan Virtual Environment (Recommended)
```bash
# Buat virtual environment
python -m venv venv

# Aktifkan virtual environment
# Windows:
venv\Scripts\activate
# Linux/Mac:
source venv/bin/activate

# Install dependencies
pip install -r requirements.txt
```

#### Opsi B: Install Langsung
```bash
pip install -r requirements.txt
```

### 4. Jalankan Jupyter Notebook
```bash
# Buka Jupyter Notebook
jupyter notebook

# Atau jika menggunakan Jupyter Lab
jupyter lab
```

Kemudian buka file `notebooks/final_project.ipynb` dan jalankan cell-cell secara berurutan.

### 5. Alternatif: Menggunakan VS Code/Positron
1. Buka folder proyek di VS Code/Positron
2. Install ekstensi Python dan Jupyter
3. Buka file `notebooks/final_project.ipynb`
4. Pilih kernel Python yang sesuai (dari virtual environment jika menggunakan)
5. Jalankan cell-cell secara berurutan

---

## 📦 Dependencies

Package yang digunakan dalam proyek ini:

| Package | Versi Minimum | Fungsi |
|---------|---------------|--------|
| numpy | 1.21.0 | Operasi array dan perhitungan statistik |
| pandas | 1.3.0 | Manipulasi dan analisis data |
| matplotlib | 3.4.0 | Visualisasi data dasar |
| seaborn | 0.11.0 | Visualisasi data statistik |

Untuk melihat detail lengkap, lihat file `requirements.txt`.

---

## 🔍 Proses Data Cleanup

### 1. Import Dataset
Dataset diimport menggunakan pandas dari folder `data/raw/`:
- `attendance.csv`
- `standings.csv`
- `games.csv`

### 2. Data Merging
Membuat DataFrame `merged_df` dengan menggabungkan dataset `attendance` dan `standings` berdasarkan kolom:
- `year`
- `team_name`
- `team`

### 3. Missing Values Analysis
- Identifikasi missing values pada setiap kolom
- Perhitungan persentase missing values
- Visualisasi distribusi missing values menggunakan bar plot

### 4. Data Cleaning
Proses cleaning dilakukan untuk:
- Menangani missing values
- Normalisasi data
- Filtering data yang relevan
- Transformasi data untuk analisis

### 5. Exploratory Data Analysis (EDA)
- Analisis tren kehadiran penonton
- Korelasi antara performa tim dan kehadiran
- Pola musiman dan mingguan
- Identifikasi tim dengan basis penggemar paling loyal

---

## 📊 Hasil Analisis

Hasil analisis lengkap dapat dilihat di dalam notebook `notebooks/final_project.ipynb`, yang mencakup:
- Visualisasi tren kehadiran dari tahun 2000-2019
- Analisis korelasi performa tim vs kehadiran penonton
- Identifikasi faktor-faktor yang mempengaruhi kehadiran
- Insight untuk strategi bisnis dan marketing

---

## 📝 Catatan Tambahan

### Color Palette
Proyek ini menggunakan NFL-themed color palette untuk visualisasi:
- Deep Navy (#0B2265)
- NFL Red (#D50A0A)
- Metallic Gold (#AA8A00)
- Dark Green (#004C54)
- Silver/Grey (#A5ACAF)
- Black (#000000)

### Dataset Information
- **merged_df**: 10,846 rows × 20 columns
- **games**: 5,324 rows × 19 columns
- Periode data: 2000-2019

---

## 🤝 Kontribusi

Setiap anggota kelompok berkontribusi dalam:
- Data collection dan preprocessing
- Exploratory Data Analysis
- Visualisasi data
- Interpretasi hasil
- Dokumentasi