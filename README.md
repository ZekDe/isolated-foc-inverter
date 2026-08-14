# Isolated FOC Inverter

Tam izoleli, FOC (Field-Oriented Control) kontrollü üç fazlı motor sürücü donanım projesi. Tasarımın hedef çalışma sınıfı 310 V DC bara ve 10 A çıkıştır.

> [!WARNING]
> Bu proje ölümcül olabilecek yüksek gerilimler içerir. Tasarımı kurmak, enerjilendirmek veya ölçmek yalnızca uygun eğitim, izolasyon, koruyucu ekipman ve güvenli laboratuvar prosedürleriyle yapılmalıdır. Depolanmış enerji nedeniyle güç kesildikten sonra da tehlikeli gerilim bulunabilir.

## Öne çıkanlar

- Üç fazlı inverter güç katı
- İzole gate sürücüler ve izole yardımcı beslemeler
- İzole akım/gerilim ölçüm katları
- Hall sensörü ve enkoder arayüzleri
- Frenleme katı
- FOC uygulamasına uygun MCU ve geri besleme arayüzleri
- Projeye özel KiCad sembolleri, footprint'ler ve 3B modeller

## Dizin yapısı

- `inverter/`: Ana KiCad 9 projesi (`inverter.kicad_pro`), hiyerarşik şemalar, PCB ve özel kütüphaneler

## Başlangıç

1. KiCad 9 veya uyumlu daha yeni bir sürüm kurun.
2. Depoyu klonlayın.
3. `inverter/inverter.kicad_pro` dosyasını KiCad ile açın.
4. İlk açılışta özel sembol ve footprint yollarını doğrulayın.

```powershell
git clone https://github.com/<kullanici-adi>/isolated-foc-inverter.git
cd isolated-foc-inverter
```

## Ekip çalışması

Doğrudan `main` üzerinde çalışmak yerine her değişiklik için ayrı bir branch açılması ve pull request kullanılması önerilir:

```powershell
git switch -c feature/kisa-aciklama
git add .
git commit -m "Kısa ve açıklayıcı değişiklik özeti"
git push -u origin feature/kisa-aciklama
```

KiCad dosyalarında çakışmaları azaltmak için aynı şema sayfası veya PCB üzerinde eş zamanlı çalışmayı ekip içinde koordine edin. Değişiklik yapmadan önce `git pull --rebase` ile güncel sürümü alın.

## Durum

Proje aktif geliştirme aşamasındadır. Elektriksel doğrulama, izolasyon mesafeleri, termal analiz ve koruma fonksiyonları tamamlanmadan donanım üretime hazır kabul edilmemelidir.
