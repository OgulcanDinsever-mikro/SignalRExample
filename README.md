SignalR ile Gerçek Zamanlı İletişim
Proje Hakkında
Bu proje, ASP.NET Core SignalR kullanılarak gerçek zamanlı iletişim sağlayan basit bir sohbet uygulamasıdır. Kullanıcılar mesaj gönderip alabilir ve bu mesajlar tüm bağlı istemcilere anlık olarak iletilir. SignalR, WebSocket gibi protokoller üzerinden çalışan güçlü bir kütüphanedir ve geri dönüş mekanizmalarını (Long Polling, Server-Sent Events gibi) otomatik olarak yönetir.

Kurulum
Proje Deposu
Bu projeyi klonlayın:

git clone https://github.com/Ogulcan-Dinsever/SignalRChat.git
cd SignalRChat
Bağımlılıkları Yükleyin
Projede kullanılan NuGet paketlerini yükleyin:

bash
Kodu kopyala
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

