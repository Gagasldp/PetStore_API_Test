Automation Testing – PetStore API
==========================================

1. DESKRIPSI
------------------------------------------

CASE 02 – PetStore API (Postman + Newman)
Project ini merupakan pengujian REST API pada layanan:
https://petstore.swagger.io/

Metode yang digunakan:
- Postman Collection dengan 15 skenario (7 positif, 7 negatif, 1 mixed)
- Chaining antar request menggunakan environment variable ({{petId}}, {{orderId}}, {{userId}}), {{deletedOrderId}}
- Assertion untuk status code dan response body
- Report hasil eksekusi menggunakan Newman CLI

Total Test Case: 15
(7 Positif, 7 Negatif, 1 Mixed)

2. REQUIREMENT
------------------------------------------

CASE 02 – PetStore API:
1. Buka Postman
2. Import file:
   - PetStore API.postman_collection.json
   - Petstore_env.postman_environment.json (untuk chaining variable)
3. Jalankan Collection Runner
4. Pastikan semua test PASS
5. Export Collection dan Environment (backup)

Menjalankan via Newman CLI:
newman run "PetStore API.postman_collection.json" -e "Petstore_env.postman_environment.json" -r cli,html,json,junit --reporter-junit-export "newman/newman-report.xml"

Hasil eksekusi tersimpan di folder:
└── newman/
    ├── newman-Report.xml
    └── newman-run-report-2025-10-05-12-11-11-637-0.json

Buka file HTML di browser untuk melihat hasil visual,
atau simpan sebagai PDF (Ctrl+P → Save as PDF).

4. CATATAN
------------------------------------------

PetStore API:
- Mencakup 15 skenario (7 positif, 7 negatif, 1 mixed)
- Assertion status code dan response body
- Chaining antar endpoint (create → get → update → delete)
- Report hasil test dihasilkan otomatis oleh Newman

5. STRUKTUR FOLDER
------------------------------------------

├── PetStore_Test/
│   ├── PetStore API.postman_collection.json
│   ├── Petstore_env.postman_environment.json
│   ├── TC_CASE02.xlsx
│   └── reports/
│       ├── newman-Report.xml
│       └── newman-run-report-2025-10-05-12-11-11-637-0.json
│
└── README.txt

------------------------------------------