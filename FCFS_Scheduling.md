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
|No| BT| CT| TAT| WT| RT|
|--|---|---|----|---|---|
|P1| 8 |8 |8 |0 |0|
|P2| 4 |12 |12| 8 |8|
|P3| 9 |21 |21 |12 |12|
|P4| 5 |26 |26 |21 |21|

Average TurnAroundTime=16.75
Average WaitingTime=10.25


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
## 1. Dengan Arrival Time
![Image](https://github.com/user-attachments/assets/eab716f5-14a8-4396-9e00-6a1998b2ebd1)
## 2. Tanpa Arrival Time
![Image](https://github.com/user-attachments/assets/c9287856-d974-441a-9c9d-08b8ad2ad94a)
