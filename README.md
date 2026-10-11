# LANKA

Tek dosyalık, mobil öncelikli orderbook izleme ekranı. `index.html` doğrudan açılabilir veya herhangi bir statik sunucuyla çalıştırılabilir.

## İçerik

- Binance’in anahtarsız public WebSocket akışından canlı fiyat, mum ve ilk 20 orderbook seviyesi
- Mum grafik üzerinde alış/satış duvarlarının canlı çizgileri
- Duvar yoğunluğuna göre beş kademeli **PİRAMİT KOVALARI** görünümü
- BTC, ETH, SOL, BNB, XRP ve DOGE için ayrı model hafızası
- Orderbook imbalance, duvar yönü, duvar kalıcılığı, momentum ve spread’den üretilen deneysel yön tahmini
- Her coin için doğrulama sonucu geldikçe güncellenen ağırlıklar ve doğruluk takibi
- Öğrenilmiş verilerin `localStorage` içinde kalıcı saklanması
- Binance bağlantısı yoksa otomatik demo akışı

## Çalıştırma

```bash
python3 -m http.server 4173 --bind 0.0.0.0
```

Sonra `http://localhost:4173` adresini açın. Uygulama sunucu tarafı veya API anahtarı gerektirmez.

> Tahminler deneysel bir görselleştirmedir ve finansal tavsiye değildir. Tarayıcı verileri temizlenirse coin hafızası da silinir.
