# PuanBak

TV+ (veya başka bir uygulama) üzerinden "Paylaş" dediğinde çıkan listede görünen, film/dizi puanlarını gösteren küçük bir web uygulaması (PWA).

## Kurulum (bir kez)

1. **Anahtarları al (ücretsiz):**
   - TMDB: https://www.themoviedb.org/settings/api (v3 API Key)
   - OMDb: https://www.omdbapi.com/apikey.aspx (günde 1000 istek)
2. **HTTPS bir yere yükle.** Paylaşım menüsünde görünmesi için HTTPS şart. En kolayı:
   - GitHub Pages: yeni repo aç, bu klasördeki dosyaları yükle, Settings > Pages > main branch.
   - ya da Netlify Drop (https://app.netlify.com/drop): klasörü sürükle bırak.
3. **Telefonda Chrome ile siteyi aç** > menü > "Ana ekrana ekle" / "Uygulamayı yükle".
4. Uygulamayı aç, sağ üstteki ⚙ ile iki anahtarı gir.
5. TV+'ta bir filmde Paylaş > **PuanBak**. Puanlar otomatik gelir.

## Nasıl çalışır

- Paylaşılan metindeki tırnak içi ad (örn. "Sörfçü") ya da TV+ bağlantısındaki adres çıkarılır.
- TMDB'de aranır (Türkçe başlık/özet, poster, TMDB puanı, Türkiye'de nerede izlenir).
- TMDB'den IMDb kodu alınır, OMDb ile IMDb, Rotten Tomatoes ve Metacritic puanı çekilir.
- Hepsinin ortalaması "genel görünüm" olarak gösterilir.
- sinemalar.com ve Letterboxd için resmi API olmadığından bu kartlar ilgili aramayı açar.

## Notlar

- Anahtarlar sadece telefonundaki tarayıcıda saklanır; sonuçlar 3 gün önbelleğe alınır.
- Yanlış film çıkarsa altındaki "Başka sonuç mu?" düğmelerinden doğrusunu seç.
