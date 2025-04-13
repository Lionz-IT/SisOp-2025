# Contoh Program Multithreading di C dengan `pthread`

Program ini menunjukkan cara membuat tiga thread yang mencetak angka "1", "2", dan "3" secara konkuren menggunakan pustaka `pthread`.

## Kode Program print123thread.c
```c
#include <stdio.h>
#include <stdlib.h>
#include <pthread.h>

void *print1(void *arg) {
    printf("1\n");
    return NULL;
}

void *print2(void *arg) {
    printf("2\n");
    return NULL;
}

void *print3(void *arg) {
    printf("3\n");
    return NULL;
}

int main() {
    pthread_t t1, t2, t3;

    pthread_create(&t1, NULL, print1, NULL);
    pthread_create(&t2, NULL, print2, NULL);
    pthread_create(&t3, NULL, print3, NULL);

    pthread_join(t1, NULL);
    pthread_join(t2, NULL);
    pthread_join(t3, NULL);

    return 0;
}
```

## Penjelasan
### 1. Fungsi Thread
- **`print1`**, **`print2`**, **`print3`**: Masing-masing fungsi mencetak angka "1", "2", atau "3" ke layar.

### 2. Pembuatan Thread
- `pthread_create()`: Digunakan untuk membuat thread baru.
  ```c
  pthread_create(&t1, NULL, print1, NULL); // Membuat thread t1
  ```

### 3. Menunggu Thread Selesai
- `pthread_join()`: Memastikan thread utama (program) menunggu semua thread selesai.
  ```c
  pthread_join(t1, NULL); // Menunggu thread t1
  ```

## Output
Urutan output **tidak tetap** karena thread dijalankan secara paralel. Contoh output:
```
1
3
2
```
atau
```
2
1
3
```

## Cara Menjamin Urutan
Untuk mencetak "1", "2", lalu "3" secara berurutan, gunakan `pthread_join()` setelah setiap thread dibuat:
```c
int main() {
    pthread_t t1, t2, t3;

    pthread_create(&t1, NULL, print1, NULL);
    pthread_join(t1, NULL); // Tunggu t1

    pthread_create(&t2, NULL, print2, NULL);
    pthread_join(t2, NULL); // Tunggu t2

    pthread_create(&t3, NULL, print3, NULL);
    pthread_join(t3, NULL); // Tunggu t3

    return 0;
}
```


