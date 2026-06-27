# AURA & ASH

Duyusal Gastronomi & Modern Odun Ateşi — "Quiet Luxury" restoran arayüzü.
React · Tailwind CSS · Framer Motion. Tüm UI ve state tek mega dosyada: [`src/App.jsx`](src/App.jsx).

## Çalıştırma

Node.js (18+) gerekir.

```bash
npm install
npm run dev
```

Tarayıcı otomatik açılır (http://localhost:5174). Üretim derlemesi: `npm run build` → `npm run preview`.

## Mimari

| Dosya | Görev |
|------|------|
| `index.html` | Google Fonts (Fraunces / Jost / JetBrains Mono) + Tailwind CDN (özel tema: ash/champagne renkleri, tracking ölçeği) |
| `src/main.jsx` | React kök montajı |
| `src/index.css` | Temel reset, ince scrollbar, focus halkası, `prefers-reduced-motion` |
| `src/App.jsx` | **Mega dosya** — tüm bölümler, paneller, animasyonlar ve state |

## Etkileşim haritası

- **Sol dikey nav** — Keşfet / Menü / Rezervasyon arası geçiş; **Canlı Mutfak** sağ-alt kokpiti açıp kapatır.
- **Menü** → her satırdaki **···** sağdan kayan **Duyusal Analiz Drawer**'ını açar (ürün rotası, animasyonlu makro barları, Şefin Akustiği oynatıcısı). Üstte **Filtre Laboratuvarı** (teknik + ruh hâli).
- **Rezervasyon** → salon seçimi (**Hearth / Greenhouse / Void**) sitenin **vurgu rengini canlı evriltir**; masa seç → altında akordeon (aydınlatma sanal masayı karartır + servis tarzı); sağda **Deneyim Sepeti** anlık toplamla.
- **Easter egg** → footer'daki telif cümlesinde gizli **"mahzen"** kelimesine **3 kez** tıkla → sinematik geçişle **The Secret Cellar**.
- **Esc** üstteki paneli kapatır.

## Notlar

- Tailwind şu an **Play CDN** ile yükleniyor (sıfır-konfig, hızlı önizleme). Prodüksiyon için Tailwind'i PostCSS ile build'e almanız önerilir.
- Tüm animasyonlar `prefers-reduced-motion` ile sönümlenir.
