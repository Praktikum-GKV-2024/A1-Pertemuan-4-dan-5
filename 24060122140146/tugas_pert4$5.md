# Resume Praktikum Pertemuan 4 dan 5
Lighting dan Shadow
Ahmad Fahrezi/24060122140146/A1/GKV

## Lighting
-Apa itu lighting?
    Lighting (pencahayaan) adalah penggunaan cahaya yang disengaja untuk mencapai efek praktis atau estetika. Pencahayaan adalah salah satu pertimbangan terpenting untuk objek 3D.

    Tujuan lighting (pencahayaan) adalah mensimulasikan sumber cahaya dan cara cahaya yang dipancarkannya berinteraksi dengan objek dalam pemandangan.

-Bagaimana cara cahaya bekerja terhadap suatu permukaan?
    Ketika cahaya mengenai suatu permukaan (objek), sebagian cahaya akan dipantulkan. Cara refleksinya sangat bergantung pada sifat permukaan, terdapat 2 jenis refleksi yaitu Specular Reflection (Pemantulan Teratur) dan Diffuse Reflection (Pemantulan Baur). Jumlah refleksi dapat berbeda untuk panjang gelombang yang berbeda. Sejauh mana suatu material memantulkan cahaya dengan panjang gelombang yang berbeda-beda menentukan warna material tersebut.

-Specular Reflection (Pemantulan Teratur)
    Specular Reflection (Pemantulan Teratur) adalah pemantulan cahaya yang sudut cahaya pantulnya sama dengan sudut cahaya datang, tetapi berlawanan dengan permukaan normal.

    Dalam praktiknya, seberkas cahaya dipantulkan bukan sebagai satu sinar sempurna, namun sebagai kerucut cahaya yang bisa lebih atau kurang sempit. Pemantulan specular dari sebuah permukaan yang sangat berkilau menghasilkan kerucut cahaya pantulan yang sangat sempit; sorotan khusus pada material tersebut kecil dan tajam. Permukaan yang lebih kusam akan menghasilkan kerucut cahaya pantulan yang lebih lebar dan sorotan specular yang lebih besar dan kabur. Di OpenGL, properti material yang menentukan ukuran dan ketajaman sorotan specular disebut shininess. Shininess di OpenGL adalah angka dalam rentang 0 hingga 128. Semakin besar angkanya, sorotan specular semakin kecil.

-Diffuse Reflection (Pemantulan Baur)
    Diffuse Reflection (Pemantulan Baur) adalah pemantulan cahaya ke segala arah yang terjadi karena berkas sinar datang jatuh pada permukaan kasar atau tidak rata.

-Bagaimana cara mensimulasi cahaya?
    Salah satu caranya adalah simulasi cahaya di Shader. Ada 2 cara yaitu Vertex shader dan Fragment shader
    1. Vertex Shader: Menghitung sudut datang (arah cahaya ke vertex), Normal di camera space, dan specular reflection (arah vertex ke camera).

    Vertex shader adalah langkah pertama dalam proses rendering di grafika komputer. Pada tahap ini, setiap vertex dalam objek 3D dihitung untuk menentukan posisi, orientasi, dan properti lainnya. Salah satu aspek penting dari vertex shader adalah perhitungan yang berkaitan dengan cahaya (pantulan), normal, dan arah pandang (sudut datang).

    Pada vertex shader, pertama-tama kita menghitung beberapa vektor penting, seperti arah cahaya ke vertex (LightPosition_cameraspace), normal di camera space (Normal_cameraspace), dan arah dari vertex ke kamera (EyeDirection_cameraspace). Hal ini penting karena digunakan dalam perhitungan fragment shader untuk menentukan warna dan refleksi di setiap fragment.

Selanjutnya, setiap vertex diproyeksikan ke dalam ruang layar menggunakan matriks transformasi. Output dari vertex shader adalah vektor posisi, koordinat tekstur, dan interpolasi yang telah dihitung sebelumnya untuk setiap fragment.

Fragment Shader: Menghitung Diffuse, Specular, dan Cahaya Ambien

Fragment shader adalah tahap selanjutnya dalam proses rendering, di mana setiap fragment (titik-titik kecil di permukaan objek) diberi warna berdasarkan informasi yang diperoleh dari vertex shader.

Diffuse reflection menggambarkan bagaimana cahaya tersebar secara merata ke seluruh permukaan objek. Dihitung berdasarkan sudut datang antara cahaya dan permukaan normal, semakin tegak lurus sudutnya, semakin kuat warna yang dipantulkan. Faktor-faktor seperti warna material, intensitas cahaya, dan jarak ke sumber cahaya mempengaruhi perhitungan ini.

Specular reflection menggambarkan cahaya yang dipantulkan secara teratur seperti cermin. Dihitung berdasarkan sudut datang antara arah pandang kamera dan vektor refleksi cahaya. Faktor seperti warna spekular, intensitas cahaya, dan kehalusan permukaan akan memengaruhi hasil akhir.

Cahaya ambien mensimulasikan efek pencahayaan tidak langsung di ruang tertutup. Ini memberikan warna minimum pada objek bahkan dalam kondisi cahaya rendah. Faktor-faktor seperti warna ambien dan warna material objek digunakan untuk menghitung efek ini.

Setelah menghitung ketiga aspek ini, tambahkan hasilnya  untuk mendapatkan warna akhir yang ditetapkan pada setiap fragmen.
 Oleh karena itu, fragment shader menghasilkan gambar akhir yang penuh warna dan realistis tergantung pada pencahayaan dan material objek yang dirender.

-Mengapa mengimplementasi/mensimulasikan lighting dalam 3D?
    Mengimplementasikan lighting dalam grafika 3D bukan hanya tentang menciptakan gambar yang terlihat bagus secara visual, tetapi juga tentang menciptakan pengalaman visual yang lebih mendalam, realistis, dan berarti bagi pengguna.

## Shadow
-Apa itu shadow?
    Bayangan (Shadow) merupakan salah satu aspek penting dalam menciptakan realisme dan kedalaman pada gambar 3D. Ini merupakan proses penting yang menentukan derajat gelap atau terang pada permukaan objek, yang tercermin dalam warna dan intensitas pada setiap piksel. Pada media yang lebih gelap atau terang, bayangan memainkan peran penting dalam memberikan dimensi visual pada objek yang dihasilkan oleh komputer.

-Bagaimana cara membuat shading?
Pada dasarnya proses shading memiliki beberapa langkah utama:
1. Menentukan luas tampak pada setiap piksel: Setiap piksel pada gambar dianalisis untuk menentukan bagian permukaan objek yang terlihat.

2. Perhitungan normal pada permukaan: Vektor normal merupakan vektor tegak lurus pada permukaan objek, dihitung untuk setiap piksel. Ini penting dalam menentukan cara cahaya memantul dari permukaan.

3. Evaluasi intensitas cahaya dan warna menggunakan model iluminasi: Model iluminasi digunakan untuk menghitung bagaimana cahaya akan diterima dan dipantulkan oleh permukaan objek, dengan memperhitungkan sudut, jarak, dan properti materi.

Unsur-unsur yang mempengaruhi bayangan meliputi vektor normal, vektor satuan, dan vektor optik. Vektor normal menentukan arah tegak lurus dari permukaan objek, sementara vektor satuan adalah vektor yang berukuran satuan dan arahnya bergantung pada vektor asalnya. Vektor optik mewakili konsep bagaimana cahaya jatuh pada suatu objek.

Metode bayangan dapat dibagi menjadi dua kategori utama: direct line dan indirect line.

1. Direct line:
   - Flat Shading: teknik shading yang memberikan satu jenis warna pada setiap polygon dan hanya memerlukan satu kali kalkulasi untuk pewarnaan. Tipe flat shading diantaranya Lambertian Shading dan Uniform Shading.
    Penerapan Flat Shading pada OpenGL :
    glShadeModel(GL_FLAT);

   - Gouraud Shading: Sebuah teknik yang menciptakan transisi warna yang lebih halus antar permukaan objek dengan memperhatikan warna dan pencahayaan di setiap sudut segitiga.

   - Phong Shading: Metode yang lebih kompleks yang melibatkan interpolasi linear dari permukaan normal di setiap piksel, menerapkan model pencahayaan Phong.

2. Indirect line:
   - Ray Tracing: Teknik yang kompleks untuk menghasilkan gambar dengan menelusuri jalur sinar atau partikel dalam suatu sistem.

   - Radiosity: Teknik pencahayaan virtual yang menghasilkan hasil yang sangat realistis namun membutuhkan waktu dan perhitungan.

Terdapat pula berbagai teknik bayangan lainnya, seperti cross hatching, yang menggunakan pola garis-garis tegak lurus untuk menciptakan dimensi visual. Macam-macam bayangan dapat dibagi berdasarkan struktur pandangan dan pandangan jarak, termasuk bayangan lembut (soft shadow) dan bayangan keras (hard shadow).

-Mengapa mengimplementasi/mensimulasi shadow?
    Karena pemahaman yang mendalam tentang bayangan dan penerapannya dalam grafika komputer memungkinkan pembuatan gambar yang lebih realistis dan menarik, menciptakan pengalaman visual yang memukau bagi pengguna.