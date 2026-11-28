# V41
Son sayfa sürümleri birleştirildi. ZIP içindeki dosyaları depo köküne yükleyin.
Google Search Console: URL prefix olarak https://kaansuleymanuz.github.io/ ekleyin, doğrulama dosyanızı köke yükleyin, sitemap.xml gönderin. Hesap doğrulaması kullanıcı tarafından yapılmalıdır.
Atıf ve h-indeksi doğrulanamadı; Google Scholar bağlantısı eklendi. Makale ve kitap sayısı yalnızca sitede listelenenlerdir. Kitap kapağı yayınevinin sunucusundan yüklenir.
Hesaplayıcılar eğitim amaçlıdır. Psikrometrik araç nem oranını hesaplar, diyagram değildir. Isıtma/soğutma yükü basitleştirilmiş duyulur yük hesabıdır.
Ziyaretçi analitiği için ayrı bir hizmet ve kullanıcı hesabı gerekir; takip kodu eklenmemiştir. Google Scholar makale indekslemesi garanti edilmez.

V41: PDF özgeçmiş bölümü ve iki CV dosyası kaldırıldı. Ana sayfadaki mevcut Özgeçmiş bağlantısı korunur. V40 daha önce yüklenmişse CV-tr.pdf ve CV-en.pdf dosyalarını GitHub deposundan ayrıca silin.

V45: latest V42–44 merged; timeline, study summaries (not verbatim abstracts), 10 calculators, 6 schematic animations, formulas, local search, contact card, CSV and print on engineering-tools. No new citation features; publication BibTeX buttons removed. External analytics and Search Console not connected.

V51: V46 yayın özetleri ve etiketleri kaldırıldı; V48 animasyon bölümü Simülasyonlar sayfasından kaldırıldı; V49 iletişim kartı ve QR bölümü kaldırıldı; V50 beyaz, şeffaf, 15 px büyüteç eklendi. enhancements.js bağlantısı önbellek yenilemesi için v=51 olarak güncellendi. Diğer içerikler korunur.

V55: Categorized lab, bilingual unit converter, expandable course material placeholders.

V59: 15 new calculators, approximate air/water properties, 15 typical materials, V57 teaching and V58 simulations retained. Educational approximations; not certified design data.

V65: Added back/forward, laboratory return and category-aware breadcrumbs to tool pages; merged V63 simulations and V64 home.

V66: Parametric sweeps for 36 calculators and Nusselt; mechanical properties; local favorites, recent use and manually saved history; offline cache; search and fullscreen. Analytics/Search Console require owner configuration.

V69: 170 terimli TR–EN mühendislik sözlüğü, kategori filtresi, arama ve CSV dışa aktarımı.

## Google Scholar otomatik güncelleme (V70)
1. SerpApi hesabı açın, API anahtarınızı alın: https://serpapi.com/manage-api-key . Üçüncü taraf hizmetin koşullarını ve kotasını kontrol edin.
2. GitHub deposunda Settings > Secrets and variables > Actions > New repository secret: `SERPAPI_KEY` (anahtar değerini girin, herkese açık dosyaya yazmayın).
3. Settings > Pages > Build and deployment > Source: GitHub Actions seçin. Paket içindeki gizli `.github/workflows/scholar-pages.yml` dahil tüm dosyaları main dalına yükleyin (gerekirse workflow dosyasını GitHub üzerinden Create new file ile oluşturun). `scripts` klasörünü de yükleyin.
4. Actions > Scholar metrics and GitHub Pages > Run workflow ile ilk eşitlemeyi başlatın. Günlük 03:23 UTC (Türkiye 06:23) planlanır; GitHub geciktirebilir. Zamanlanmış iş, 60 gün etkinlik olmadığında devre dışı kalabilir.
5. İzin hatasında Settings > Actions > General ve branch protection ayarlarını kontrol edin; işin main dalına yazma ve Pages yayımlama yetkisi gerekir.

Atıf/h-indeksi tüm yıllar Google Scholar değerleridir. Makale/kitap sayısı Scholar profilindeki benzersiz başlıklardan, mevcut doğrulanmış başlıklar ve Crossref tam başlık/yazar eşleşmesiyle sınıflandırılır; belirsizler dışarıda bırakılır. Yeni belirsiz kayıtlar `scholar-metrics.json` içinde görünür; `scripts/publication-types.json` dosyasına doğrulanmış tür (`article`, `book`, `other`) eklenebilir. Yayın kartları otomatik değiştirilmez. Başarısız sorgu eski JSON'u korur. Son başarılı eşitleme zamanı ekranda gösterilir. Sonraki site güncellemelerinde canlı `scholar-metrics.json` dosyasını boş şablonla ezmeyin. API anahtarı olmadan canlı bağlantı test edilmemiştir.
