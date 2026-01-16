Rast Mobile Kanban Task Management System
Bu proje, Rast Mobile teknik mülakat süreci için geliştirilmiş, dinamik board yapısına sahip Fullstack bir Kanban uygulamasıdır. Figma tasarımı temel alınarak modernize edilmiştir.

Öne Çıkan Özellikler:
Dinamik Board (ID) Sistemi: Her board benzersiz bir slug/ID üzerinden oluşturulur ve erişilir. Örn: localhost:3001/proje-adi.

Fullstack Mimari: Veriler MongoDB üzerinde kalıcı olarak saklanır.

Sürükle ve Bırak (DnD): @dnd-kit kullanılarak kartlar hem sütunlar arası hem de liste içi taşınabilir.

Sabit 4 Liste Yapısı: Task gereksinimlerine uygun olarak Backlog, To Do, In Progress ve Done sütunları mevcuttur.

Gelişmiş UI/UX: Figma tasarımına %100 sadık kalınan, Tailwind CSS ile güçlendirilmiş responsive arayüz.

Bonus (Son Gezilenler): localStorage entegrasyonu ile kullanıcının ziyaret ettiği son boardlar giriş ekranında listelenir.

Kullanılan Teknolojiler
Frontend: React 18, Next.js 14 (App Router), TypeScript
Styling: Tailwind CSS
Database & ORM: MongoDB Atlas, Prisma ORM
State Management: DnD-kit

Kurulum ve Çalıştırma:
Projeyi yerel ortamınızda çalıştırmak için aşağıdaki adımları takip edebilirsiniz:

1. Bağımlılıkları Yükleyin
npm install

2. Ortam Değişkenlerini Ayarlayın
Kök dizinde bir .env dosyası oluşturun ve MongoDB bağlantı adresinizi ekleyin:
Kod snippet'i
DATABASE_URL="mongodb+srv://<username>:<password>@cluster.mongodb.net/rast-kanban"

3. Veritabanı Şemasını Senkronize Edin:
Prisma modellerini veritabanına yansıtmak ve istemciyi oluşturmak için:
npx prisma db push
npx prisma generate

4. Uygulamayı Başlatın
npm run dev
Uygulama varsayılan olarak http://localhost:3000 (veya port doluysa 3001) adresinde çalışacaktır.

Proje Yapısı:
src/app/[id]/page.tsx: Dinamik routing (Board ID) mantığının yönetimi.
src/components: KanbanBoard, Column ve Card gibi atomik bileşenler.
src/services: Frontend'den API'ye veri taşıyan servis katmanı.
prisma/schema.prisma: Veritabanı modellerinin (Board ve Task) tanımları.

API Testi
Proje kök dizininde bulunan postman_collection.json dosyasını Postman'e import ederek RESTful API endpoint'lerini test edebilirsiniz.