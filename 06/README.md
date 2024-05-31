1. Jelaskan beberapa contoh fungsi aktivasi
   
   fungsi aktivasi = Komponen penting dalam jaringan saraf tiruan ( neural network) yg memperkenalkan non- linearitas ke dalam model, memungkinkan jaringan untuk belajar dan mempresentasikan data yang lebih kompleks.

   non linearitas yang di maksud adalah sistem yg perubahan keluarannya tidak sebanding dengan perubahan masukkan.
   
non - linearitas dalam model aktivasi adlaah : keluaran pada unit manapun tidak dapat diproduksi darri fungsi masukan yang linier.

contoh beberapa fuungsi aktivasi :

a.) sigmoid
fungsi ini utk memetakan nilai ke dalam rentang 0-1

![image](https://github.com/mymyid/kelas/assets/164980491/2a46f450-7ae8-4b96-8ebe-d2f4d2f45094)


    kelebihan:
    memetakkan input menjadi rentang antara  0 - 1 sehingga cocok utk model probabilitas.

    kelemahan:
    menderita masalah varishing gradient pada lapisan yg lebih dalam, yg membuat pelatihan jaringan menjadi sulit. 

    b.) Tan H (Hiperbolic Tangent)
    Fungsi ini mirip dengan fungsi sigmoid, hanya saja fungsi ini memetakan nilai input ke dalam rentang -1 hingga 1.

![image](https://github.com/mymyid/kelas/assets/164980491/716cda0e-b7a5-4fa2-a9a9-7a9f7330353b)


    kelebihan : 
    memetakkan input menjadi rentang antara -1 dan 1,, yg sering kali menghasilkan konvergensi lebih cepat daripada sigmoid. 

    kekurangan:
sama seperti sigmoid,tan h juga mengalami vanishing gradient. 

c.) ReLU (Rectified Linear Unit) 
Fungsi ReLU melakukan operasi ambang batas pada setiap elemen masukan di mana semua nilai yang kurang dari nol disetel ke nol. 

kelebihan : 
mengatasi masalah vanishing Gradient 
dengan baik dan sangat populer karna konvergensinya cepat. 

kekurangan: 
dapat menyebabkab " dead neurons" dimana neurons berhenti memperbaharui karena gradien nol. 

![image](https://github.com/mymyid/kelas/assets/164980491/f04a7f19-e7d2-4eef-a7e3-d97af3609a8d)


d.) Leaky ReLU

LeakyReLU merupakan fungsi aktivasi luas dari fungsi aktivasi ReLU. Perbedaan dari ReLU dan LeakyReLU adalah dalam model pemetaan nilai inputnya. Jika ReLU akan memetaan dalam rentang 0 hingga x, tetapi jika LeakyReLU tidak terbatas (y=x*0,01).

![image](https://github.com/mymyid/kelas/assets/164980491/954d9f08-c5c6-43a1-95e8-29dfce2d1349)

![image](https://github.com/mymyid/kelas/assets/164980491/037cf8f2-c56e-42cc-93a3-f47ff225d231)



kelebihan : 
mengatasi maslah  " dead neurons" dngan memberikan gradien kecil utk nilai negatif.

kekurangan: perlu memilih konstanta leak yang optimal, biasanya dipilih secara ad-hoc. 

e.) softmax

digunakan dalam jaringan saraf untuk menghitung distribusi probabilitas dari vektor bilangan real. Fungsi ini menghasilkan keluaran yang berkisar antara nilai 0 dan 1 dan dengan jumlah probabilitas sama dengan 1.

kelebihan: mengubah output menajdi distribusi probabilitas yg totallnya 1, sering digunakan pada lapisan output utk klasifikasi multikelas

kekurangan : 
dapat mengalami maslah numeric overflow / underflow pd input yg snagat besar / snagat kecil. 

![image](https://github.com/mymyid/kelas/assets/164980491/51ecb503-c446-4d7e-a6be-99b766c1a69d)

![image](https://github.com/mymyid/kelas/assets/164980491/e6cc7d93-fa93-4fd9-a705-959903778a62)


f.) swish 

Fungsi aktivasi Swish adalah pemain kunci dalam pembelajaran mendalam dan membedakan dirinya dari fungsi aktivasi lainnya dalam beberapa cara.  Swish menonjol sebagai fungsi aktivasi yang efektif dan efisien yang dapat menangani data kompleks dengan mudah dan menghindari masalah umum pada fungsi aktivasi lainnya.

kelebihan : 
ditemukan secara otomatis melalui pencarian arsitektur neural, sering menghasilkan performa yang lebih baik dubandingkan ReLU dan fungsi Aktivasi lainnya pada beberapa tugas. 

kekurangan :

leboh kompleks dalam perhitungan dibandingkan dengan ReLU, namun seringkali sepadan dngan peningkatan performa. 

![image](https://github.com/mymyid/kelas/assets/164980491/d8011876-6050-4b78-aa18-818df4c25492)


![image](https://github.com/mymyid/kelas/assets/164980491/12b69bdc-c9fd-44b1-b982-7d54c5a20a46)



2. Coba gambarkan dan jelaskan beberapa arsitektur berikut:
   
   a. GAN
Generative Adversarial Network (GAN) adalah jenis arsitektur jaringan saraf tiruan yang terdiri dari dua bagian utama: generator dan discriminator. Keduanya beroperasi dalam suatu siklus pelatihan yang iteratif, di mana generator mencoba membuat data semirip mungkin dengan data nyata, sementara discriminator berusaha membedakan antara data yang dihasilkan oleh generator dan data nyata.


![image](https://github.com/mymyid/kelas/assets/164980491/756da321-ff4a-46de-864d-96be7633096c)


Kelebihan Generative Adversarial Network (GAN):
- Fleksibilitas dalam Pembuatan Data:

- Pemahaman Konten dan Stil:

- Pembelajaran Tanpa Pengawasan:

- Peningkatan Kreativitas:

- Aplikasi di Berbagai Bidang:



   b. AE

   Autoencoder adalah jenis arsitektur jaringan saraf yang dirancang untuk secara efisien mengompresi (encode) data input hingga ke fitur-fitur esensialnya, kemudian merekonstruksi (decode) input asli dari representasi yang dikompresi ini.

  ![WhatsApp Image 2024-05-31 at 12 33 01_6f37c0a3](https://github.com/mymyid/kelas/assets/164980491/0ab23457-b1e8-40c3-8ef5-9f8eaf5cd5d9)

  contoh penggunaan Autoencoder:

  * kompresi data
  * pengurangan dimensi
  * deteksi anomali dan pengenalan wajah
  * denoising gambar dan denoising audio
  * Rekosntruksi gambar
  * Tugas Generatif

  
   c. LSTM

  LSTM merupakan modifikasi dari RNN yang memiliki memory dan banyak jenis gerbang yaitu input gate, forget gate, dan output gate. LSTM mampu mempelajari lebih dari 1000 langkah sebelumnya tergantung pada kompleksitas jaringan.

![image](https://github.com/mymyid/kelas/assets/164980491/b86a9c7a-db14-4266-b583-1f0409465d2b)

   
   d. VGG
   
VGG adalah singkatan dari Visual Geometry Group; ini adalah arsitektur Convolutional Neural Network (CNN) standar dalam dengan banyak lapisan. Yang “dalam” mengacu pada jumlah lapisan dengan VGG-16 atau VGG-19 yang terdiri dari 16 dan 19 lapisan konvolusional.

Arsitektur VGG adalah dasar dari model pengenalan objek yang inovatif. Dikembangkan sebagai jaringan neural dalam, VGGNet juga melampaui garis dasar dalam banyak tugas dan kumpulan data di luar ImageNet . Selain itu, saat ini arsitektur ini masih menjadi salah satu arsitektur pengenalan gambar yang paling populer. 

![image](https://github.com/mymyid/kelas/assets/164980491/08a15214-93cb-40ea-8e09-9350daef1762)

![image](https://github.com/mymyid/kelas/assets/164980491/dea07f3e-42ac-4ad8-9b7a-6e167fecfd68)

![image](https://github.com/mymyid/kelas/assets/164980491/651c7e73-7065-4165-ac6d-854cd8c86380)


   e RNN
   
   RNN (Recurrent Neural Network) adalah salah satu jenis arsitektur ANN yang digunakan untuk memproses data urutan atau rangkaian, seperti teks, audio, atau data waktu. RNN memiliki kemampuan untuk mengingat informasi dari waktu sebelumnya dan menggunakan informasi itu untuk menghasilkan output pada waktu saat ini.
   
   ![image](https://github.com/mymyid/kelas/assets/164980491/15337fde-7e78-4db8-b8e7-a7c16f3ef359)

   
3. Buatkan kodingan from scracth NN

buat folder pada Visual Code dengan nama simple_neural_network.py

```
import numpy as np

# Fungsi aktivasi (sigmoid)
def sigmoid(x):
    return 1 / (1 + np.exp(-x))

# Turunan dari fungsi sigmoid untuk backpropagation
def sigmoid_derivative(x):
    return x * (1 - x)

# Inisialisasi parameter
input_layer_neurons = 3   # Jumlah neuron di lapisan input (sesuai dengan fitur input)
hidden_layer_neurons = 4  # Jumlah neuron di lapisan tersembunyi
output_neurons = 1        # Jumlah neuron di lapisan output (sesuai dengan target output)

# Inisialisasi bobot dengan nilai acak
weights_input_hidden = np.random.uniform(size=(input_layer_neurons, hidden_layer_neurons))
weights_hidden_output = np.random.uniform(size=(hidden_layer_neurons, output_neurons))

# Definisikan learning rate
learning_rate = 0.5

# Input data (4 sampel dengan 3 fitur)
X = np.array([[0, 0, 1],
              [1, 1, 1],
              [1, 0, 1],
              [0, 1, 1]])

# Target output
y = np.array([[0], [1], [1], [0]])

# Training process
for epoch in range(10000):
    # Feedforward
    hidden_layer_input = np.dot(X, weights_input_hidden)
    hidden_layer_output = sigmoid(hidden_layer_input)
    
    output_layer_input = np.dot(hidden_layer_output, weights_hidden_output)
    predicted_output = sigmoid(output_layer_input)
    
    # Backpropagation
    error = y - predicted_output
    d_predicted_output = error * sigmoid_derivative(predicted_output)
    
    error_hidden_layer = d_predicted_output.dot(weights_hidden_output.T)
    d_hidden_layer = error_hidden_layer * sigmoid_derivative(hidden_layer_output)
    
    # Update bobot
    weights_hidden_output += hidden_layer_output.T.dot(d_predicted_output) * learning_rate
    weights_input_hidden += X.T.dot(d_hidden_layer) * learning_rate

# Output hasil training
print("Output setelah training:")
print(predicted_output)
```
![WhatsApp Image 2024-05-31 at 13 00 27_ab3a9982](https://github.com/mymyid/kelas/assets/164980491/bbf652bf-024a-41bf-8e1c-45507ee46976)

