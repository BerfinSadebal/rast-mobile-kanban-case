PROJE ANALİZİ VE GELİŞTİRME SÜRECİ
1. Projenin Tanımı ve Beklentiler
Bu proje, Rast Mobile tarafından iletilen Figma tasarımı doğrultusunda geliştirilmiş, dinamik bir Kanban Board uygulamasıdır. Projenin temel amacı, kullanıcıların benzersiz Board ID'leri üzerinden görevlerini (Tasks) kategorize edebilmesi ve bu görevleri sürükle-bırak yöntemiyle yönetebilmesidir.

2. İzlenen Geliştirme Adımları
Altyapı Kurulumu: Next.js kullanılarak projenin iskeleti oluşturuldu ve TypeScript ile tip güvenliği sağlandı.

Veritabanı Entegrasyonu: Verilerin kalıcı olarak saklanması için MongoDB Atlas tercih edildi. src/lib/mongodb.ts üzerinden bağlantı sağlandı.

Dinamik Routing: Taskta istenen https://localhost/:id formatı için Next.js'in [id] klasör yapısı kullanılarak dinamik sayfa yapısı kurgulandı.

Bileşen (Component) Mimarisi: Proje; KanbanBoard, Column ve Card gibi modüler bileşenlere ayrıldı.

Sürükle-Bırak Mantığı: Kartların sütunlar arası taşınabilmesi ve liste içi sıralanması için @dnd-kit kütüphanesi entegre edildi.

Responsive Tasarım: Tailwind CSS kullanılarak uygulamanın hem masaüstü hem de mobil cihazlarda sorunsuz çalışması sağlandı.

3. Kullanılan Teknolojiler
Frontend: React, Next.js, Tailwind CSS
Backend: Next.js API Routes (Restful API prensiplerine uygun)
Database: MongoDB
State & DnD: dnd-kit