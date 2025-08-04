# MYOB MULIA MODISTE SETUP PACKAGE

## 📋 OVERVIEW

Package lengkap untuk setup MYOB AccountRight untuk MULIA MODISTE, termasuk semua file CSV, panduan setup, dan instruksi data entry.

## 📁 FILE STRUCTURE

```
📁 MULIA_MODISTE_MYOB_SETUP/
├── 📄 chart_of_accounts.csv          # Chart of Accounts
├── 📄 customer_cards.csv             # Customer Cards
├── 📄 supplier_cards.csv             # Supplier Cards
├── 📄 item_service_list.csv          # Item/Service List
├── 📄 sample_transactions.csv        # Sample Transactions
├── 📄 mulia_modiste_setup_guide.md   # Comprehensive Setup Guide
├── 📄 setup_instructions.txt         # Step-by-step Setup Instructions
├── 📄 data_entry_guide.txt           # Data Entry Guide
└── 📄 README.md                      # This file
```

## 🎯 TARGET MYOB VERSION

**MYOB AccountRight v19.4 atau v20**
- Mendukung multi-currency (IDR)
- Fitur lengkap untuk small business
- Interface yang user-friendly
- Laporan keuangan yang komprehensif

## 📊 DATA SUMMARY

### **CUSTOMERS (2)**
1. **Pelanggan** - General customers untuk jasa jahit
2. **LIO TAILOR** - Specific customer untuk jasa obras

### **SUPPLIERS (8)**
1. **Toko MAJU** - Perlengkapan jahit dan rupa-rupa
2. **Toko BINTANG** - Mesin jahit dan peralatan
3. **Toko MEKAR** - Aneka perlengkapan rupa-rupa
4. **PDAM dan PLN** - Tagihan air dan listrik
5. **Surianto** - Sewa kios
6. **Suminah** - Jasa penjahit (karyawan)
7. **Anton Servis** - Servis mesin jahit
8. **Jamal** - Iuran keamanan dan kebersihan

### **CHART OF ACCOUNTS (25)**
- **Assets (9 accounts)**
- **Liabilities (4 accounts)**
- **Equity (3 accounts)**
- **Income (2 accounts)**
- **Expenses (7 accounts)**

### **ITEMS/SERVICES (12)**
- **Services (2 items)**
- **Assets (4 items)**
- **Expenses (6 items)**

### **SAMPLE TRANSACTIONS (28)**
- Cash Inflows (6 transactions)
- Cash Outflows (8 transactions)
- Sales Invoices (2 transactions)
- Purchase Bills (4 transactions)
- Journal Entries (8 transactions)

## 🚀 QUICK START

### **Step 1: Install MYOB**
```bash
# Download MYOB AccountRight v19.4/v20
# Install sesuai sistem operasi
# Aktivasi lisensi
```

### **Step 2: Setup Company**
```bash
# Buka MYOB AccountRight
# Create new company file
# Masukkan informasi MULIA MODISTE
# Set currency: IDR
# Set financial year: 1 Maret - 28 Februari
```

### **Step 3: Import Data**
```bash
# Import chart_of_accounts.csv
# Import customer_cards.csv
# Import supplier_cards.csv
# Import item_service_list.csv
```

### **Step 4: Enter Transactions**
```bash
# Enter opening balances
# Enter sample transactions dari sample_transactions.csv
# Verify trial balance
```

## 📖 DETAILED GUIDES

### **1. Setup Guide (`mulia_modiste_setup_guide.md`)**
- Informasi perusahaan lengkap
- Chart of accounts detail
- Customer dan supplier details
- Item/service list
- Sample transactions
- Setup instructions
- Data entry guide
- Report generation
- Troubleshooting

### **2. Setup Instructions (`setup_instructions.txt`)**
- Step-by-step setup process
- Import procedures
- Verification steps
- Backup procedures
- User training
- Go live checklist

### **3. Data Entry Guide (`data_entry_guide.txt`)**
- Cash inflow procedures
- Cash outflow procedures
- Sales invoice procedures
- Purchase bill procedures
- Journal entry procedures
- Payment recording
- Adjusting entries
- Closing entries
- Data validation
- Error handling
- Backup procedures
- Report generation
- Security measures
- Maintenance procedures
- Troubleshooting
- Best practices

## 📊 CSV FILES EXPLANATION

### **1. chart_of_accounts.csv**
```csv
Account Number,Account Name,Account Type,Description,Tax Code
1-101,Kas,Asset,Cash on hand,-
1-102,Piutang Usaha,Asset,Accounts Receivable,-
...
```
**Columns:**
- `Account Number`: Nomor akun (1-101, 1-102, dll)
- `Account Name`: Nama akun (Kas, Piutang Usaha, dll)
- `Account Type`: Tipe akun (Asset, Liability, Equity, Income, Expense)
- `Description`: Deskripsi akun dalam bahasa Inggris
- `Tax Code`: Kode pajak (kosong untuk semua)

### **2. customer_cards.csv**
```csv
Card Name,Card Type,Address,Phone,Email,Payment Terms,Default Account,Notes
Pelanggan,Customer,Jl. Adisucipto No. 1A Sungai Raya,(0561) 712345,muliamodiste@gmail.com,Cash,4-101,General customers for sewing services
LIO TAILOR,Customer,Jl. Adisucipto Kompl Sakura Permai No 14 Sungai Raya,0561-6122223,lio.tailor@email.com,n/15,4-102,Embroidery services customer
```
**Columns:**
- `Card Name`: Nama customer
- `Card Type`: Tipe card (Customer)
- `Address`: Alamat customer
- `Phone`: Nomor telepon
- `Email`: Alamat email
- `Payment Terms`: Syarat pembayaran (Cash, n/15)
- `Default Account`: Account default untuk revenue
- `Notes`: Catatan tambahan

### **3. supplier_cards.csv**
```csv
Card Name,Card Type,Address,Phone,Email,Payment Terms,Default Account,Notes
Toko MAJU,Supplier,Jl. Djuanda No 2 Pontianak,(0561) 888 666,maju@email.com,n/15,2-101,Supplies sewing materials
...
```
**Columns:**
- `Card Name`: Nama supplier
- `Card Type`: Tipe card (Supplier)
- `Address`: Alamat supplier
- `Phone`: Nomor telepon
- `Email`: Alamat email
- `Payment Terms`: Syarat pembayaran
- `Default Account`: Account default untuk payable
- `Notes`: Catatan tambahan

### **4. item_service_list.csv**
```csv
Item Number,Item Name,Item Type,Description,Unit Price,Account,Notes
JHT001,Jasa Jahit,Service,Sewing services for customers,150000,4-101,Per piece/item
...
```
**Columns:**
- `Item Number`: Nomor item (JHT001, OBR001, dll)
- `Item Name`: Nama item
- `Item Type`: Tipe item (Service, Asset, Expense)
- `Description`: Deskripsi item
- `Unit Price`: Harga per unit
- `Account`: Account yang terkait
- `Notes`: Catatan tambahan

### **5. sample_transactions.csv**
```csv
Date,Transaction Type,Reference,Card Name,Account,Description,Amount,Debit Account,Credit Account
01/03/2019,Cash Outflow,KK-01,Surianto,5-102,Sewa kios untuk 3 bulan (Maret - Mei 2019),900000,5-102,1-101
...
```
**Columns:**
- `Date`: Tanggal transaksi (DD/MM/YYYY)
- `Transaction Type`: Tipe transaksi (Cash Outflow, Cash Inflow, Purchase, Sales Invoice, Journal Entry)
- `Reference`: Nomor referensi (KK-01, KM-03, dll)
- `Card Name`: Nama customer/supplier
- `Account`: Account yang terkait
- `Description`: Deskripsi transaksi
- `Amount`: Jumlah transaksi
- `Debit Account`: Account yang didebit
- `Credit Account`: Account yang dikredit

## 🔧 IMPORT PROCEDURES

### **Chart of Accounts Import**
1. Buka menu "Accounts" > "Accounts List"
2. File > Import > Chart of Accounts
3. Pilih file `chart_of_accounts.csv`
4. Map columns sesuai format
5. Klik "Import"

### **Customer Cards Import**
1. Buka menu "Card File" > "Cards List"
2. Pilih tab "Customer"
3. File > Import > Customer Cards
4. Pilih file `customer_cards.csv`
5. Map columns sesuai format
6. Klik "Import"

### **Supplier Cards Import**
1. Buka menu "Card File" > "Cards List"
2. Pilih tab "Supplier"
3. File > Import > Supplier Cards
4. Pilih file `supplier_cards.csv`
5. Map columns sesuai format
6. Klik "Import"

### **Item/Service List Import**
1. Buka menu "Sales" > "Items"
2. File > Import > Item List
3. Pilih file `item_service_list.csv`
4. Map columns sesuai format
5. Klik "Import"

## 💰 OPENING BALANCES

### **Assets**
- Kas: Rp 12,500,000
- Sewa Kios Dibayar Dimuka: Rp 900,000
- Perlengkapan Jahit: Rp 100,000
- Perlengkapan Rupa-Rupa: Rp 40,000
- Peralatan Jahit: Rp 2,750,000
- Peralatan Rupa-Rupa: Rp 500,000

### **Liabilities**
- Utang Bank: Rp 7,500,000

### **Equity**
- Modal Ny. Mulia: Rp 5,000,000

## 📈 SAMPLE TRANSACTIONS SUMMARY

### **Cash Inflows (6 transactions)**
- Total: Rp 4,250,000
- Sources: Pelanggan (4), LIO TAILOR (2)

### **Cash Outflows (8 transactions)**
- Total: Rp 1,700,000
- Recipients: Surianto, PDAM dan PLN, Suminah, Anton Servis, Ny. Mulia, Jamal

### **Sales Invoices (2 transactions)**
- Total: Rp 350,000
- Customer: LIO TAILOR

### **Purchase Bills (4 transactions)**
- Total: Rp 3,250,000
- Suppliers: Toko BINTANG, Toko MAJU, Toko MEKAR

### **Journal Entries (8 transactions)**
- Total adjustments: Rp 1,540,000
- Types: Accrued revenue, accrued expenses, depreciation, loan payments, wages, supplies

## 📊 REPORTS AVAILABLE

### **Financial Reports**
- Profit & Loss Statement
- Balance Sheet
- Cash Flow Statement
- Statement of Owner's Equity

### **Management Reports**
- Aged Receivables
- Aged Payables
- Sales Register
- Purchases Register
- General Ledger

### **Customer Reports**
- Customer List
- Sales by Customer
- Customer Transaction History
- Aged Receivables by Customer

### **Supplier Reports**
- Supplier List
- Purchases by Supplier
- Supplier Transaction History
- Aged Payables by Supplier

## 🔒 SECURITY & BACKUP

### **Backup Procedures**
1. Manual Backup: File > Backup
2. Automatic Backup: Set schedule
3. Test Restore: Verify backup integrity

### **Security Measures**
1. User Access Control
2. Password Protection
3. Data Encryption
4. Access Logging

## 🆘 SUPPORT & TROUBLESHOOTING

### **Common Issues**
1. **Import Errors**: Check CSV format, verify column mapping
2. **Balance Errors**: Review opening balances, check journal entries
3. **Report Issues**: Check date ranges, verify account filters
4. **Performance Issues**: Optimize database, regular maintenance

### **Support Resources**
1. MYOB Help Center: help.myob.com
2. MYOB Community Forum: community.myob.com
3. Local MYOB Support: Check MYOB Indonesia website
4. Online Tutorials: MYOB Learning Center

## ✅ CHECKLIST

### **Setup Checklist**
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

### **Data Entry Checklist**
- [ ] Basic navigation
- [ ] Data entry procedures
- [ ] Report generation
- [ ] Backup procedures
- [ ] Error handling
- [ ] Security measures
- [ ] Troubleshooting
- [ ] Best practices

## 📞 CONTACT INFORMATION

### **MYOB Support**
- Website: www.myob.com
- Phone: +61 3 9222 2555
- Email: support@myob.com
- Local Support: Check MYOB Indonesia website

### **Technical Support**
- Installation: MYOB Installation Guide
- Setup: MYOB Setup Wizard
- Data Migration: MYOB Data Migration Tool
- Backup: MYOB Backup & Restore Guide

## 📝 NOTES

1. **Currency**: Semua transaksi dalam IDR (Indonesian Rupiah)
2. **Date Format**: DD/MM/YYYY
3. **Amount Format**: Tanpa koma ribuan (150000 bukan 150,000)
4. **Backup**: Lakukan backup secara regular
5. **Training**: Pastikan user terlatih sebelum go live
6. **Support**: Siapkan prosedur support dan troubleshooting

## 🎯 GO LIVE PREPARATION

1. **Review Setup**: Pastikan semua data terimport dengan benar
2. **Test Transactions**: Verifikasi semua transaksi sample
3. **Generate Reports**: Review laporan keuangan
4. **Backup Data**: Backup data terakhir sebelum go live
5. **Train Users**: Pastikan semua user terlatih
6. **Monitor**: Monitor sistem setelah go live

---

**Catatan**: Package ini menyediakan semua yang diperlukan untuk setup MYOB MULIA MODISTE secara lengkap. Pastikan untuk review semua data sebelum go live dan backup secara regular. # readje
