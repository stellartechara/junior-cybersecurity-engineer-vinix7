# 🖥️ Modul 01 – Virtualisasi

Modul ini berfokus pada instalasi berbagai platform virtualisasi, pembuatan VM, kustomisasi sistem operasi, export OVA/OVF, serta pemahaman konsep virtualisasi secara fundamental.

## 📌 1. Instalasi Tools Virtualisasi

Tools yang dicoba pada modul ini:
- VMware Workstation
- VirtualBox
- Proxmox
- Xen
- OpenStack (MicroStack)

Semua dokumentasi instalasi disimpan dalam folder `screenshots/`.

### ✔ Status Instalasi
| Tools                  | Status     | Folder Screenshot            |
|------------------------|------------|-------------------------------|
| VirtualBox             | ✔ Berhasil | screenshots/virtualbox/      |
| VMware                 | ✔ Berhasil | screenshots/vmware/          |
| Proxmox                | ✔ Berhasil   | screenshots/proxmox/         |
| Xen                    | ✔ Dicoba   | screenshots/xen/             |
| OpenStack/MicroStack   | ✔ Berhasil | screenshots/openstack/        |

## 📌 2. Pembuatan 2 Virtual Machine (Windows & Kali Linux)

VM dibuat menggunakan ISO installer masing-masing:

- Kali Linux

### 📎 Bukti Instalasi
Tersedia pada folder:
```
screenshots/
```

### 📎 Kustomisasi yang dilakukan:

**Kali Linux**
- Install Tor Browser
- Update & upgrade sistem

## 📌 3. Export OVA/OVF

Setelah konfigurasi selesai, VM diexport menjadi format OVA/OVF.

Folder export:
```
ova-export/
```

## 📌 4. Perbandingan Tools Virtualisasi

### VirtualBox
**Kelebihan:**
- Gratis & open-source
- Mudah digunakan

**Kekurangan:**
- Performa di bawah VMware

### VMware
**Kelebihan:**
- Stabil & performa tinggi

**Kekurangan:**
- Tidak sepenuhnya gratis

### Proxmox
**Kelebihan:**
- Mendukung cluster, backup, LXC

**Kekurangan:**
- Butuh hardware lebih kuat

### Xen
**Kelebihan:**
- Banyak dipakai untuk cloud skala besar

**Kekurangan:**
- Kompleks untuk pemula

### OpenStack/MicroStack
**KKelebihan:**
- Private cloud lengkap (Compute, Storage, Network)

**Kekurangan:**
- Instalasi kompleks & resource besar

## 📌 5. Penjelasan Istilah Virtualisasi

**Virtualisasi** – Menjalankan beberapa OS pada satu hardware fisik melalui hypervisor.  
**Host** – Mesin fisik yang menjalankan hypervisor.  
**Guest** – Sistem operasi yang berjalan sebagai VM.  
**Cloud** – Resource komputasi yang tersedia secara on‑demand.  
**Cluster** – Sekumpulan server yang bekerja sebagai satu sistem.  
**Node** – Server individual dalam cluster.  
**Backup** – Salinan data/VM untuk pemulihan.  
**Restore** – Mengembalikan data dari backup.  
**Snapshot** – Menyimpan kondisi VM pada satu waktu.  
**Suspend** – Menghentikan VM sementara tanpa reboot.

## 📁 Struktur Folder
```
modul-01-virtualisasi/
│
├── README.md
├── screenshots/
│   ├── virtualbox/
│   ├── vmware/
│   ├── proxmox/
│   ├── xen/
│   ├── openstack/
│   └── kali/
└── ova-export/
    └── kali/
```

## 📌 Catatan Tambahan
VM pada modul ini digunakan sebagai fondasi untuk modul cybersecurity lainnya seperti:
- Pentesting
- SIEM
- Digital Forensics
- Vulnerability Assessment
