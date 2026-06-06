# Tasarım Yönergesi — Hanzade Tekstil

> Bu dosya sitenin tasarım anayasasıdır. Claude Code'a context olarak verilir.
> Amaç: Sézane'in **sistemini** referans almak — sitesini kopyalamamak.
> Marka kimliği kendine ait kalır: koç-kırmızısı aksan, atölye anlatısı.
>
> NOT: Görseller (atölye/kesim/etkinlik fotoğrafları) ve logo/amblem
> site sahibi tarafından ayrıca sağlanacaktır. Claude Code logo, amblem
> veya yer-tutucu görsel ÜRETMEZ; bunlar için boş/placeholder alan bırakır.

---

## 1. Marka özü

- **İsim:** Hanzade
- **Kim:** Ölçüye özel kesim/dikim yapan, el emeği bir tekstil atölyesi.
- **His:** Sade, zarif, sıcak. "Bir atölyenin kapısından içeri girmek" gibi.
- **Ton:** Mağaza değil, takdim. Ürünü dizmiyoruz; sahneye çıkarıyoruz (Aslan/Güneş), ama tek bir keskin aksanla (Koç/Mars).
- **İsim oyunu (marka cinası, sözlük iddiası değil):** Han → Erkek · Hanzade → Kadın · Zade → Çocuk. Kadın hattı markanın tam adını taşır. "Markamızın üç odası" diye sunulur, "ismin gizli anlamı budur" diye değil.

## 2. Sézane'den ne alıyoruz (ilke), neyi almıyoruz (asla)

ALIYORUZ:
- Bol beyaz/fildişi alan — nefes alan layout.
- Editöryel, büyük ve az sayıda görsel (katalog değil, dergi).
- Sıcak, davetkâr, "toprak" renk paleti.
- Serif display + sade sans gövde tipografi hiyerarşisi.
- Yumuşak, sakin mikro-etkileşimler (hover'da hafif geçiş).

ALMIYORUZ:
- Sézane'in fotoğraflarını, font dosyalarını, birebir layout'unu.
- Onun logosunu/renk kodlarını.
- Hazır giyim e-ticaret mantığını olduğu gibi — bizimki atölye + ölçüye özel.

## 3. Renk token'ları

| Token | Hex | Kullanım |
|---|---|---|
| `--bg-ivory` | `#F7F1E6` | Ana zemin |
| `--surface` | `#FBF7EF` | Kart/panel yüzeyi |
| `--ink` | `#2B211A` | Ana metin (sıcak siyah, asla saf #000) |
| `--ink-soft` | `#5C5142` | İkincil metin |
| `--gold` | `#B79A6E` | Altın aksan, ince çizgiler, ikonlar |
| `--gold-deep` | `#A8895C` | Altın koyu ton |
| `--oxblood` | `#9A3324` | TEK keskin aksan: butonlar, vurgu (Koç/Mars) |
| `--line` | `rgba(43,33,26,.12)` | İnce ayraç çizgileri |

KURAL: Oxblood **tek** vurgu rengi. Sayfada 1-2 yerden fazla görünmez (ana CTA, aktif durum). Çoğaltırsan "ucuz" görünür.

## 4. Tipografi

- **Display / başlıklar:** Klasik serif. Öneri: EB Garamond, Cormorant veya Fraunces.
  → Türkçe glif desteği (ş, ğ, İ, ı, ö, ü, ç) MUTLAKA kontrol edilecek; eksikse alternatif.
- **Gövde:** Humanist sans. Öneri: Inter veya Work Sans (Türkçe glif tam).
- **Ölçek:** h1 ~30-40px serif / h2 ~22px / gövde 16px / küçük etiket 11-12px harf aralığı geniş (letter-spacing).
- Asla ALL CAPS başlık (yalnızca küçük etiketlerde, geniş tracking ile).
- Cümle düzeni (sentence case), her kelime baş harfi büyük DEĞİL.

## 5. Sayfa mimarisi

### Anasayfa — üç şerit (mimarlık portföyü mantığı)
Ziyaretçi tam bu sırayla ikna olur:

1. **01 — Reyon / Koleksiyon** → ne yapıyoruz. Temiz grid, az ama büyük görsel. Sergi gibi. (Han · Hanzade · Zade reyonları buradan dallanır.)
2. **02 — Atölyeden** → nasıl yapıyoruz. Kumaş, kesim, makine, eller. Güven buradan gelir (savoir-faire / Dior, Celine mantığı).
3. **03 — Etkinliklerde** → kanıt. Kesimlerin gittiği düğün/defile/sahne fotoğraflarına kısa bir bakış; "Tüm geçmiş işler" linkiyle portföy sayfasına açılır.

### Geçmiş Etkinlikler / Portföy (ayrı sayfa)
> Mimarlık ofislerinin "tamamlanmış projeler" sayfası mantığı.
> Yeteneği **iddia etmeyiz, kanıtla gösteririz.**

- Geçmişte yapılan kesimlerin/işlerin gittiği etkinlikler kronolojik veya kategorize galeri.
- Her giriş: büyük fotoğraf + kısa bağlam (ne tür iş, hangi etkinlik — kişisel isim/credential olmadan).
- **Kanıtla, iddia etme:** "X yıllık tecrübe" gibi sayısal/kişisel ifadelerden kaçın; söz yerine gerçek işlerin görselleri konuşsun. (Marka düzeyinde kalır, bireysel iddia içermez.)
- Bu sayfa sitenin en güçlü ikna ve güven aracıdır; "bizi neden seçmeli" sorusunun görsel cevabı.

### Diğer sayfalar
- Hakkımızda (atölye hikâyesi — marka düzeyinde, kişisel isim/sayısal iddia yok).
- İletişim.

## 6. İletişim & sipariş

- **Şimdi (Faz 1):** Her ürün/sayfada sabit **"WhatsApp'tan sor / sipariş ver"** CTA. Sipariş, ölçü, fiyat oradan döner. Site, çevrimiçi ödeme olmadan tam işlevseldir.
- **Sonra (Faz 2 — henüz kararlaştırılmadı):** Çevrimiçi/kredi kartı ödemesi ileride değerlendirilecek. Platform ve ödeme altyapısı (yöntem, sağlayıcı) **henüz karara bağlanmadı** — bu aşama şimdilik açık bırakıldı, brief'e teknik detay yazılmayacak.

WhatsApp butonu: marka tonuna yakın koyu yeşil/zeytin; mobilde de kolay erişilir.

## 7. Bileşen notları

- **Görsel kartları:** Köşe yarıçapı çok küçük (2px) veya keskin. Yumuşak değil, atölye gibi net.
- **Görsel alanları:** Gerçek fotoğraflar sahip tarafından sağlanacak. Şimdilik doğru en-boy oranında boş/placeholder kutular bırak (stok görsel veya AI görsel ÜRETME).
- **Hover:** Görsel hafif koyulaşır / başlık alttan belirir. Abartısız.
- **Butonlar:** Oxblood dolgu + fildişi metin VEYA çizgi (outline) buton. Köşe keskin.
- **Ayraçlar:** İnce `--line` çizgiler, bölüm numaraları (01/02/03) serif ile.
- **Mobil öncelik:** Müşteri çoğunlukla telefondan gelir. Mobilde önce test et.

## 8. Yapılacaklar (Claude Code için sıralı)

1. [ ] Token'ları CSS değişkeni / tema olarak kur.
2. [ ] Tipografi yükle, Türkçe glif doğrula.
3. [ ] Anasayfa: hero + üç şerit iskeleti (görseller için placeholder).
4. [ ] WhatsApp CTA bileşeni (her sayfada).
5. [ ] Reyon koleksiyon grid'i — Han / Hanzade / Zade reyonları (Faz 1: WhatsApp linkli ürün kartı).
6. [ ] Atölyeden bölümü.
7. [ ] Geçmiş Etkinlikler / Portföy sayfası (kanıt odaklı galeri).
8. [ ] Hakkımızda + İletişim sayfaları.

> Logo, amblem, favicon ve tüm fotoğraflar site sahibi tarafından sağlanır — Claude Code bunları üretmez, yalnızca yerleştirileceği alanı hazırlar.

---

*Referans: Sézane (ton/tipografi), Galerie Dior & Celine (atölye/süreç anlatısı), Kenny & Harlow (gelinlik + hover görsel). Hiçbiri kopyalanmaz; ilke alınır.*
