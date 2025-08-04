# PANDUAN LENGKAP SETUP MYOB MULIA MODISTE

## 📋 DAFTAR ISI
1. [Informasi Perusahaan](#informasi-perusahaan)
2. [Chart of Accounts](#chart-of-accounts)
3. [Customer Cards](#customer-cards)
4. [Supplier Cards](#supplier-cards)
5. [Item/Service List](#itemservice-list)
6. [Sample Transactions](#sample-transactions)
7. [Setup Instructions](#setup-instructions)
8. [Data Entry Guide](#data-entry-guide)
9. [Report Generation](#report-generation)

---

## 🏢 INFORMASI PERUSAHAAN

### Company Details
```
Nama Perusahaan: MULIA MODISTE
Alamat: Jalan Adisucipto No. 1A Sungai Raya - Kubu Raya
Telepon: (0561) 712345
Email: muliamodiste@gmail.com
Website: -
Bisnis: Jasa Jahit dan obras (Sewing and Embroidery Services)
Tanggal Berdiri: 1 Maret 2019
Pemilik: Ny. Mulia
```

### Business Information
```
ABN: -
GST Registration: -
Tax File Number: -
Financial Year: 1 Maret - 28 Februari
Default Currency: IDR (Indonesian Rupiah)
```

---

## 📊 CHART OF ACCOUNTS

### File: chart_of_accounts.csv
```csv
Account Number,Account Name,Account Type,Description,Tax Code
1-101,Kas,Asset,Cash on hand,-
1-102,Piutang Usaha,Asset,Accounts Receivable,-
1-103,Sewa Kios Dibayar Dimuka,Asset,Prepaid Rent,-
1-104,Perlengkapan Jahit,Asset,Sewing Supplies,-
1-105,Perlengkapan Rupa-Rupa,Asset,Miscellaneous Supplies,-
1-201,Peralatan Jahit,Asset,Sewing Equipment,-
1-202,Ak. Peny. Peralatan Jahit,Asset,Accumulated Depreciation - Sewing Equipment,-
1-203,Peralatan Rupa-Rupa,Asset,Miscellaneous Equipment,-
1-204,Ak. Peny. Peralatan Rupa-Rupa,Asset,Accumulated Depreciation - Miscellaneous Equipment,-
2-101,Utang Usaha,Liability,Accounts Payable,-
2-102,Utang Bunga,Liability,Interest Payable,-
2-103,Utang Gaji,Liability,Salaries Payable,-
2-201,Utang Bank,Liability,Bank Loan,-
3-101,Modal Ny. Mulia,Equity,Ny. Mulia Capital,-
3-102,Prive Ny. Mulia,Equity,Ny. Mulia Drawings,-
3-999,Ikhtisar Laba Rugi,Equity,Income Summary,-
4-101,Pendapatan Jahit,Income,Sewing Revenue,-
4-102,Pendapatan Obras,Income,Embroidery Revenue,-
5-101,Gaji dan Upah,Expense,Salaries and Wages,-
5-102,Beban Sewa Kios,Expense,Rent Expense,-
5-103,Beban Perlengkapan Jahit,Expense,Sewing Supplies Expense,-
5-104,Beban Perlengkapan Rupa-Rupa,Expense,Miscellaneous Supplies Expense,-
5-105,Beban Listrik dan Air,Expense,Electricity and Water Expense,-
5-106,Beban Pemeliharaan Peralatan,Expense,Equipment Maintenance Expense,-
5-107,Beban Peny. Peralatan Jahit,Expense,Depreciation Expense - Sewing Equipment,-
5-108,Beban Peny. Peralatan Rupa-Rupa,Expense,Depreciation Expense - Miscellaneous Equipment,-
5-109,Beban Bunga,Expense,Interest Expense,-
5-199,Beban Rupa-Rupa,Expense,Miscellaneous Expense,-
```

---

## 👥 CUSTOMER CARDS

### File: customer_cards.csv
```csv
Card Name,Card Type,Address,Phone,Email,Payment Terms,Default Account,Notes
Pelanggan,Customer,Jl. Adisucipto No. 1A Sungai Raya,(0561) 712345,muliamodiste@gmail.com,Cash,4-101,General customers for sewing services
LIO TAILOR,Customer,Jl. Adisucipto Kompl Sakura Permai No 14 Sungai Raya,0561-6122223,lio.tailor@email.com,n/15,4-102,Embroidery services customer
```

### Customer Details:
```
1. PELANGGAN (General Customers)
   - Address: Jl. Adisucipto No. 1A Sungai Raya
   - Phone: (0561) 712345
   - Payment Terms: Cash/Immediate
   - Services: Sewing (Jahit)
   - Revenue Account: 4-101 Pendapatan Jahit

2. LIO TAILOR (Tn. LIO CHEN)
   - Address: Jl. Adisucipto Kompl Sakura Permai No 14 Sungai Raya
   - Phone: 0561-6122223
   - Payment Terms: n/15 (Net 15 days)
   - Services: Embroidery (Obras)
   - Revenue Account: 4-102 Pendapatan Obras
```

---

## 🏪 SUPPLIER CARDS

### File: supplier_cards.csv
```csv
Card Name,Card Type,Address,Phone,Email,Payment Terms,Default Account,Notes
Toko MAJU,Supplier,Jl. Djuanda No 2 Pontianak,(0561) 888 666,maju@email.com,n/15,2-101,Supplies sewing materials
Toko BINTANG,Supplier,Jl. H. Agus Salim No. 14 Pontianak,(0561) 101 222,bintang@email.com,Cash,2-101,Sewing machines and equipment
Toko MEKAR,Supplier,Jl. Ahmad Yani II No. 16,0561-650011,mekar@email.com,Cash,2-101,Various accessories
PDAM dan PLN,Supplier,Jl. Adisucipto No. 1A Sungai Raya,(0561) 712345,utilities@email.com,Monthly,2-101,Water and electricity
Surianto,Supplier,Jl. Adisucipto No. 1A Sungai Raya,(0561) 712345,surianto@email.com,Quarterly,2-101,Kiosk rent
Suminah,Supplier,Jl. Adisucipto No. 1A Sungai Raya,(0561) 712345,suminah@email.com,Weekly,5-101,Tailor employee
Anton Servis,Supplier,Jl. Adisucipto No. 1A Sungai Raya,(0561) 712345,anton@email.com,On Demand,5-106,Sewing machine service
Jamal,Supplier,Jl. Adisucipto No. 1A Sungai Raya,(0561) 712345,jamal@email.com,Monthly,5-199,Security and cleaning
```

### Supplier Details:
```
1. TOKO MAJU
   - Address: Jl. Djuanda No 2, Pontianak
   - Phone: (0561) 888 666
   - Payment Terms: n/15
   - Items: Perlengkapan jahit dan rupa-rupa
   - Account: 2-101 Utang Usaha

2. TOKO BINTANG
   - Address: Jl. H. Agus Salim No. 14, Pontianak
   - Phone: (0561) 101 222
   - Payment Terms: Cash
   - Items: Mesin jahit dan peralatan
   - Account: 2-101 Utang Usaha

3. TOKO MEKAR
   - Address: Jl. Ahmad Yani II No. 16
   - Phone: 0561-650011
   - Payment Terms: Cash
   - Items: Aneka perlengkapan rupa-rupa
   - Account: 2-101 Utang Usaha

4. PDAM dan PLN
   - Address: Jl. Adisucipto No. 1A Sungai Raya
   - Phone: (0561) 712345
   - Payment Terms: Monthly
   - Items: Tagihan air dan listrik
   - Account: 2-101 Utang Usaha

5. SURIANTO
   - Address: Jl. Adisucipto No. 1A Sungai Raya
   - Phone: (0561) 712345
   - Payment Terms: Quarterly
   - Items: Sewa kios
   - Account: 2-101 Utang Usaha

6. SUMINAH
   - Address: Jl. Adisucipto No. 1A Sungai Raya
   - Phone: (0561) 712345
   - Payment Terms: Weekly
   - Items: Upah karyawan
   - Account: 5-101 Gaji dan Upah

7. ANTON SERVIS
   - Address: Jl. Adisucipto No. 1A Sungai Raya
   - Phone: (0561) 712345
   - Payment Terms: On Demand
   - Items: Servis mesin jahit
   - Account: 5-106 Beban Pemeliharaan Peralatan

8. JAMAL
   - Address: Jl. Adisucipto No. 1A Sungai Raya
   - Phone: (0561) 712345
   - Payment Terms: Monthly
   - Items: Iuran keamanan dan kebersihan
   - Account: 5-199 Beban Rupa-Rupa
```

---

## 📦 ITEM/SERVICE LIST

### File: item_service_list.csv
```csv
Item Number,Item Name,Item Type,Description,Unit Price,Account,Notes
JHT001,Jasa Jahit,Service,Sewing services for customers,150000,4-101,Per piece/item
OBR001,Jasa Obras,Service,Embroidery services for LIO TAILOR,200000,4-102,Per package
MES001,Mesin Jahit Serbaguna Singer,Asset,Singer multi-purpose sewing machine,800000,1-201,Fixed asset
MES002,Mesin Jahit Butterfly,Asset,Butterfly sewing machine,750000,1-201,Fixed asset
MES003,Mesin Obras,Asset,Overlock machine,450000,1-201,Fixed asset
PRL001,Peralatan Rupa-Rupa,Asset,Miscellaneous equipment,500000,1-203,Fixed asset
PLG001,Perlengkapan Jahit,Expense,Sewing supplies (thread, needles),60000,5-103,Consumable
PLG002,Perlengkapan Rupa-Rupa,Expense,Miscellaneous supplies,50000,5-104,Consumable
UTL001,Tagihan Air dan Listrik,Expense,Water and electricity bills,100000,5-105,Monthly utility
SEWA001,Sewa Kios,Expense,Kiosk rent,300000,5-102,Quarterly payment
GAJI001,Upah Karyawan,Expense,Employee wages,150000,5-101,Weekly payment
SERV001,Servis Mesin Jahit,Expense,Sewing machine maintenance,50000,5-106,As needed
IURAN001,Iuran Keamanan dan Kebersihan,Expense,Security and cleaning fee,150000,5-199,Monthly fee
```

### Item Categories:
```
1. SERVICES (Jasa)
   - Jasa Jahit (Sewing Services)
   - Jasa Obras (Embroidery Services)

2. ASSETS (Aktiva)
   - Mesin Jahit (Sewing Machines)
   - Peralatan (Equipment)

3. EXPENSES (Beban)
   - Perlengkapan (Supplies)
   - Utilitas (Utilities)
   - Sewa (Rent)
   - Gaji (Wages)
   - Servis (Services)
   - Iuran (Fees)
```

---

## 💰 SAMPLE TRANSACTIONS

### File: sample_transactions.csv
```csv
Date,Transaction Type,Reference,Card Name,Account,Description,Amount,Debit Account,Credit Account
01/03/2019,Cash Outflow,KK-01,Surianto,5-102,Sewa kios untuk 3 bulan (Maret - Mei 2019),900000,5-102,1-101
02/03/2019,Purchase,TB-NK-53,Toko BINTANG,1-201,Mesin Jahit Serbaguna merk Singer,800000,1-201,1-101
02/03/2019,Purchase,TB-NK-53,Toko BINTANG,1-201,2x Mesin Jahit merk Butterfly,1500000,1-201,1-101
02/03/2019,Purchase,TB-NK-53,Toko BINTANG,1-201,Mesin Obras,450000,1-201,1-101
02/03/2019,Purchase,TB-NK-53,Toko BINTANG,1-203,Peralatan Rupa-Rupa,500000,1-203,1-101
06/03/2019,Cash Outflow,KK-02,PDAM dan PLN,5-105,Tagihan untuk air dan listrik kios,100000,5-105,1-101
07/03/2019,Purchase,TM01,Toko MAJU,5-103,Perlengkapan jahit,60000,5-103,2-101
09/03/2019,Cash Outflow,KK-03,Suminah,5-101,Upah mingguan periode 1-8 Maret 2019,150000,5-101,1-101
09/03/2019,Cash Inflow,KM-03,Pelanggan,4-101,Upah jahit dari langganan,850000,1-101,4-101
12/03/2019,Purchase,M-NK0311,Toko MEKAR,5-104,Aneka perlengkapan rupa-rupa,50000,5-104,1-101
15/03/2019,Sales Invoice,F0301,LIO TAILOR,4-102,Pekerjaan Obras periode 2-14 Maret 2019,200000,1-102,4-102
16/03/2019,Cash Inflow,KM-04,Pelanggan,4-101,Upah jahit dari langganan,1250000,1-101,4-101
17/03/2019,Cash Inflow,KM-05,LIO TAILOR,4-102,Pelunasan faktur no F0301 tanggal 15 Maret 2019,200000,1-101,1-102
21/03/2019,Cash Outflow,KK-04,Toko MAJU,2-101,Pembayaran Faktur No. TM01 tanggal 7 Maret 2019,60000,2-101,1-101
22/03/2019,Cash Outflow,KK-05,Anton Servis,5-106,Ongkos servis mesin jahit,50000,5-106,1-101
23/03/2019,Cash Outflow,KK-06,Ny. Mulia,3-102,Pengambilan untuk keperluan pribadi,150000,3-102,1-101
24/03/2019,Cash Outflow,KK-07,Suminah,5-101,Upah mingguan periode 9-23 Maret 2019,150000,5-101,1-101
26/03/2019,Purchase,TM23,Toko MAJU,5-103,Perlengkapan jahit,150000,5-103,2-101
27/03/2019,Cash Outflow,KK-08,Jamal,5-199,Iuran keamanan dan kebersihan lingkungan kios,150000,5-199,1-101
28/03/2019,Cash Inflow,KM-06,Pelanggan,4-101,Upah jahit dari langganan,950000,1-101,4-101
30/03/2019,Sales Invoice,F0302,LIO TAILOR,4-102,Pekerjaan Obras periode 16-29 Maret 2019,150000,1-102,4-102
31/03/2019,Cash Outflow,KK-09,Ny. Mulia,5-101,Gaji bagian pembukuan/keuangan bulan Maret 2019,300000,5-101,1-101
31/03/2019,Journal Entry,M-0301,-,4-101,Jasa jahit yang telah selesai tetapi belum diterima,150000,1-102,4-101
31/03/2019,Journal Entry,M-0302,-,5-102,Sewa yang telah jatuh tempo untuk bulan maret,300000,5-102,2-101
31/03/2019,Journal Entry,M-0303,-,5-107,Peralatan jahit dan peralatan rupa-rupa disusutkan,250000,5-107,1-202
31/03/2019,Journal Entry,M-0304,-,2-201,Angsuran utang bank sebesar Rp 500.000,- sudah dibayarkan,500000,2-201,1-101
31/03/2019,Journal Entry,M-0305,-,5-101,Upah karyawan minggu terakhir yang belum dibayarkan,150000,5-101,2-103
31/03/2019,Journal Entry,M-0306,-,5-103,Perlengkapan jahit yang masih ada senilai Rp 100.000,-,100000,1-104,5-103
31/03/2019,Journal Entry,M-0306,-,5-104,Perlengkapan rupa-rupa yang terpakai sebesar Rp 40.000,-,40000,5-104,1-105
```

---

## ⚙️ SETUP INSTRUCTIONS

### Step 1: Install MYOB AccountRight
```
1. Download MYOB AccountRight v19.4 atau v20
2. Install sesuai sistem operasi (Windows/Mac)
3. Aktivasi lisensi
4. Setup company file baru
```

### Step 2: Company Setup
```
1. Buka MYOB AccountRight
2. File > New Company
3. Masukkan informasi perusahaan:
   - Company Name: MULIA MODISTE
   - Address: Jalan Adisucipto No. 1A Sungai Raya - Kubu Raya
   - Phone: (0561) 712345
   - Email: muliamodiste@gmail.com
4. Set financial year: 1 Maret - 28 Februari
5. Set currency: IDR (Indonesian Rupiah)
```

### Step 3: Import Chart of Accounts
```
1. Buka Accounts > Accounts List
2. File > Import > Chart of Accounts
3. Pilih file: chart_of_accounts.csv
4. Map columns sesuai format
5. Import dan review
```

### Step 4: Import Customer Cards
```
1. Buka Card File > Cards List
2. File > Import > Customer Cards
3. Pilih file: customer_cards.csv
4. Map columns sesuai format
5. Import dan review
```

### Step 5: Import Supplier Cards
```
1. Buka Card File > Cards List
2. File > Import > Supplier Cards
3. Pilih file: supplier_cards.csv
4. Map columns sesuai format
5. Import dan review
```

### Step 6: Import Item/Service List
```
1. Buka Sales > Items
2. File > Import > Item List
3. Pilih file: item_service_list.csv
4. Map columns sesuai format
5. Import dan review
```

### Step 7: Enter Opening Balances
```
1. Buka Accounts > Accounts List
2. Set opening balances untuk semua accounts
3. Review trial balance
4. Post opening balances
```

### Step 8: Enter Sample Transactions
```
1. Buka Banking > Spend Money (untuk cash outflows)
2. Buka Banking > Receive Money (untuk cash inflows)
3. Buka Sales > Enter Sales (untuk sales invoices)
4. Buka Purchases > Enter Purchases (untuk purchase bills)
5. Buka Accounts > Record Journal Entry (untuk adjustments)
6. Enter semua transaksi dari sample_transactions.csv
```

---

## 📝 DATA ENTRY GUIDE

### Cash Inflow (BUKTI KAS MASUK)
```
1. Banking > Receive Money
2. Deposit To: Cash Account (1-101)
3. Card: Pilih customer (Pelanggan/LIO TAILOR)
4. Date: Tanggal transaksi
5. Reference: BKM No. (KM-01, KM-02, dll)
6. Amount: Jumlah diterima
7. Memo: Keterangan transaksi
8. Account: Revenue account (4-101/4-102)
9. Record
```

### Cash Outflow (BUKTI KAS KELUAR)
```
1. Banking > Spend Money
2. Pay From: Cash Account (1-101)
3. Card: Pilih supplier
4. Date: Tanggal transaksi
5. Reference: BKK No. (KK-01, KK-02, dll)
6. Amount: Jumlah dibayar
7. Memo: Keterangan transaksi
8. Account: Expense account sesuai jenis
9. Record
```

### Sales Invoice (FAKTUR PENJUALAN)
```
1. Sales > Enter Sales
2. Card: Pilih customer (LIO TAILOR)
3. Date: Tanggal invoice
4. Invoice No.: No. Faktur (F0301, F0302)
5. Terms: Payment terms (n/15)
6. Item: Pilih item/service
7. Quantity: Jumlah
8. Price: Harga per unit
9. Account: Revenue account (4-101/4-102)
10. Record
```

### Purchase Bill (FAKTUR PEMBELIAN)
```
1. Purchases > Enter Purchases
2. Card: Pilih supplier
3. Date: Tanggal bill
4. Purchase No.: No. Faktur supplier
5. Terms: Payment terms
6. Item: Pilih item
7. Quantity: Jumlah
8. Price: Harga per unit
9. Account: Expense/Asset account
10. Record
```

### Journal Entry (BUKTI MEMORIAL)
```
1. Accounts > Record Journal Entry
2. Date: Tanggal adjustment
3. Reference: BM No. (M-0301, M-0302, dll)
4. Memo: Keterangan adjustment
5. Debit Account: Account yang didebit
6. Credit Account: Account yang dikredit
7. Amount: Jumlah adjustment
8. Record
```

---

## 📊 REPORT GENERATION

### Financial Reports
```
1. Reports > Financial Reports
   - Profit & Loss Statement
   - Balance Sheet
   - Cash Flow Statement
   - Statement of Owner's Equity

2. Reports > Management Reports
   - Aged Receivables
   - Aged Payables
   - Sales Register
   - Purchases Register
   - General Ledger
```

### Customer Reports
```
1. Reports > Sales Reports
   - Customer List
   - Sales by Customer
   - Customer Transaction History
   - Aged Receivables by Customer
```

### Supplier Reports
```
1. Reports > Purchases Reports
   - Supplier List
   - Purchases by Supplier
   - Supplier Transaction History
   - Aged Payables by Supplier
```

### Custom Reports
```
1. Reports > Custom Reports
   - Create custom reports sesuai kebutuhan
   - Export to Excel/PDF
   - Schedule automatic reports
```

---

## 🔧 TROUBLESHOOTING

### Common Issues
```
1. Import Errors
   - Check CSV format
   - Verify column mapping
   - Review data validation

2. Balance Errors
   - Check opening balances
   - Review journal entries
   - Verify account types

3. Report Issues
   - Check date ranges
   - Verify account filters
   - Review report settings
```

### Support Resources
```
1. MYOB Help Center
2. MYOB Community Forum
3. Local MYOB Support
4. Online Tutorials
5. User Manual
```

---

## 📞 CONTACT INFORMATION

### MYOB Support
```
Website: www.myob.com
Phone: +61 3 9222 2555
Email: support@myob.com
Local Support: Check MYOB Indonesia website
```

### Technical Support
```
Installation: MYOB Installation Guide
Setup: MYOB Setup Wizard
Data Migration: MYOB Data Migration Tool
Backup: MYOB Backup & Restore Guide
```

---

## 📁 FILE STRUCTURE

```
📁 MULIA_MODISTE_MYOB_SETUP/
├── 📄 chart_of_accounts.csv
├── 📄 customer_cards.csv
├── 📄 supplier_cards.csv
├── 📄 item_service_list.csv
├── 📄 sample_transactions.csv
├── 📄 mulia_modiste_setup_guide.md
├── 📄 setup_instructions.txt
├── 📄 data_entry_guide.txt
└── 📄 troubleshooting_guide.txt
```

---

## ✅ CHECKLIST SETUP

- [ ] Install MYOB AccountRight
- [ ] Setup company information
- [ ] Import chart of accounts
- [ ] Import customer cards
- [ ] Import supplier cards
- [ ] Import item/service list
- [ ] Enter opening balances
- [ ] Enter sample transactions
- [ ] Generate trial balance
- [ ] Review financial reports
- [ ] Setup backup schedule
- [ ] Train users
- [ ] Go live

---

**Catatan:** Semua file CSV dan panduan ini dapat digunakan untuk setup MYOB MULIA MODISTE secara lengkap. Pastikan untuk backup data secara regular dan review setup sebelum go live. 