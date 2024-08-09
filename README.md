# Hull-MA-BB---PineScript
Bu script, TradingView platformunda özel göstergeler ve stratejiler oluşturmak için kullanılan Pine Script dilinde yazılmıştır. Aşağıda scriptin işlevselliği hakkında detaylı bir açıklama bulunmaktadır:

Genel Bakış:
Scriptin Amacı: Bu script, Hull Hareketli Ortalaması (HMA), Bollinger Bantları (BB) ve Hacim Ağırlıklı Ortalama Fiyat (VWAP) gibi birden fazla teknik analiz aracını bir araya getiren özel bir gösterge gibi görünüyor. Ayrıca potansiyel ticaret sinyalleri için uyarılar içerir.
Lisanslama: Script, Mozilla Public License 2.0 altında olup, bir kısmı (Moving Average 3.0 scripti) Alex Orekhov tarafından MIT lisansı altında lisanslanmıştır.

Girdiler:
Uzunluk Girdileri: Script, farklı hareketli ortalamalar için iki uzunluk (length1 ve length2) kullanır.
MA Türü: Kullanıcı, farklı hareketli ortalama türleri (EMA, SMA, VWMA, WMA) arasında seçim yapabilir.
Kaynak: Genellikle fiyat verilerine dayalı olan hareketli ortalamalar için giriş kaynağı, hl2 (yüksek ve düşük fiyatların ortalaması) gibi kullanılır.
VWAP ve Bollinger Bantları: VWAP uzunluğu, kaynak, offset ve Bollinger Bantları için standart sapma gibi parametreler ayarlanabilir.

Fonksiyonlar:
getMA(): Kullanıcı girişine dayalı olarak seçilen hareketli ortalama türünü döndüren yardımcı bir fonksiyondur.
getNMA(): İki farklı hareketli ortalama kullanarak özel bir normalize edilmiş hareketli ortalama (NMA) hesaplayan bir fonksiyondur.
hma(): Hull Hareketli Ortalamasını hesaplar, bu da gecikmeyi azaltmak için tasarlanmış daha hızlı ve daha düzgün bir hareketli ortalamadır.
hma3(): Ekstra yumuşatma ile HMA hesaplamasının değiştirilmiş bir versiyonudur.
kahlman(): Trendin yumuşatılması ve tahmini için kullanılan bir Kahlman filtresini uygular.

Grafikler:
NMA Grafiği: Script, normalize edilmiş hareketli ortalamayı (NMA) sarı bir çizgi olarak grafikte çizer.
VWAP Grafiği: Orta VWAP çizgisi, kullanıcı girdisine göre belirlenen uzunluğu ile pembe renkte çizilir.
Bollinger Bantları: Script, üst ve alt Bollinger Bantlarını ve bir temel çizgiyi çizer.
Hull Trend ve Kahlman: Hull Hareketli Ortalamasına dayalı olarak uzun ve kısa sinyalleri çizer, isteğe bağlı olarak Kahlman filtresi ile yumuşatılır. Bu grafikler renk kodludur (yukarı trend için lime, aşağı trend için kırmızı) ve kesişim noktaları grafikte şekillerle işaretlenir.

Uyarılar:
Uyarı Koşulları: Script, uzun veya kısa kesişim meydana geldiğinde kullanıcıların belirli koşullar karşılandığında bilgilendirilmesini sağlayan uyarılar içerir.

Özet:
Bu script, birden fazla hareketli ortalama, Bollinger Bantları ve VWAP'yi birleştirerek piyasa trendlerini analiz etmek isteyen tüccarlar için kapsamlı bir araç olarak tasarlanmıştır. Ekstra trend yumuşatma için bir Kahlman filtresi içerir ve potansiyel ticaret girişleri (uzun veya kısa pozisyonlar) için uyarılar üretir. Hareketli ortalamalar, kaynak veriler ve uyarı koşulları için özelleştirme seçenekleri, bunu farklı ticaret stratejileri için çok yönlü bir araç haline getirir.
