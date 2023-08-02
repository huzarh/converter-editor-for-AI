# Kararlı Difüzyon web kullanıcı arayüzü
Stable Diffusion için Gradio kitaplığına dayalı bir tarayıcı arabirimi.

![](ekran görüntüsü.png)

## Özellikler
[Resimlerle birlikte ayrıntılı özellik gösterimi](https://github.com/AUTOMATIC1111/stable-diffusion-webui/wiki/Features):
- Orijinal txt2img ve img2img modları
- Tek tıklamayla betiği kurun ve çalıştırın (ancak yine de python ve git'i yüklemelisiniz)
- Dış boyama
- boyama
- Renkli Taslak
- Bilgi İstemi Matrisi
- Kararlı Difüzyon Yükseltmesi
- Dikkat, modelin daha fazla dikkat etmesi gereken metin kısımlarını belirtin
     - `((smokin)` giyen bir adam - smokine daha fazla dikkat eder
     - `(smokin:1.21)` giyen bir adam - alternatif sözdizimi
     - metni seçin ve dikkati seçilen metne (anonim kullanıcı tarafından sağlanan kod) otomatik olarak ayarlamak için "Ctrl+Yukarı" veya "Ctrl+Aşağı" (veya bir MacOS kullanıyorsanız "Command+Yukarı" veya "Command+Aşağı") tuşlarına basın )
- Geri döngü, img2img işlemeyi birden çok kez çalıştırın
- X/Y/Z çizimi, farklı parametrelerle 3 boyutlu bir resim çizimi çizmenin bir yolu
- Metin Tersine Çevirme
     - istediğiniz kadar yerleştirmeye sahip olun ve onlar için istediğiniz isimleri kullanın
     - belirteç başına farklı sayıda vektör içeren birden fazla yerleştirme kullanın
     - yarı duyarlıklı kayan noktalı sayılarla çalışır
     - 8GB'ta tren yerleştirmeleri (ayrıca 6GB'ın çalıştığına dair raporlar)
- Ekstralar sekmesi:
     - GFPGAN, yüzleri düzelten sinir ağı
     - CodeFormer, GFPGAN'a alternatif olarak yüz restorasyon aracı
     - RealESRGAN, sinir ağı yükseltme
     - ESRGAN, birçok üçüncü parti modele sahip sinir ağı yükseltme aracı
     - SwinIR ve Swin2SR ([buraya bakın](https://github.com/AUTOMATIC1111/stable-diffusion-webui/pull/2092)), sinir ağı yükselticileri
     - LDSR, Gizli difüzyon süper çözünürlük yükseltme
- En boy oranı seçeneklerini yeniden boyutlandırma
- Örnekleme yöntemi seçimi
     - Örnekleyici eta değerlerini ayarlayın (gürültü çarpanı)
     - Daha gelişmiş gürültü ayarı seçenekleri
- Herhangi bir zamanda işlemeyi durdurun
- 4GB ekran kartı desteği (ayrıca 2GB'lık çalışma raporları)
- Partiler için doğru tohumlar
- Canlı bilgi istemi belirteç uzunluğu doğrulaması
- Üretim parametreleri
      - görüntüleri oluşturmak için kullandığınız parametreler o görüntüyle birlikte kaydedilir
      - PNG için PNG parçalarında, JPEG için EXIF'te
      - oluşturma parametrelerini geri yüklemek ve bunları otomatik olarak kullanıcı arayüzüne kopyalamak için görüntüyü PNG bilgi sekmesine sürükleyebilir
      - ayarlarda devre dışı bırakılabilir
      - bir resim/metin parametrelerini sürükleyip bilgi istemi kutusuna bırakın
- Oluşturma Parametrelerini Oku Düğmesi, istem kutusundaki parametreleri kullanıcı arayüzüne yükler
- Ayarlar sayfası
- Kullanıcı arabiriminden isteğe bağlı python kodu çalıştırma (etkinleştirmek için "--allow-code" ile çalıştırılmalıdır)
- Çoğu UI öğesi için fareyle üzerine gelme ipuçları
- UI öğeleri için varsayılanları/mix/maks/adım değerlerini metin yapılandırması aracılığıyla değiştirmek mümkündür
- Döşeme desteği, dokular gibi döşenebilen görüntüler oluşturmak için bir onay kutusu
- İlerleme çubuğu ve canlı görüntü oluşturma önizlemesi
     - Neredeyse sıfır VRAM veya bilgi işlem gereksinimi olmadan önizlemeler oluşturmak için ayrı bir sinir ağı kullanabilir
- Olumsuz bilgi istemi, oluşturulan resimde görmek istemediklerinizi listelemenizi sağlayan ekstra bir metin alanı
- İstemin bir bölümünü kaydetmenin ve bunları daha sonra açılır menü aracılığıyla kolayca uygulamanın bir yolu olan stiller
- Varyasyonlar, aynı görüntüyü küçük farklarla oluşturmanın bir yolu
- Tohum yeniden boyutlandırma, aynı görüntüyü ancak biraz farklı çözünürlükte oluşturmanın bir yolu
- CLIP sorgulayıcı, bir görüntüden istemi tahmin etmeye çalışan bir düğme
- Komut İstemi Düzenleme, orta nesli değiştirmenin bir yolu, diyelim ki bir karpuz yapmaya başlayın ve yarıda anime kıza geçin
- Toplu İşleme, img2img kullanarak bir grup dosyayı işleyin
- Img2img Alternatif, çapraz dikkat kontrolünün ters Euler yöntemi
- Yüksek Çözünürlük Düzeltme, her zamanki bozulmalar olmadan tek bir tıklamayla yüksek çözünürlüklü resimler üretmek için kullanışlı bir seçenek
- Anında kontrol noktalarını yeniden yükleme
- Kontrol Noktası Birleşmesi, 3 adede kadar kontrol noktasını tek bir kontrol noktasında birleştirmenize izin veren bir sekme
- Topluluktan birçok uzantı içeren [Özel komut dosyaları](https://github.com/AUTOMATIC1111/stable-diffusion-webui/wiki/Custom-Scripts)
- [Composable-Diffusion](https://energy-based-model.github.io/Compositional-Visual-Generation-with-Composable-Diffusion-Models/), aynı anda birden fazla bilgi istemi kullanmanın bir yolu



   - büyük `VE` kullanarak istemleri ayırın
      - ayrıca istemler için ağırlıkları destekler: `bir kedi :1.2 VE bir köpek VE bir penguen :2.2`
- İstemler için belirteç sınırı yok (orijinal kararlı difüzyon, 75'e kadar belirteç kullanmanıza izin verir)
- DeepDanbooru entegrasyonu, anime istemleri için danbooru tarzı etiketler oluşturur
- [xformers](https://github.com/AUTOMATIC1111/stable-diffusion-webui/wiki/Xformers), belirli kartlar için büyük hız artışı: (komut satırı argümanlarına `--xformers` ekleyin)
- uzantı aracılığıyla: [Geçmiş sekmesi](https://github.com/yfszzx/stable-diffusion-webui-images-browser): görüntüleri kullanıcı arayüzü içinde kolayca görüntüleyin, yönlendirin ve silin
- Sonsuza kadar oluştur seçeneği
- Eğitim sekmesi
      - hiper ağlar ve yerleştirme seçenekleri
      - Görüntüleri ön işleme: BLIP veya deepdanbooru (anime için) kullanarak kırpma, yansıtma, otomatik etiketleme
- Klip atlama
- hiper ağlar
- Loras (Hypernetworks ile aynı ama daha güzel)
- İsteminize hangi gömmelerin, hiper ağların veya Loras'ın ekleneceğini seçebileceğiniz, önizlemeli, ayrı bir kullanıcı arayüzü
- Ayarlar ekranından farklı bir VAE yüklemeyi seçebilir
- İlerleme çubuğunda tahmini tamamlanma süresi
- API
- RunwayML tarafından özel [inpainting model](https://github.com/runwayml/stable-diffusion#inpainting-with-stable-diffusion) desteği
- uzantı aracılığıyla: [Aesthetic Gradients](https://github.com/AUTOMATIC1111/stable-diffusion-webui-aesthetic-gradients), klip görüntü yerleştirmelerini kullanarak belirli bir estetiğe sahip görüntüler oluşturmanın bir yolu ([https uygulaması: //github.com/vicgalle/stable-diffusion-aesthetic-gradients](https://github.com/vicgalle/stable-diffusion-aesthetic-gradients))
- [Stable Diffusion 2.0](https://github.com/Stability-AI/stablediffusion) desteği - bkz. [wiki](https://github.com/AUTOMATIC1111/stable-diffusion-webui/wiki/Features#stable- difüzyon-20) talimatlar için
- [Alt-Diffusion](https://arxiv.org/abs/2211.06679) desteği - bkz. [wiki](https://github.com/AUTOMATIC1111/stable-diffusion-webui/wiki/Features#alt-diffusion) talimatlar için
- Artık kötü mektuplar olmadan!
- Güvenli tensör formatında kontrol noktalarını yükleyin
- Kolaylaştırılmış çözünürlük kısıtlaması: oluşturulan görüntünün hakimiyeti 64 yerine 8'in katı olmalıdır
- Şimdi bir lisansla!
- Kullanıcı arabirimindeki öğeleri ayarlar ekranından yeniden sıralayın

## Kurulum ve Çalıştırma
Gerekli [bağımlılıkların](https://github.com/AUTOMATIC1111/stable-diffusion-webui/wiki/Dependencies) karşılandığından emin olun ve her iki [NVidia](https://github.com/AUTOMATIC1111) için mevcut talimatları izleyin. /stable-diffusion-webui/wiki/Install-and-Run-on-NVidia-GPUs) (önerilir) ve [AMD](https://github.com/AUTOMATIC1111/stable-diffusion-webui/wiki/Install-and -Run-on-AMD-GPU'lar) GPU'lar.

Alternatif olarak, çevrimiçi hizmetleri (Google Colab gibi) kullanın:

- [Çevrimiçi Hizmetlerin Listesi](https://github.com/AUTOMATIC1111/stable-diffusion-webui/wiki/Online-Services)

### Sürüm paketi kullanılarak NVidia-GPU'larla Windows 10/11'e kurulum
1. [v1.0.0-pre](https://github.com/AUTOMATIC1111/stable-diffusion-webui/releases/tag/v1.0.0-pre) adresinden `sd.webui.zip` dosyasını indirin ve içeriğini çıkarın.
2. `update.bat`ı çalıştırın.
3. `run.bat`ı çalıştırın.
> Daha fazla ayrıntı için bkz.

### Windows'ta Otomatik Kurulum
1. [Python 3.10.6](https://www.python.org/downloads/release/python-3106/) yükleyin (Python'un daha yeni sürümü meşaleyi desteklemez), "Python'u PATH'e Ekle"yi işaretleyin.
2. [git](https://git-scm.com/download/win) yükleyin.
3. Stable-diffusion-webui deposunu indirin, örneğin "git clone https://github.com/AUTOMATIC1111/stable-diffusion-webui.git" komutunu çalıştırarak.
4. Windows Explorer'dan "webui-user.bat" dosyasını yönetici olmayan normal bir kullanıcı olarak çalıştırın.

### Linux'ta Otomatik Kurulum
1. Bağımlılıkları kurun:
``` bash
# Debian tabanlı:
sudo apt kurulum wget git python3 python3-venv
# Red Hat tabanlı:
sudo dnf wget'i kurun git python3
# Arch tabanlı:
sudo pacman -S wget git python3
```
2. Webui'nin kurulmasını istediğiniz dizine gidin ve aşağıdaki komutu çalıştırın:
``` bash
bash <(wget -qO- https://raw.githubusercontent.com/AUTOMATIC1111/stable-diffusion-webui/master/webui.sh)
```
3. "webui.sh"yi çalıştırın.
4. Seçenekler için "webui-user.sh" dosyasını kontrol edin.
### Apple Silicon'a Kurulum

Talimatları [burada](https://github.com/AUTOMATIC1111/stable-diffusion-webui/wiki/Installation-on-Apple-Silicon) bulun.

## Katkı
Bu depoya nasıl kod ekleyeceğiniz aşağıda açıklanmıştır: [Katkıda Bulunma](https://github.com/AUTOMATIC1111/stable-diffusion-webui/wiki/Contributing)

## Dokümantasyon

Belgeler, bu BENİOKU'dan projenin [wiki](https://github.com/AUTOMATIC1111/stable-diffusion-webui/wiki) sayfasına taşındı.

Google'ın ve diğer arama motorlarının wiki'yi taramasını sağlamak amacıyla, (insanlar için değil) [taranabilir wiki](https://github-wiki-see.page/m/AUTOMATIC1111/stable-diffusion-) bağlantısını burada bulabilirsiniz. webui/wiki).
## Kredi
Ödünç alınan kod için lisanslar, "Ayarlar -> Lisanslar" ekranında ve ayrıca "html/licenses.html" dosyasında bulunabilir.

- Kararlı Difüzyon - https://github.com/CompVis/stable-diffusion, https://github.com/CompVis/taming-transformers
- k-difüzyon - https://github.com/crowsonkb/k-diffusion.git
- GFPGAN - https://github.com/TencentARC/GFPGAN.git
- CodeFormer - https://github.com/sczhou/CodeFormer
- ESRGAN - https://github.com/xinntao/ESRGAN
- SwinIR - https://github.com/JingyunLiang/SwinIR
- Swin2SR - https://github.com/mv-lab/swin2sr
- LDSR - https://github.com/Hafiidz/latent-diffusion
- MiDaS - https://github.com/isl-org/MiDaS
- Optimizasyon fikirleri - https://github.com/basujindal/stable-diffusion
- Çapraz Dikkat katmanı optimizasyonu - Doggettx - https://github.com/Doggettx/stable-diffusion, hızlı düzenleme için orijinal fikir.
- Çapraz Dikkat katmanı optimizasyonu - InvokeAI, lstein - https://github.com/invoke-ai/InvokeAI (başlangıçta http://github.com/lstein/stable-diffusion)
- İkinci dereceden Çapraz Dikkat katmanı optimizasyonu - Alex Birch (https://github.com/Birch-san/diffusers/pull/1), Amin Rezaei (https://github.com/AminRezaei0x443/memory-efficiency-attention)
- Metin Tersine Çevirme - Rinon Gal - https://github.com/rinongal/textual_inversion (onun kodunu kullanmıyoruz ama fikirlerini kullanıyoruz).
- SD yükseltme fikri - https://github.com/jquesnelle/txt2imghd
- mk2'yi boyamak için gürültü üretimi - https://github.com/parlance-zz/g-diffuser-bot
- CLIP sorgulayıcı fikri ve bazı kodların ödünç alınması - https://github.com/pharmapsychotic/clip-interrogator
- Şekillendirilebilir Difüzyon için Fikir - https://github.com/energy-based-model/Compositional-Visual-Generation-with-Composable-Diffusion-Models-PyTorch
- xformers - https://github.com/facebookresearch/xformers
- DeepDanbooru - anime yayıcılar için sorgulayıcı https://github.com/KichangKim/DeepDanbooru
- Bir float16 UNet'ten float32 hassasiyetinde örnekleme - fikir için marunine, örnek Diffusers uygulaması için Birch-san (https://github.com/Birch-san/diffusers-play/tree/92feee6)
- Talimat pix2pix - Tim Brooks (yıldız), Aleksander Holynski (yıldız), Alexei A. Efros (yıldız yok) - https://github.com/timothybrooks/instruct-pix2pix
- Güvenlik tavsiyesi - RyotaK
- UniPC örnekleyici - Wenliang Zhao - https://github.com/wl-zhao/UniPC
- TAESD - Ollin Boer Bohan - https://github.com/madebyollin/taesd
- LyCORIS - KohakuBlueleaf
- İlk Gradio betiği - 4chan'da Anonim bir kullanıcı tarafından yayınlandı. Teşekkürler Anonim kullanıcı.
