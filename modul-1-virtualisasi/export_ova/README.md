# 🗂️ README – Kali Linux OVA

## 📌 Overview
File ini berisi dokumentasi pembuatan **Kali Linux OVA** 
OVA dibuat dari instalasi fresh Kali Linux dan hanya berisi dua kustomisasi:

- Update & upgrade sistem  
- Instalasi Tor Browser  

OVA digunakan sebagai contoh bagaimana saya membuat *pre-configured virtual machine* untuk kebutuhan lab keamanan siber.

---

## 🚀 1. Proses Pembuatan OVA

### 1. Buat VM Baru
Menggunakan VirtualBox:

1. New → Name: `Kali Linux`
2. Type: Linux, Version: Debian (6464-bit)
3. Memory: 4096MB  
4. CPU: 4 cores  
5. Disk: 80GB (VDI, dynamically allocated)

---

### 2. Instal Kali Linux
1. Boot ISO Kali Linux  
2. Pilih *Graphical Install*  
3. Konfigurasi user & regional  
4. Instalasi hingga selesai  
5. Login ke desktop

---

### 3. Lakukan Kustomisasi

#### Update & upgrade
```
sudo apt update && sudo apt upgrade -y
```

#### Install Tor Browser

##### Download Tor Browser di (www.torproject.org)

```
# Masuk ke folder Downloads
cd ~/Downloads

# Extract file
tar -xvf [nama file tor]

# Jalankan Tor Browser
./start-tor-browser.desktop

```

---

### 4. Bersihkan Cache
```
sudo apt autoremove -y
sudo apt clean
```

---

### 5. Shutdown VM
Pastikan dalam kondisi **Power Off**, bukan suspended.

---

### 6. Export OVA
Via VirtualBox:

1. File → Export Appliance  
2. Pilih VM  
3. Format: **OVA 1.0**  
4. Filename: `kali Linux.ova`  
5. Finish  

Screenshot proses export ada pada folder ini.

---

## 📁 Folder Contents
```
export_ova
├── README.md
├── export-proses.png
├── export-hasil.png
└── file-info.txt
```

---

## 📄 file-info.txt (Contoh Isi)
```
File Name: kali-portfolio-minimal.ova
Size: 13.6 GB
Created: 02-Desember-2025
Description: Kali Linux fresh install + update/upgrade + Tor Browser
Hypervisor: VirtualBox 7.x
```

---

## 2. Cara Menggunakan OVA (Import Appliance)

1. Buka VirtualBox  
2. File → Import Appliance  
3. Pilih `kali Linux.ova`  
4. Next  
5. Sesuaikan resource (optional)  
6. Import  

VM siap digunakan.

---

