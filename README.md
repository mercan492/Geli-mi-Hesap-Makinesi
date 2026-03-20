# Geli-mi-Hesap-Makinesi
Python ile geliştirilmiş, bilimsel fonksiyonları ve işlem geçmişi takibini destekleyen, modüler yapıda gelişmiş hesap makinesi uygulaması.

🧠 Kodun Teknik Analizi ve Çalışma Mantığı
Bu proje, "Sorumlulukların Ayrılması" (Separation of Concerns) prensibi üzerine inşa edilmiştir. Kod üç ana katmandan oluşur:
1. İş Mantığı Katmanı (Business Logic Layer)
Matematiksel hesaplamalar, ana programdan bağımsız fonksiyonlar olarak tanımlanmıştır.
•	Dinamik İşleme: sum(), len() gibi Python'un gömülü fonksiyonları kullanılarak, veri setinin boyutu (n adet sayı) ne olursa olsun aynı mantıkla çalışması sağlanmıştır.
•	List Comprehension: Kare ve karekök hesaplamalarında kullanılan [n**2 for n in veriler] yapısı, hem bellek yönetimi hem de kod okunabilirliği açısından en üst seviye Pythonic yaklaşımdır.
2. Veri Giriş ve Dönüştürme Katmanı (Data Ingestion)
Kullanıcının girdiği ham metin (string), analiz edilebilir sayısal verilere (float list) dönüştürülür.
•	split() & float(): Boşluklarla ayrılmış metni parçalayıp sayıya çevirerek, geleneksel "tek tek sayı isteme" hantallığı ortadan kaldırılmıştır. Bu, veri bilimindeki "Veri Temizleme" (Data Cleaning) aşamasının minyatür bir örneğidir.
3. Güvenlik ve Hata Yönetimi Katmanı (Robustness)
Gerçek dünya verisi kirli ve hatalıdır. Kod, bu riskleri try-except bloklarıyla yönetir.
•	Hata Yakalama: Kullanıcı sayı yerine harf girerse veya boş bırakırsa program çökmez; kullanıcıyı profesyonel bir dille uyarır.
•	Mantıksal Kontroller: Bölme işleminde "sıfır" (ZeroDivision) kontrolü yapılarak uygulamanın çalışma zamanı (runtime) hataları önlenmiştir.
4. Giriş Noktası (Entry Point)
if __name__ == "__main__": bloğu kullanılarak, kodun hem tek başına bir uygulama olarak çalışabilmesi hem de ileride başka bir projeye "modül" olarak dahil edilebilmesi sağlanmıştır. Bu, ölçeklenebilir yazılımın temelidir.
________________________________________






