SignalR Nedir?
SignalR, Microsoft tarafından geliştirilen, ASP.NET Core ile entegre çalışan bir gerçek zamanlı iletişim kütüphanesidir. SignalR, istemci ve sunucu arasında çift yönlü iletişim kurmayı kolaylaştırır. Bu sayede sunucu, istemciye anlık güncellemeler gönderebilir.

SignalR, WebSocket gibi modern iletişim protokollerini destekler ve gerektiğinde diğer geri dönüş mekanizmalarına (Long Polling, Server-Sent Events) otomatik olarak geçiş yapar.

SignalR'ın Özellikleri
Gerçek Zamanlı İletişim

İstemci ve sunucu arasında hızlı ve anlık veri iletimi sağlar.
Örneğin, canlı sohbet uygulamaları, oyunlar veya gerçek zamanlı bildirimler için kullanılabilir.
Çift Yönlü İletişim

Sunucu, istemciye veri gönderebilir ve istemci de sunucuya mesaj iletebilir.
Protokol Yönetimi

SignalR, varsayılan olarak WebSocket kullanır. Ancak tarayıcı veya ağ kısıtlamaları nedeniyle WebSocket kullanılamazsa, Long Polling veya Server-Sent Events gibi alternatiflere geçiş yapar.
Kolay Kullanım

Karmaşık protokollerle uğraşmadan, basit bir API ile gerçek zamanlı uygulamalar geliştirmenizi sağlar.
SignalR Hangi Durumlarda Kullanılır?
Canlı Sohbet Uygulamaları
Kullanıcıların anlık olarak mesaj alışverişi yaptığı uygulamalar.
Bildirim Sistemleri
Yeni mesaj, güncelleme veya olay bildirimlerini istemcilere anında göndermek için.
Gerçek Zamanlı Paneller
Örneğin, bir finans uygulamasında anlık hisse senedi güncellemeleri.
Çok Oyunculu Oyunlar
Oyuncular arasında hızlı iletişim sağlayarak oyun deneyimini geliştirmek için.
Takip ve İzleme Uygulamaları
Haritalar üzerinde gerçek zamanlı konum veya hareket takibi yapmak için.
SignalR'ın Çalışma Mekanizması
Sunucu Tarafı (Hub)

SignalR, sunucuda Hub adı verilen bir sınıf üzerinden iletişimi yönetir.
Hub, istemci ile sunucu arasındaki veri alışverişini kontrol eder.
İstemci Tarafı

SignalR istemcileri, JavaScript, .NET, Java veya diğer dillerle entegre edilebilir.
İstemciler, sunucuya mesaj gönderir ve sunucudan mesaj alır.
Bağlantı Protokolleri

SignalR, bağlantıyı sağlamak için aşağıdaki protokolleri sırasıyla dener:
WebSocket (En hızlı ve modern protokol)
Server-Sent Events
Long Polling
SignalR'ın Avantajları
Geliştirici Dostu: Basit ve anlaşılır API sayesinde karmaşık protokollerle uğraşmadan gerçek zamanlı iletişim sağlanır.
Esneklik: Farklı istemci türleri (web, mobil, masaüstü) için geniş destek sunar.
Performans: WebSocket sayesinde yüksek performans sağlar.
Ölçeklenebilirlik: Redis, Azure SignalR Service gibi teknolojilerle büyük ölçekli uygulamalarda kullanılabilir.
SignalR Nasıl Kullanılır?
SignalR kullanımı genellikle şu adımları içerir:

Hub Oluşturma
Sunucu tarafında bir hub sınıfı yazarak istemci-sunucu iletişimini tanımlayın.

SignalR Endpoint Tanımlama
SignalR hub'ını bir endpoint olarak yapılandırın.

İstemci Kodunu Yazma
İstemci tarafında SignalR bağlantısını kurarak hub ile iletişim kurun.

Mesajlaşma
Hub üzerinden sunucu ve istemci arasında veri iletin.

Örnek Kullanım: Bir Sohbet Uygulaması
SignalR ile bir sohbet uygulaması geliştirmek için:

Sunucuda bir ChatHub oluşturulur.
İstemciler, mesaj göndermek için hub'a bağlanır.
Hub, tüm istemcilere mesajları iletir.
SignalR, modern gerçek zamanlı uygulamalar geliştirmek için ideal bir araçtır. Kolaylığı, performansı ve esnekliği sayesinde, basit sohbet uygulamalarından karmaşık sistemlere kadar geniş bir yelpazede kullanılabilir.


SignalR ile Gerçek Zamanlı İletişim
Proje Hakkında
Bu proje, ASP.NET Core SignalR kullanılarak gerçek zamanlı iletişim sağlayan basit bir sohbet uygulamasıdır. Kullanıcılar mesaj gönderip alabilir ve bu mesajlar tüm bağlı istemcilere anlık olarak iletilir. SignalR, WebSocket gibi protokoller üzerinden çalışan güçlü bir kütüphanedir ve geri dönüş mekanizmalarını (Long Polling, Server-Sent Events gibi) otomatik olarak yönetir.

Kurulum
Proje Deposu
Bu projeyi klonlayın:

git clone https://github.com/Ogulcan-Dinsever/SignalRExample.git
cd SignalRChat
Bağımlılıkları Yükleyin
Projede kullanılan NuGet paketlerini yükleyin:

dotnet restore
Projeyi Çalıştırın
Aşağıdaki komutu kullanarak uygulamayı çalıştırın:

dotnet run
Tarayıcıda Test Edin
Tarayıcıda şu adresi açarak uygulamayı test edin:

https://localhost:7145/index.html
Özellikler
Gerçek Zamanlı İletişim: Mesajlar anlık olarak tüm bağlı istemcilere iletilir.
Basit Kullanıcı Arayüzü: Kullanıcı adı ve mesaj girerek kolayca iletişim kurabilirsiniz.
SignalR Desteği: WebSocket üzerinden hızlı ve güvenilir iletişim sağlar, gerekirse alternatif protokollere otomatik geçiş yapar.
Kullanılan Teknolojiler
ASP.NET Core 7.0
SignalR
HTML, JavaScript
Dosya Yapısı
Hubs/ChatHub.cs: SignalR hub'ı, mesajların yönlendirilmesinden sorumludur.
wwwroot/index.html: Kullanıcı arayüzü ve istemci tarafında SignalR bağlantısı.
Program.cs: Uygulama yapılandırması ve SignalR endpoint'i tanımları.
Örnek Kullanım
Mesaj Gönderin

"User name" alanına bir kullanıcı adı girin.
"Message" alanına mesajınızı yazın ve "Send" butonuna tıklayın.
Mesaj Alın

Mesajınız ve diğer kullanıcıların mesajları, ekranın altındaki listeye anında eklenir.
Geliştirme İpuçları
Bağlantı Durumu Kontrolü
SignalR istemcisi, bağlantı koparsa otomatik olarak yeniden bağlanmayı dener.
connection.start() çağrısı sırasında oluşan hataları konsoldan kontrol edin.

Sunucu Tarafında Özelleştirme
ChatHub sınıfını genişleterek kişiye özel mesajlaşma veya gruplar gibi yeni özellikler ekleyebilirsiniz.

Performans
SignalR, WebSocket kullanarak minimum gecikme sağlar. Daha fazla istemci için performans optimizasyonları düşünebilirsiniz.

