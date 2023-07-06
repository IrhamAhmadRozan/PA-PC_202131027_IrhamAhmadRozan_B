# PA-PC_202131027_IrhamAhmadRozan_B
Projek UAS Pengolahan Citra

## Remove Background Teori

Penghapusan latar belakang atau background removal adalah proses dalam pengolahan citra yang bertujuan untuk menghilangkan latar belakang atau elemen-elemen yang tidak diinginkan dari suatu gambar, sehingga fokus utama pada gambar menjadi lebih menonjol. Proses ini biasanya dilakukan dalam konteks pengolahan citra komputer, desain grafis, pengenalan pola, dan aplikasi-aplikasi lainnya.

Terdapat beberapa metode umum yang digunakan dalam penghapusan latar belakang:

1. Metode berbasis Ambang (Threshold-based Method):
   - Metode Thresholding: Metode ini melibatkan penggunaan ambang batas untuk memisahkan piksel objek dan latar belakang. Dengan mengubah gambar menjadi citra biner menggunakan ambang batas yang sesuai, piksel yang melebihi ambang batas dianggap sebagai bagian objek, sementara piksel yang kurang dari ambang batas dianggap sebagai latar belakang.
   - Metode Adaptive Thresholding: Metode ini serupa dengan metode thresholding, tetapi ambang batasnya disesuaikan secara adaptif berdasarkan karakteristik lokal di sekitar setiap piksel. Hal ini memungkinkan penyesuaian yang lebih baik terhadap variasi intensitas dalam citra.

2. Metode berbasis Segmentasi:
   - Metode Segmentasi Berdasarkan Pewarnaan (Color-based Segmentation): Metode ini memisahkan objek dan latar belakang berdasarkan perbedaan warna. Pada citra berwarna, ruang warna seperti RGB atau HSV digunakan untuk menentukan batasan warna antara objek dan latar belakang.
   - Metode Segmentasi Berbasis Tekstur (Texture-based Segmentation): Metode ini memanfaatkan perbedaan tekstur antara objek dan latar belakang. Fitur tekstur seperti filter Gabor, transformasi wavelet, atau matriks ko-occurance (co-occurrence matrix) dapat digunakan untuk membedakan antara objek dan latar belakang.

3. Metode berbasis Algoritma:
   - Metode GrabCut: Metode ini menggunakan algoritma iteratif yang menggabungkan penggunaan model warna dan perbaikan berulang untuk menghasilkan segmentasi yang lebih baik. Dalam metode ini, pengguna harus memberikan informasi awal mengenai wilayah objek dan wilayah latar belakang.
   - Metode Pembelajaran Mesin (Machine Learning-based Methods): Metode ini melibatkan penggunaan algoritma pembelajaran mesin seperti Support Vector Machines (SVM), Random Forest, atau Convolutional Neural Networks (CNN) untuk mempelajari dan memprediksi perbedaan antara objek dan latar belakang.

Pada projek UAS kali ini saya membuat menggunakan program Python, terdapat beberapa library yang saya gunakan untuk melakukan background removal, seperti OpenCV, PIL (Python Imaging Library), dan rembg. Berikut adalah penjelasan mengenai penggunaan beberapa library tersebut:

1. OpenCV:
OpenCV (Open Source Computer Vision Library) adalah library populer untuk pengolahan citra dan komputerisasi pandangan komputer. Library ini menyediakan berbagai fungsi dan algoritma yang kuat untuk memanipulasi citra, termasuk background removal. Dalam OpenCV, background removal dapat dilakukan dengan menggunakan metode pengolahan citra seperti segmentasi berbasis warna atau deteksi tepi. 

2. PIL (Python Imaging Library):
PIL (Python Imaging Library) atau juga dikenal sebagai Pillow adalah library Python yang digunakan untuk memanipulasi dan memproses citra. Meskipun tidak sekuat OpenCV dalam hal pengolahan citra, PIL cukup sederhana dan mudah digunakan.

3. rembg
Fungsi rembg adalah sebuah library Python yang digunakan untuk melakukan penghapusan latar belakang pada gambar menggunakan model deep learning berbasis neural network. Library ini memanfaatkan model deep learning yang dilatih untuk memisahkan objek dari latar belakang dengan akurasi yang tinggi.

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

### Save File Image

Kemudian saya melakukan penyimpanan file gambar yang sudah saya hapus latar belakangnya dengan format png yang diberikan nama 'output.png'. Tetapi sebelum itu saya harus meng-convert gambarnya terlebih dahulu ke RGB dan kemudian menghapus kembali latar belakangnya menggunakan library rembg.

## Jurnal Terkait

[ResearchGate - Autonomous image background removal for accurate and efficient close-range photogrammetry](https://www.researchgate.net/publication/365500074_Autonomous_image_background_removal_for_accurate_and_efficient_close-range_photogrammetry)

[CoreIT - Deteksi Obyek Manusia Pada Basis Data Video Menggunakan Metode Background Subtraction Dan Operasi Morfologi](https://ejournal.uin-suska.ac.id/index.php/coreit/article/view/2391/pdf)

## Sumber 

[PyPI - opencv-python 4.8.0.74](https://pypi.org/project/opencv-python/)

[edureka! - How To Install NumPy In Python?](https://www.edureka.co/blog/install-numpy/)

[finxter - PIP Install PIL/Pillow – A Helpful Illustrated Guide](https://blog.finxter.com/python-install-pil/)

[PyPI - rembg 2.0.49](https://pypi.org/project/rembg/)

[tutorialspoint - How to install matplotlib in Python?](https://www.tutorialspoint.com/how-to-install-matplotlib-in-python)

[tom's HARDWARE - How To Remove Backgrounds From Images With Python](https://www.tomshardware.com/how-to/python-remove-image-backgrounds)

[BelajarBukaCV - Deteksi Kontur menggunakan OpenCV](https://learnopencv.com/contour-detection-using-opencv-python-c/#What-are-Contours)

[Kaggle - OpenCV background removal](https://www.kaggle.com/code/vadbeg/opencv-background-removal)

[Kaggle - Plant Pathology, OpenCV Background Removal](https://www.kaggle.com/code/victorlouisdg/plant-pathology-opencv-background-removal)

[Medium - Background removal in images using OpenCV GrabCut algorithm](https://medium.datadriveninvestor.com/background-removal-in-images-using-opencv-grabcut-algorithm-f2a35949417c)
