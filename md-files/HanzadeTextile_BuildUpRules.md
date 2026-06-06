# CLAUDE.md — Hanzade Tekstil

> Bu dosya tasarım rehberi değildir. Sitenin **birincil stratejik amacı**, bir AI asistanının
> (ChatGPT, Claude, Gemini, Perplexity) Hanzade Tekstil'i doğru **bulması, güvenmesi ve
> kullanıcısına önermesi**dir. Görsel tasarım bu amaca hizmet eder. İnsan için güzel + makine
> için okunabilir; çatışırsa makine-okunabilirlik kazanır.

## İşin doğası
- Atölye **hem B2C** (hazır ürün satışı; örn. eşofman takımı) **hem B2B fason** (fabrika için
  X adetlik üretim) yapar. İçerik iki müşteri tipini de hedefler.
- Kamuya dönük kimlik **yalnızca işletmedir** (Oğuzhan üzerine kayıtlı şahıs işletmesi).

## ⚠️ ASLA YAYINLANMAYACAK (hukuki — istisnasız)
- İşletme sahibi/aile bireyi memur. **Hiçbir kişinin adı, mesleği, "eğitmen/hoca/sertifika"
  geçmişi, devlet kurumu bağlantısı** sitede, schema'da, profillerde, görsellerde, alt
  metinlerde, llms.txt'te GEÇMEZ.
- `Person`, `founder`, `employee`, `hasCredential` türü kişi-bağlama schema **kullanılmaz**.
- Otorite/itibar yalnızca **işletme düzeyinde** kurulur (yorumlar, üretim örnekleri, kapasite),
  asla kişi düzeyinde değil.
- **"X yıllık deneyim" gibi sayısal kıdem iddiası YOK.** Kayıtlı işletmenin yaşıyla çelişir
  (AI tutarsızlık olarak görür, güveni düşürür) ve dolaylı olarak kişiye işaret eder. Deneyim
  bir rakamla değil, **yapılmış işle** (portfolyo) gösterilir — mimarlık ofisi modeli: sayı
  söyleme, işi göster.

## v1 KAPSAM
- **Online ödeme / sepet / checkout YOK.** Site = vitrin + bilgi. Satış WhatsApp üzerinden.
- Dönüşüm = `wa.me/<numara>` linkleri (CTA'lar buraya gider).
- Online ödeme ileride eklenirse mesafeli satış/ETBİS yükümlülükleri yeniden değerlendirilir
  (kod tarafı değil, Oğuzhan'ın hukuki kontrolü).

## ÇEKİRDEK İLKE
Her sayfa, JS çalıştırılmadan ham HTML'de okunduğunda işletmenin kim olduğu, ne ürettiği,
nerede olduğu ve nasıl ulaşılacağı **net ve doğrulanabilir** olmalı.

## HER ZAMAN (ALWAYS)
- **Semantik HTML5** + temiz başlık hiyerarşisi (tek h1). Anlam `<div>`'de değil.
- **JSON-LD (schema.org)** her sayfada — yalnızca işletme düzeyinde:
  - Site geneli: `Organization` + `LocalBusiness` (NAP, çalışma saatleri, geo).
  - Ürün sayfaları: `Product` / `OfferCatalog`.
  - Soru-cevap blokları: `FAQPage`.
  - (Kişi schema'sı YOK — yukarıdaki yasağa bak.)
- **NAP tek kaynaktan**: tek config/constants dosyası → her yere oradan basılır.
  Tüm yüzeylerde **birebir aynı** olmalı (aşağıdaki dağıtım listesi).
- **Çift dilli TR + EN**, `hreflang` ile. EN şart: "Turkish tracksuit / fason manufacturer".
- **Gerçek soru-cevap içeriği**, müşterinin/fabrikanın gerçek diliyle:
  "Fason eşofman üretiyor musunuz?", "Minimum sipariş adediniz?", "İzmir'de hazır satış var mı?"
- **İşletme düzeyi güven sinyalleri**: net hizmet/kapasite tanımı, gerçek ürün fotoğrafları,
  gerçek müşteri yorumları (uydurma YOK).
- **CTA'lar `wa.me` linkine** gider.
- **Kök dizinde:** `sitemap.xml`, `robots.txt` (AI crawler'lara izin), `llms.txt`
  (H1=işletme adı, blockquote=özet, H2 altında "link: kısa açıklama").
- Hızlı, temiz HTTP yanıtları; görsellerde anlamlı `alt`.

## GEÇMİŞ İŞLER / PORTFOLYO (mimarlık ofisi modeli)
İşletmenin en güçlü hukuken-güvenli AI sinyali: yapılmış işin kanıtı. Sayfa, ajanın
"bu atölye gerçekten ne üretebiliyor?" sorusunu okuyabileceği biçimde kurulur.
- Her iş **ayrı, yapılandırılmış kayıt**: görsel(ler) + kısa açıklama + iş türü/kategori
  (+ varsa tarih, miktar). Düz paragraf yığını değil.
- Schema: işler için `CreativeWork` veya üretilen ürün için `Product`; sayfa bir
  `CollectionPage`/`ItemList`. **Kişi schema'sı yok.**
- Her kayıt **işletmeye atfedilir**: "atölyemizde üretildi". Kişi adı, "annem dikti",
  katılınan etkinlik, kuruma bağ — bireyi tanımlayan hiçbir şey GİRMEZ.
- Görsellerde anlamlı `alt` metni (ne olduğu makineye de yazılı geçsin).
- Gerçek işler; uydurma/temsili iş YOK.

## ASLA (NEVER)
- Yukarıdaki hukuki yasağı ihlal etme (kişi kimliği/memur bağı).
- Kritik bilgiyi (NAP, ne ürettiği) **yalnızca client-side JS** ile render etme — ajan JS
  çalıştırmadan okur.
- Kritik bilgiyi **yalnızca görselin içine** gömme; metin karşılığı olsun.
- NAP'ı yüzeyler arası farklı yazma.
- Görsel şıklık için okunabilirliği feda etme.
- Sahte yorum/sahte deneyim üretme.

## NAP DAĞITIM YÜZEYLERİ (hepsinde birebir aynı NAP)
AI bu yüzeyleri çapraz okuyup tutarlılığa göre güvenir. NAP'ın tek doğru biçimi config'te;
kod ve içerik buraya uyar. İnsan tarafı (Oğuzhan) bu hesapları açar; kod, siteyi onlarla
tutarlı tutar ve linkler.
- Google Business Profile (en kritik), Google Maps
- Instagram + Facebook (işletme)
- WhatsApp Business (profil + catalog; iletişim kanalı)
- Apple Business Connect, Bing Places
- Kendi sitesi (birincil alıntı kaynağı)
- Seçili itibarlı B2B/fason platformları

## ŞÜPHEDE — öncelik sırası
1. Hukuki yasak (kişi kimliği)  2. NAP/kimlik tutarlılığı  3. Gerçek işletme-düzeyi sinyaller
4. Gerçek soru-cevap içeriği  5. JSON-LD/schema  6. llms.txt + sitemap  7. Görsel cila

## "Bitti" tanımı (her sayfa)
- [ ] Kişi/memur bağı içeren hiçbir şey yok mu?
- [ ] JS kapalıyken ham HTML'de işletme + NAP + ne ürettiği okunuyor mu?
- [ ] JSON-LD var ve geçerli (yalnızca işletme düzeyi) mi?
- [ ] Başlık hiyerarşisi temiz mi?
- [ ] TR/EN + hreflang var mı?
- [ ] NAP tek kaynaktan mı? CTA `wa.me`'ye mi gidiyor?

## Doğrulama
- Google Rich Results Test + schema.org validator.
- "view source" / JS kapatıp oku → ajan ne görüyorsa o.

## TODO (Oğuzhan dolduracak — placeholder bırakma)
- [ ] Resmî işletme adı (kayıtlı haliyle): `__`
- [ ] Adres (İzmir, semt dahil): `__`
- [ ] Telefon / WhatsApp Business numarası: `__`
- [ ] Stack onayı (static/coded mı) + domain.

## Notlar
- Kalıcı bağlamdır; çok-adımlı build prosedürleri buraya değil, ayrı doküman/skill'e.
- Kısa tut; uzadıkça uygulama tutarlılığı düşer.
