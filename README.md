# Word2Vec ve FastText Karşılaştırması
**BM5204 Doğal Dil İşleme — Hafta 6 Ödevi**  
Ahmetcan PEKTAŞ | Bandırma Onyedi Eylül Üniversitesi

---

## Hakkında

Bu çalışmada, Wikipedia Türkçe kaynağından derlenen 450 paragraflık bir corpus üzerinde Word2Vec ve FastText modelleri eğitilmiş; beş farklı türde hedef kelime üzerinden iki model karşılaştırılmıştır. Çalışmanın temel amacı, Türkçe gibi morfolojik açıdan zengin dillerde subword temsilinin sağladığı avantajı gözlemlemektir.

## Veri Seti

Wikipedia Türkçe API'si aracılığıyla derlenen corpus; bilim, tarih ve spor kategorilerinden 150'şer paragraf (toplam 450 paragraf) içermektedir.

## Kullanılan Teknolojiler

- Python 3.10
- [gensim](https://radimrehurek.com/gensim/) — Word2Vec ve FastText modelleri
- pandas, matplotlib — veri işleme ve görselleştirme
- nltk — tokenizasyon

## Dosyalar

| Dosya | Açıklama |
|-------|----------|
| `Hafta6_Embedding_Karsilastirma.ipynb` | Model eğitimi ve analiz kodu |
| `Emmbeding_Rapor.pdf` | Araştırma raporu |

## Temel Bulgular

- FastText, Türkçe'nin eklemeli yapısına Word2Vec'e kıyasla belirgin biçimde daha iyi uyum sağlamaktadır.
- 'Kimyasal' ve 'futbol' örneklerinde FastText morfolojik akrabalıkları başarıyla temsil etti.
- Her iki model de çok anlamlılık (polisemi) problemini çözemedi — bu problem ancak BERT gibi bağlamsal modellerle ele alınabilmektedir.

## Kurs Bilgisi

Bu çalışma, BM5204 Doğal Dil İşleme dersi kapsamında hazırlanmıştır.  
Hafta 3 ödevi ile bağlantılıdır: aynı corpus üzerinde önceki haftada TF-IDF sparse temsil kullanılmış, bu haftada dense embedding yöntemleri uygulanmıştır.
