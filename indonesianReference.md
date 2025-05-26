## Nama
**Rafif Ahmad Yudhistira** (3124500045)

## Dosen Pengajar
**Dr Ferry Astika Saputra ST, M.Sc**

## 2.11. Soal-soal Latihan

### 2.11.1. Proses

#### Soal 3: Tindakan Kernel saat Alih Konteks
```plaintext
1. Simpan konteks proses lama (register, PC, status) ke PCB
2. Pilih proses baru dari ready queue
3. Muat konteks proses baru dari PCB ke CPU
4. Mulai eksekusi proses baru
```

#### Soal 4: Informasi dalam Tabel Proses
```plaintext
- Status proses (running/ready/waiting)
- Program Counter
- Nilai register CPU
- Informasi manajemen memori
- Informasi akunting (waktu CPU, ID proses)
- Status I/O (perangkat yang digunakan)
```

---

### 2.11.2. Thread

#### Soal 3: Perbedaan User vs Kernel Thread
| Aspek                  | User-Level Thread                  | Kernel-Level Thread                     |
|------------------------|------------------------------------|-----------------------------------------|
| Pengelolaan            | Oleh library di user space         | Oleh kernel                             |
| Efisiensi Context Switch | Cepat, tanpa syscall               | Lambat, perlu syscall                   |
| Cocok digunakan saat   | Proses ringan dan tidak block I/O  | Proses blocking I/O dan multiprosesor   |

#### Soal 4: Alih Konteks Kernel Thread
```plaintext
1. Simpan state thread lama ke TCB
2. Pilih thread baru dari ready queue  
3. Muat state thread baru ke CPU
4. Lanjutkan eksekusi (tanpa ubah ruang memori)
```

---

### 2.11.3. Penjadualan CPU

#### Soal 3: Keuntungan Quantum Berbeda di Multilevel Queue
```plaintext
1. Prioritas tinggi: quantum kecil → respons cepat
2. Prioritas rendah: quantum besar → throughput tinggi
3. Minimalkan overhead context switch
4. Adaptif terhadap jenis proses (I/O vs CPU-bound)
```

#### Soal 4: Gantt Chart
**FCFS**  
`P1(0-10) → P2(10-11) → P3(11-13) → P4(13-14) → P5(14-19)`

**SJF**  
`P2(0-1) → P4(1-2) → P3(2-4) → P5(4-9) → P1(9-19)`

**Prioritas**  
`P2(0-1) → P5(1-6) → P1(6-16) → P3(16-18) → P4(18-19)`

**Round Robin (q=1)**  
`P1,P2,P3,P4,P5,P1,P3,P5,P1,P5,P1,P5,P1,P1,P1,P1,P1,P1`

#### Soal 5: Waktu Tunggu
| Algoritma   | P1 | P2 | P3 | P4 | P5 | Rata-rata |
|-------------|----|----|----|----|----|----------|
| **FCFS**    | 0  | 10 | 11 | 13 | 14 | 9.6 ms   |
| **SJF**     | 9  | 0  | 2  | 1  | 4  | 3.2 ms   |
| **Prioritas**| 6  | 0  | 16 | 18 | 1  | 8.2 ms   |
| **RR**      | 9  | 1  | 3  | 4  | 5  | 4.4 ms   |

---

