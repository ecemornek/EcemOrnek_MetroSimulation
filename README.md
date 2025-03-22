METRO SİMÜLASYONU
Bu proje, bir metro ağı hattı üzerinde en kısa ve en hızlı rotaları bulmayı sağlayan bir simülasyondur. BFS (Genişlik öncelikli arama) ve A* algoritmaları kullanılarak istasyonlar arası geçişlerin en verimli şekilde hesaplanması amaçlanmıştır.

-Kullanılan Teknolojiler ve Kütüphaneler
	-> heapq: Öncelikli kuyruk yapısı sağlamak için kullanılır. A algoritmasında en düşük maliyetli düğümü verimli bir şekilde seçmek için kullanılır.
	-> collections: Özellikle **deque* yapısı, BFS algoritmasında kuyruk tabanlı gezinme işlemlerinde kullanılır.
	-> math: A algoritması için Öklidyen mesafe veya diğer heuristik hesaplamalarda kullanılır.

	
-Algoritmaların Çalışma Mantığı

   BFS Algoritması(En Az Aktarma Bulma):
 BFS (Breadth-First Search), en kısa mesafeli yolu bulmak için kullanılan bir algoritmadır. Metro sistemlerinde, en az hat değiştirerek bir istasyondan diğerine ulaşmak için güzel bir yöntemdir.Tüm yolları eşit değerlendirip aktarma sayısını minimize ettiği için kullanımı avantajlıdır.
  BFS Nasıl Çalışır?
1-) Başlangıç istasyonu kuyruğa eklenir.
2-)Her adımda komşu istasyonlar kontrol edilir.
3-)En kısa yol keşfedildiğinde, durulur.


    A*Algoritması(En Hızlı Rota):
  A* algoritması, bir noktadan diğerine en kısa sürede ulaşmayı sağlar. Metro sistemlerinde, en kısa sürede hedefe varmak için kullanılır. Trafik yoğunluğu gibi dinamik süreler eklenebilmesi, hızlı olması ve en kısa sürede hedefe ulaşması avantajlarındandır.
  A* Nasıl Çalışır?
1-) Şu ana kadar geçen süre (g) hesaplanır.
2-)Tahmini kalan süre (h) tahmin edilir.
3-)Toplam süre (f = g + h) en düşük olan yol seçilir.


-Örnek Kullanım ve Test Sonuçları

Aşağıda bir örnek test senaryosu gösterilmiştir:

-> Başlangıç Noktası: İstasyon A
-> Hedef Noktası: İstasyon F
-> BFS Sonucu: 3 aktarma
-> A* Sonucu: 12 dakika

Testler, farklı metro ağı yapıları üzerinde uygulanmış ve her iki algoritmanın farklı senaryolarda uygun çözümler sunduğu gözlemlenmiştir.



-Projeyi Geliştirme Fikirleri

-> Görselleştirme: NetworkX ve Matplotlib kullanarak metro haritası görselleştirilebilir.
-> Mobil Uygulama: Bir mobil uygulama ile kullanıcılara en iyi metro rotası önerilebilir.
-> Gerçek Zamanlı Veri: Trafik yoğunluğu, tren gecikmeleri gibi dinamik veriler sisteme entegre edilebilir.
-> Makine Öğrenmesi Desteği: Kullanıcı verileri analiz edilerek en uygun güzergah önerileri geliştirilebilir.



