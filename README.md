# PA-PC_202131027_IrhamAhmadRozan_B
Projek UAS Pengolahan Citra

# Remove Background

Remove background image menggunakan aplikasi Jupyter Notebook.

## Instalasi Library

Lakukan instalasi library terlebih dahulu pada Command Prompt atau Terminal kalian

```bash
  pip install opencv-python
  pip install numpy
  pip install Pillow
  pip install rembg
  pip install matplotlib
```

## Penjelasan Program

### Import library

Di sini saya mengimport beberapa library yang sudah saya install sebelumnya. Library yang saya masukkan adalah library yang saya butuhkan untuk me-remove background.

### Read and Show image

Di sini saya memasukkan gambar bernama 'object.jpg' yang sudah berada dalam satu folder. Di sini saya melakukan proses convert color image ke RGB, yang kemudian saya tampilkan gambarnya menggunakan library pyplot.

### Convert Image to Binary with Thresholding Method

Di sini saya melakukan convert image ke dalam binary menggunakan Thresholding Method. Akan tetapi sebelum saya meng-convert gambarnya saya melakukan convert dari gambar asli ke dalam grayscale.

### Contour from Binary, Mask, Contour Image on Mask

Di sini saya memproses gambar saya yang sudah menjadi binary untuk di-masking menggunakan deteksi kontur. Dengan menggunakan deteksi kontur ini, kita dapat mendeteksi batas objek, dan melokalkannya dengan mudah ke dalam sebuah gambar. Fungsi dari deteksi kontur ini adalah untuk mengganti atau merubah atau menghilangkan latar belakang pada suatu gambar.

### Merge the Original Images with Masks Using the Bitwise AND Operator

Di sini saya menggabungkan gambar asli dengan gambar yang di-masking dengan menggunakan operator AND. Kemudian saya menampilkan gambar yang sudah digabungkan tersebut, tetapi sebelum itu saya mengconvert hasil gabungan gambarnya ke RGB

### Remove Background

Di sini saya melakukan penghapusan latar belakang yang di mana akan menghilangkan latar belakang dari objek gambar yang saya ambil. Di sini saya menghapus latar belakang gambar menggunakan library rembg.

### Showing Original Image and Removed Background Image

Di sini saya hanya menampilkan perbedaan gambar antara gambar yang asli dengan gambar yang sudah saya hapus latar belakangnya.

#### Save File Image

Kemudian saya melakukan penyimpanan file gambar yang sudah saya hapus latar belakangnya dengan format png yang diberikan nama 'output.png'. Tetapi sebelum itu saya harus meng-convert gambarnya terlebih dahulu ke RGB dan kemudian menghapus kembali latar belakangnya menggunakan library rembg.
