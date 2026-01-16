Rast Mobile Kanban Task Management System
Bu projede kullanıcılar kendi board’larını oluşturabilir, task’leri sürükle-bırak ile yönetebilir ve tüm veriler kalıcı olarak veritabanında saklanır.
Projeyi geliştirirken fullstack olarak çalıştım ve hem frontend hem backend tarafını kendim oluşturdum.

Projede Kullandıklarım & Özellikler:
Fullstack Yapı
Uygulamada frontend ve backend birlikte çalışmaktadır. Veriler MongoDB üzerinde tutulur.

Sürükle & Bırak (DnD)
@dnd-kit kullanarak task’ler hem sütunlar arasında hem de kendi listesi içinde taşınabilir.

Sabit 4 Liste Yapısı
Kanban mantığına uygun olarak:
Backlog
To Do
In Progress
Done

Gelişmiş UI / UX
Arayüzü Tailwind CSS kullanarak modern, responsive ve kullanıcı dostu şekilde tasarladım.

Son Gezilen Boardlar
localStorage entegrasyonu sayesinde kullanıcının ziyaret ettiği son board’lar giriş ekranında listelenir.

Kullanılan Teknolojiler
React / Next.js
TypeScript
Tailwind CSS
MongoDB
Prisma ORM
@dnd-kit

Projeyi Çalıştırma
Projeyi yerel ortamda çalıştırmak için:
npm install
MongoDB bağlantınızı .env dosyasına ekleyin.
DATABASE_URL="mongodb+srv://..."
Ardından:
npm run dev
komutuyla uygulamayı başlatabilirsiniz.
