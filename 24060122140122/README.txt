Muhammad Anugerah Ramadhan
24060122140180
Tugas 4&5

                                                  LIGHTNING

Pencahayaan adalah elemen penting dalam grafika komputer, memungkinkan kita menciptakan adegan virtual dengan tingkat realisme yang tinggi. Seperti dalam dunia nyata, pencahayaan dalam dunia virtual mempengaruhi cara kita melihat dan berinteraksi dengan objek. Mari kita lihat lebih dekat pentingnya pencahayaan, teknik implementasinya, dan bagaimana hal ini dapat digunakan untuk meningkatkan kualitas dan kedalaman adegan yang dirender.

Konsep Pencahayaan dalam Grafika Komputer
Pencahayaan dalam grafika komputer melibatkan simulasi bagaimana cahaya berinteraksi dengan objek dan permukaan dalam adegan virtual. Ini mencakup pemantulan, penyerapan, dan transmisi cahaya. Pencahayaan dapat membuat adegan terlihat realistis dengan menambahkan kedalaman dan dimensi. Ini juga memengaruhi suasana dan emosi yang dapat dibangkitkan oleh adegan tertentu.

Mengapa Pencahayaan Penting?
Pencahayaan memainkan peran penting dalam meningkatkan realisme dan imersi. Tanpa pencahayaan yang baik, adegan dapat terlihat datar dan kurang hidup. Dengan pencahayaan yang tepat, kita dapat menciptakan bayangan, sorotan, dan gradasi cahaya yang membantu menggambarkan bentuk dan tekstur objek. Pencahayaan juga membantu dalam memisahkan dan membedakan objek, menambahkan dimensi ekstra ke adegan.

Selain itu, pencahayaan berperan dalam menyampaikan suasana dan narasi. Lampu redup dengan warna hangat dapat memberikan kesan keintiman, sementara cahaya terang dan tajam dapat menciptakan suasana yang tegang atau dinamis. Dengan kata lain, pencahayaan tidak hanya tentang menampilkan objek dengan benar, tetapi juga tentang menciptakan pengalaman visual yang sesuai dengan konteks dan tujuan.

Teknik Implementasi Pencahayaan
Implementasi pencahayaan memerlukan pemahaman tentang matematika dan algoritma kompleks. Dalam grafika komputer, shader—kode yang berjalan di GPU untuk mengolah gambar—memegang peran kunci dalam mensimulasikan interaksi cahaya.

Pemantulan Spekular dan Pemantulan Difus
Pemantulan Spekular: Pemantulan ini terjadi pada permukaan yang halus, menciptakan sorotan yang terang dan tajam. Pemantulan spekular memberi efek mengkilap pada objek, yang bergantung pada sudut cahaya, sudut pandang, dan sifat permukaan.
Pemantulan Difus: Ini melibatkan penyebaran cahaya ke segala arah pada permukaan kasar. Pemantulan difus lebih merata dan memberikan efek pencahayaan yang lembut dan halus.
Dengan menggabungkan pemantulan spekular dan difus dalam shader, kita dapat meniru sifat pemantulan berbagai jenis bahan, dari logam hingga kain.

Simulasi Cahaya dalam Shader
Vertex Shader: Di sini, posisi vertex dan normal dihitung dan ditransformasikan ke dalam ruang kamera. Langkah ini penting untuk memastikan bahwa perhitungan pencahayaan dilakukan dengan benar.
Shader Fragmen: Di sinilah pemantulan difus dan spekular dihitung berdasarkan sudut insiden, jarak ke sumber cahaya, dan sifat permukaan. Perhitungan ini melibatkan penggunaan fungsi-fungsi matematika yang kompleks untuk mensimulasikan bagaimana cahaya bergerak dan memantul dalam adegan.
Cahaya Ambien
Cahaya ambien adalah komponen pencahayaan tidak langsung yang memberikan nuansa lembut pada adegan, mengurangi bayangan yang keras, dan menambah kohesi visual. Dengan menyertakan cahaya ambien, adegan terasa lebih alami dan seimbang.

- Pencahayaan dalam Grafika: Memahami, Mengimplementasikan, dan Mensimulasikan
Pencahayaan memainkan peran fundamental dalam ranah grafika komputer, dengan rumitnya menyatukan realisme ke dalam dunia 
virtual dan meningkatkan pengalaman visual. Dalam esai ini, kita akan menyelami inti dari pencahayaan - apa itu, mengapa 
itu tak tergantikan, dan bagaimana cara mengimplementasikannya - menggali wawasan dari prinsip-prinsip cahaya dan 
simulasi dalam shader.

- Apa itu Pencahayaan?
Pada intinya, pencahayaan dalam grafika mencakup simulasi tentang bagaimana cahaya berinteraksi dengan permukaan dalam 
lingkungan virtual. Ini mencakup pemantulan, penyerapan, dan transmisi sinar cahaya, meniru fenomena dunia nyata untuk 
menciptakan adegan yang menarik secara visual. Sama seperti dalam dunia fisik, cahaya dalam grafika dapat menunjukkan 
berbagai perilaku saat bertemu permukaan, termasuk pemantulan spekular dan pemantulan difus.

- Mengapa Mengimplementasikan Pencahayaan?
Implementasi pencahayaan berperan sebagai batu penjuru dalam pengejaran keterampilan visual dan imersi dalam ruang 
virtual. Dengan menduplikasi interaksi antara cahaya dan permukaan secara akurat, pencahayaan memberi nafas pada adegan 
digital, memberikannya kedalaman, tekstur, dan realisme. Melalui pencahayaan, seniman dan pengembang dapat membangkitkan 
emosi, menetapkan suasana, dan menyampaikan narasi, memperkaya pengalaman pengguna dan memupuk keterlibatan.

Selain itu, pencahayaan memainkan peran kunci dalam meningkatkan persepsi bentuk, bentuk, dan tekstur, memungkinkan 
penonton untuk membedakan detail-detail rumit dan menghargai nuansa lingkungan virtual. Baik dalam game, visualisasi 
arsitektur, atau rendering sinematik, integrasi pencahayaan meningkatkan kualitas gambar yang dihasilkan komputer, 
memudarkan batas antara dunia nyata dan virtual.

- Bagaimana Cara Mengimplementasikan Pencahayaan?

Implementasi pencahayaan melibatkan permainan algoritma yang rumit, matematika, dan teknik pemrograman grafis. Dalam 
ranah shader, khususnya shader fragmen, simulasi pemantulan dan pencahayaan terungkap.

- Pemantulan Spekular dan Pemantulan Difus:
Pemantulan spekular, yang ditandai dengan pemantulan cahaya seperti cermin, terjadi terutama pada permukaan halus. 
Sebaliknya, pemantulan difus melibatkan penyebaran cahaya ke segala arah saat bertemu permukaan kasar. Dengan memasukkan 
fenomena ini ke dalam shader, pengembang dapat meniru beragam sifat pemantulan dari bahan, memperkaya kualitas visual 
adegan yang dirender.

- Mensimulasikan Cahaya dalam Shader:
Dalam pipa shader, vertex shader berfungsi sebagai pelopor perhitungan pencahayaan, mentransformasikan posisi vertex dan 
normal ke dalam ruang kamera. Selanjutnya, dalam shader fragmen, perhitungan rumit pemantulan difus dan spekular terungkap.

- Pemantulan Difus:
Simulasi pemantulan difus melibatkan perhitungan kompleks, memasukkan faktor-faktor seperti sudut insiden dan jarak ke 
sumber cahaya. Dengan memodelkan interaksi antara sinar cahaya dan normal permukaan, shader dapat menentukan intensitas 
dan warna pemantulan difus, berkontribusi pada pencahayaan keseluruhan objek virtual.

- Pemantulan Spekular:
Pemantulan spekular, di sisi lain, melibatkan perhitungan sinar cahaya yang memantul langsung menuju kamera, menciptakan 
sorotan dan efek mengkilap. Melalui manipulasi warna spekular, kekuatan cahaya, dan eksponen pemantulan, shader dapat 
mensimulasikan interaksi rumit antara cahaya, permukaan, dan sudut pandang pengamat.

- Cahaya Ambien:
Untuk lebih meningkatkan realisme, simulasi cahaya ambien meniru pencahayaan tidak langsung yang hadir dalam lingkungan 
dunia nyata. Dengan memasukkan kontribusi warna ambien minimal, shader memberi nuansa halus pada adegan virtual, meredakan 
bayangan yang keras, dan meningkatkan kohesi visual keseluruhan.

Sebagai kesimpulan, pencahayaan dalam grafika mencerminkan penyatuan seni dan teknologi, memungkinkan penciptaan pengalaman 
virtual yang menarik dan imersif. Dengan memahami prinsip-prinsip cahaya dan memanfaatkan kekuatan shader, pengembang dapat 
memberikan nafas pada dunia digital, mengangkut penonton ke ranah yang hanya dibatasi oleh imajinasi.

Kesimpulan
Pencahayaan dalam grafika komputer adalah perpaduan antara seni dan teknologi. Dengan pemahaman mendalam tentang prinsip-prinsip cahaya dan implementasi shader yang tepat, kita dapat menciptakan dunia virtual yang imersif dan realistis. Pencahayaan tidak hanya tentang memberikan cahaya, tetapi juga tentang membentuk pengalaman visual yang menarik dan bermakna.


                                                  SHADOW MAPPING
                                      Pemetaan Bayangan: Mencerahkan Realisme

Konsep Dasar Pemetaan Bayangan
Pada dasarnya, pemetaan bayangan menggunakan pendekatan dua langkah untuk mensimulasikan bayangan dalam adegan tiga dimensi. Pertama, adegan dirender dari sudut pandang sumber cahaya untuk membuat peta kedalaman. Peta kedalaman ini menyimpan informasi tentang jarak objek dari sumber cahaya. Kedua, ketika adegan dirender dari sudut pandang kamera, peta kedalaman ini digunakan untuk menentukan area mana yang berada dalam bayangan.

Pemetaan Bayangan dalam Implementasi Grafis
Implementasi pemetaan bayangan memiliki beberapa elemen kunci:

Matriks Transformasi dan Proyeksi: Untuk merender peta kedalaman, transformasi yang tepat diperlukan untuk mengubah objek dan posisi kamera agar sesuai dengan perspektif cahaya. Matriks proyeksi akan bergantung pada jenis sumber cahaya, apakah itu lampu arah, lampu spot, atau lampu titik.
Perhitungan Bayangan: Saat merender dari sudut pandang kamera, fragmen yang dirender perlu diperiksa apakah berada dalam bayangan. Ini dilakukan dengan membandingkan jarak fragmen dengan informasi kedalaman yang ada di peta kedalaman. Jika fragmen lebih jauh dari sumber cahaya daripada kedalaman yang tersimpan, itu berarti fragmen tersebut berada dalam bayangan.
Pengurangan Artefak Bayangan: Salah satu masalah yang sering muncul dalam pemetaan bayangan adalah artefak seperti bayangan acne dan peter panning. Bayangan acne terjadi ketika tekstur peta kedalaman tidak mencakup semua detail dengan cukup baik, menyebabkan pola bayangan yang tidak teratur. Peter panning terjadi saat bayangan tidak tepat mencerminkan geometri karena bias atau ketidakakuratan peta kedalaman. Untuk mengatasi ini, digunakan bias bayangan dan metode penyaringan, seperti penyaringan persentase-closer (PCF), yang membantu menghaluskan bayangan.
Proyeksi Ortografis vs. Perspektif: Lampu arah biasanya menggunakan proyeksi ortografis, yang tidak memperhitungkan jarak (paralel). Sementara lampu spot dan lampu titik lebih cocok dengan proyeksi perspektif, di mana sinar menyebar dengan sudut tertentu.
Dampak Pemetaan Bayangan pada Visualisasi
Pemetaan bayangan memiliki dampak besar pada visualisasi grafis komputer. Bayangan yang dihasilkan dengan baik bisa menambahkan dimensi dan realisme pada adegan. Bayangan tidak hanya menggambarkan ketidakhadiran cahaya tetapi juga memberikan informasi tambahan tentang posisi, ukuran, dan bentuk objek dalam adegan.

Pada akhirnya, pemetaan bayangan adalah salah satu dari banyak teknik yang digunakan untuk menciptakan pengalaman grafis komputer yang lebih realistis dan imersif. Dengan implementasi yang benar, pemetaan bayangan dapat membantu menciptakan lingkungan virtual yang lebih dinamis dan menarik.

- Apa itu Pemetaan Bayangan?
Bayangan bukan sekadar ketiadaan cahaya; mereka adalah petunjuk visual penting yang menambah kedalaman dan realisme pada 
adegan yang dirender. Pemetaan bayangan adalah teknik yang digunakan dalam grafika komputer untuk mensimulasikan efek 
bayangan yang dihasilkan oleh objek dalam suatu adegan yang disinari oleh sumber cahaya. Ini melibatkan merender adegan
dari sudut pandang sumber cahaya untuk membuat peta kedalaman, yang kemudian digunakan untuk menentukan area mana dalam 
adegan yang berada dalam bayangan ketika dirender dari sudut pandang pemirsa.

- Mengapa Melakukan Pemetaan Bayangan?
Melakukan pemetaan bayangan meningkatkan kesetiaan visual dari adegan yang dirender dengan memberikan petunjuk kedalaman 
dan hubungan spasial antara objek. Bayangan berkontribusi secara signifikan pada persepsi realisme, memungkinkan pemirsa 
untuk lebih memahami posisi relatif objek dan distribusi cahaya dalam adegan. Tanpa bayangan, adegan yang dirender mungkin 
terlihat datar dan kurang menarik secara visual. Oleh karena itu, mensimulasikan bayangan melalui teknik seperti pemetaan 
bayangan sangat penting untuk menciptakan lingkungan virtual yang imersif dan dapat dipercaya.

- Bagaimana Pemetaan Bayangan Diimplementasikan?
Proses implementasi pemetaan bayangan melibatkan beberapa langkah:
1. Merender Peta Kedalaman: Adegan dirender dari sudut pandang sumber cahaya untuk menghasilkan peta kedalaman, yang 
merepresentasikan jarak objek dari sudut pandang cahaya. Peta kedalaman ini disimpan sebagai tekstur.

2. Transformasi dan Proyeksi: Transformasi khusus dan matriks proyeksi digunakan untuk merender adegan dari sudut 
pandang cahaya dengan akurat. Matriks ini memastikan bahwa objek ditempatkan dengan benar relatif terhadap sumber cahaya.

3. Perhitungan Bayangan: Selama merender adegan dari sudut pandang pemirsa, posisi setiap fragmen ditransformasikan ke 
dalam ruang koordinat cahaya. Dengan membandingkan kedalaman setiap fragmen dalam adegan dengan nilai kedalaman yang 
sesuai yang disimpan dalam peta kedalaman, ditentukan apakah fragmen tersebut berada dalam bayangan atau tidak.

4. Bias Bayangan dan Penyaringan: Teknik seperti bias bayangan diterapkan untuk mengurangi artefak seperti bayangan acne 
dan peter panning, yang dapat terjadi karena batasan resolusi dan sampling peta kedalaman. Selain itu, metode seperti 
penyaringan persentase-closer (PCF) digunakan untuk menghasilkan bayangan yang lebih halus dan lembut dengan menyampel 
beberapa titik dalam peta kedalaman.

5. Proyeksi Ortografis vs. Perspektif: Pilihan matriks proyeksi (ortografis atau perspektif) tergantung pada jenis sumber 
cahaya yang disimulasikan. Proyeksi ortografis cocok untuk lampu arah, sementara proyeksi perspektif lebih disukai untuk 
lampu spot dan lampu titik.

Secara keseluruhan, pemetaan bayangan adalah teknik yang serbaguna dan efektif untuk mensimulasikan bayangan realistis 
dalam gambar-gambar yang dihasilkan oleh komputer, berkontribusi pada imersi dan kualitas visual keseluruhan dari adegan 
yang dirender.