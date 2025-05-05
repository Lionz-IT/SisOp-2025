# Analisis FCFS Scheduling Algorithm (Dengan dan Tanpa Arrival Time)

## 1. **FCFS Tanpa Arrival Time**
### Penjelasan Algoritma
- **Asumsi**: Semua proses memiliki waktu kedatangan (arrival time) = 0.
- **Proses Eksekusi**: Proses dijalankan secara berurutan sesuai urutan input.
- **Perhitungan**:
  - **Completion Time (CT)** = Akumulasi Burst Time (BT).
  - **Turnaround Time (TAT)** = CT (karena AT dianggap 0).
  - **Waiting Time (WT)** = TAT - BT.
  - **Response Time (RT)** = WT (untuk FCFS non-preemptive).

### Contoh Output
![Image](https://github.com/user-attachments/assets/c9287856-d974-441a-9c9d-08b8ad2ad94a)

### Kelebihan dan Kekurangan
| **Kelebihan**                          | **Kekurangan**                          |
|----------------------------------------|-----------------------------------------|
| Sederhana dan mudah diimplementasikan. | Tidak realistis untuk kasus AT berbeda. |
| Cocok untuk proses yang datang bersamaan. | WT/TAT lebih tinggi karena eksekusi berurutan. |

---

## 2. **FCFS Dengan Arrival Time**
### Penjelasan Algoritma
- **Asumsi**: Proses memiliki waktu kedatangan (AT) yang berbeda.
- **Proses Eksekusi**:
  1. Proses diurutkan berdasarkan AT menggunakan **bubble sort**.
  2. CT dihitung dengan menambahkan BT ke CT sebelumnya.
  3. Jika proses berikutnya memiliki **AT > CT saat ini**, terjadi **bug** karena CT tidak diupdate ke `max(CT, AT)`.
- **Perhitungan**:
  - **TAT** = CT - AT.
  - **WT** = TAT - BT.

### Contoh Output
![Image](https://github.com/user-attachments/assets/eab716f5-14a8-4396-9e00-6a1998b2ebd1)
