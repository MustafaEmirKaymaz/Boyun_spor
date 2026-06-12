readme_content = """# 🎮 Nexus Games — Çoklu Mini Oyun ve Veri Yönetim Platformu

Nexus Games, tarayıcı üzerinden doğrudan oynanabilen **20 farklı mini oyun simülasyonunu**, dinamik bir kullanıcı arayüzünü ve gerçek zamanlı bir **Admin Yönetim Panelini** tek bir kaynak dosyada (`index.html`) birleştiren modern, siberpunk temalı bir web uygulamasıdır.

Bu proje; veri listeleme, dinamik arama, kategori filtreleme, modüler etkileşim (modal sistemleri), yerel durum yönetimi (local state management) ve veri kümesi dışa aktarma (JSON Export) konseptlerini uygulamalı olarak göstermek amacıyla geliştirilmiştir.

---

## 🚀 Öne Çıkan Özellikler

### 1. Kullanıcı Arayüzü & Deneyimi (UI/UX)
* **Siberpunk & Neon Tema:** Derin koyu arka planlar (`#050a14`), neon mavi (`#00f5ff`) ve neon pembe (`#ff006e`) vurgularla zenginleştirilmiş, göz yormayan modern oyun lobisi tasarımı.
* **Akıcı Animasyonlar:** Kartların lobiye yüklenmesinde gecikmeli (staggered) giriş efektleri ve hover animasyonları.
* **Tam Responsive Yapı:** Büyük ekranlı oyuncu monitörlerinden mobil cihazlara kadar kusursuz uyum sağlayan esnek grid yapısı.

### 2. Akıllı Filtreleme ve Arama Motoru
* Kullanıcılar, arama çubuğuna yazdıkları harfe göre oyun adları ve türleri arasında anında (real-time) filtreleme yapabilirler.
* **Kategori Sekmeleri:** Aksiyon, Bulmaca, Strateji, Yarış, Spor ve Klasik türleri arasında tek tıkla geçiş imkanı.

### 3. Etkileşimli Oyun Modalı & Puanlama Sistemi
* Herhangi bir oyuna tıklandığında sayfa yenilenmeden açılan **Modal (Pencere)** mimarisi.
* **Oyun Simülasyonu:** `TriggerScore` fonksiyonları ile oyuncuların anlık puan toplama mekanizması.
* **Gelişmiş Değerlendirme Sistemi:** Yıldız tabanlı derecelendirme (1-5 Yıldız) ve anlık yorum bırakma alanı. Gönderilen yorumlar anında oyun verisine işlenir ve ağırlıklı ortalama puanı dinamik olarak yeniden hesaplar.

### 4. Gelişmiş Admin Paneli & Veri Seti Yönetimi
* **Anlık İstatistik Kartları:** Toplam oynanma sayısı, platform genelindeki yorum sayısı, ortalama kullanıcı puanı ve platformun "En Popüler" (En çok tıklanan) oyununu dinamik hesaplayan algoritmalar.
* **Veri Tablosu:** Tüm oyunların performans metriklerini, puan barlarını (CSS Progress Bar) ve durum pencerelerini içeren detaylı yönetim tablosu.
* **Canlı JSON Görünümü:** Veri tabanında (state) tutulan 20 oyunun tüm güncel yorumları ve puanlarıyla birlikte anlık üretilen kod çıktısı.
* **JSON Dışa Aktarma (Export):** Tek tıkla güncel veri kümesini `nexus_games_dataset.json` adıyla bilgisayara indirme altyapısı.

---

## 🗃️ Sistemde Yer Alan 20 Oyunun Listesi

Platform, her biri kendine ait açıklama, emoji, dinamik renk kodu ve oynanış yönergesine sahip şu oyunları içerir:

1. **🐍 Snake Nexus** (Klasik) — Neon yılan oyunu.
2. **🏓 Pong Wars** (Klasik) — Çift toplu nostaljik masa tenisi.
3. **👾 Space Invaders X** (Aksiyon) — Uzaylı istilası shooter oyunu.
4. **🧠 Memory Master** (Bulmaca) — Görsel hafıza ve kart eşleştirme.
5. **🟦 Tetris Blitz** (Bulmaca) — Hızlı tempolu blok yerleştirme ve combo.
6. **Rex Dino Runner** (Aksiyon) — Engellerden kaçış sonsuz koşu oyunu.
7. **🌌 2048 Galaxy** (Strateji) — Sayı birleştirme ve galaksi bulmacası.
8. **📝 Crossword Ultra** (Bulmaca) — Türkçe çapraz harf bulmaca oyunu.
9. **🐦 Flappy Neon** (Aksiyon) — Hassas refleks odaklı boru geçiş oyunu.
10. **💣 Minesweeper Pro** (Strateji) — Mantık ve sayılara dayalı mayın tarlası.
11. **🏎️ Racing Pixel** (Yarış) — Piksel grafikli dikey şerit yarış oyunu.
12. **🏀 Basketball Shoot** (Spor) — Fizik tabanlı açı ve güç ayarlı pota atışı.
13. **🔤 Word Scramble** (Bulmaca) — Karışık harflerden kelime türetme yarışı.
14. **🏰 Tower Defense X** (Strateji) — Savunma kuleleri yerleştirme ve strateji.
15. **🧱 Brick Breaker** (Klasik) — Platformla topu sektirip tuğla kırma oyunu.
16. **❌ Tic-Tac-Toe AI** (Strateji) — Yenilmez yapay zekaya karşı XOX.
17. **🍉 Fruit Ninja Lite** (Aksiyon) — Ekranda geçen meyveleri kesme simülasyonu.
18. **🔢 Sudoku Zen** (Bulmaca) — Zihin rahatlatıcı klasik 9x9 sayı bulmacası.
19. **☄️ Asteroids Fury** (Aksiyon) — Asteroit fırtınasında hayatta kalma savaşı.
20. **🎹 Piano Tiles** (Spor) — Ritme göre akan siyah tuşlara basma oyunu.

---

## 🛠️ Teknik Altyapı ve Kurulum

Proje **sıfır bağımlılık (zero-dependency)** ilkesiyle yazılmıştır. Çalışması için herhangi bir sunucuya, Node.js paketine veya harici bir kütüphaneye (React, Vue vb.) ihtiyaç duymaz. Google Fonts haricindeki tüm CSS ve JS mantığı dosyanın içinde gömülüdür.

### Çalıştırma Adımları:
1. Bilgisayarınızda bir klasör oluşturun.
2. `index.html` dosyasını bu klasöre kaydedin.
3. Dosyaya çift tıklayarak herhangi bir modern web tarayıcısında (Chrome, Edge, Safari, Firefox) anında çalıştırın.

### Kod Yapısı:
* **HTML5:** Sayfa iskeleti, modal pencereleri ve admin tabloları için semantik etiketleme.
* **CSS3:** CSS Değişkenleri (Variables), CSS Grid, Flexbox yapısı ve `@keyframes` animasyonları.
* **Pure JavaScript (ES6+):** Temiz durum yönetimi (state management), `map()` ve `filter()` tabanlı dinamik DOM manipülasyonu, olay yöneticileri (event listeners) ve veri akış algoritmaları.

---

## 📈 Veri Modeli Şeması (Örnek)

Admin panelinden dışa aktarılan veya sistem içinde işlenen her oyun objesi şu veri şemasına uyar:

```json
{
  "id": 1,
  "name": "Snake Nexus",
  "emoji": "🐍",
  "genre": "klasik",
  "description": "Efsanevi yılan oyununun neon versiyonu. Yemi ye, büy, duvarlara çarpma!",
  "howToPlay": "Ok tuşları veya WASD ile yılanı yönlendir. Yemi ye puan kazan. Duvara veya kendine çarpma!",
  "rating": 4.7,
  "totalPlays": 12543,
  "commentCount": 2,
  "badge": "hot",
  "comments": [
    { "stars": 5, "text": "Süper klasik! Bitirene kadar duramadım." },
    { "stars": 4, "text": "Güzel ama biraz hızlı." }
  ]
}
