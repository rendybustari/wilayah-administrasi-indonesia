# Wilayah Administrasi Indonesia
Data Wilayah Administrasi Indonesia terdiri dari Provinsi, Kota/Kabupaten, Kecamatan, Kelurahan, data ini disimpan dalam bentuk SQL

## Installation Untuk Pengguna Laravel
- Clone sql data administrasi indonesia

```
git clone https://github.com/rendybustari/wilayah-administrasi-indonesia
```

- Pindahkan file indonesian_region_data.sql ke project/public/sql/
- Buat file seeder

```
php artisan make:seeder SqlIndonesianRegionDataSeeder
```

- Lengkapi source codenya menjadi

```
<?php

namespace Database\Seeders;

use Illuminate\Database\Seeder;
use Illuminate\Support\Facades\DB;

class SqlIndonesianRegionDataSeeder extends Seeder
{
    /**
     * Run the database seeds.
     *
     * @return void
     */
    public function run()
    {
        $path = public_path('sql/indonesian_region_data.sql');
        $sql = file_get_contents($path);
        DB::unprepared($sql);
    }
}

```

- Jalankan Perintah Seedernya
```
php artisan db:seed --class=SqlIndonesianRegionDataSeeder
```

- Selesai :)
# happyu
