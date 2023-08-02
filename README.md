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



     - separate prompts using uppercase `AND`
     - also supports weights for prompts: `a cat :1.2 AND a dog AND a penguin :2.2`
- No token limit for prompts (original stable diffusion lets you use up to 75 tokens)
- DeepDanbooru integration, creates danbooru style tags for anime prompts
- [xformers](https://github.com/AUTOMATIC1111/stable-diffusion-webui/wiki/Xformers), major speed increase for select cards: (add `--xformers` to commandline args)
- via extension: [History tab](https://github.com/yfszzx/stable-diffusion-webui-images-browser): view, direct and delete images conveniently within the UI
- Generate forever option
- Training tab
     - hypernetworks and embeddings options
     - Preprocessing images: cropping, mirroring, autotagging using BLIP or deepdanbooru (for anime)
- Clip skip
- Hypernetworks
- Loras (same as Hypernetworks but more pretty)
- A sparate UI where you can choose, with preview, which embeddings, hypernetworks or Loras to add to your prompt 
- Can select to load a different VAE from settings screen
- Estimated completion time in progress bar
- API
- Support for dedicated [inpainting model](https://github.com/runwayml/stable-diffusion#inpainting-with-stable-diffusion) by RunwayML
- via extension: [Aesthetic Gradients](https://github.com/AUTOMATIC1111/stable-diffusion-webui-aesthetic-gradients), a way to generate images with a specific aesthetic by using clip images embeds (implementation of [https://github.com/vicgalle/stable-diffusion-aesthetic-gradients](https://github.com/vicgalle/stable-diffusion-aesthetic-gradients))
- [Stable Diffusion 2.0](https://github.com/Stability-AI/stablediffusion) support - see [wiki](https://github.com/AUTOMATIC1111/stable-diffusion-webui/wiki/Features#stable-diffusion-20) for instructions
- [Alt-Diffusion](https://arxiv.org/abs/2211.06679) support - see [wiki](https://github.com/AUTOMATIC1111/stable-diffusion-webui/wiki/Features#alt-diffusion) for instructions
- Now without any bad letters!
- Load checkpoints in safetensors format
- Eased resolution restriction: generated image's domension must be a multiple of 8 rather than 64
- Now with a license!
- Reorder elements in the UI from settings screen

## Installation and Running
Make sure the required [dependencies](https://github.com/AUTOMATIC1111/stable-diffusion-webui/wiki/Dependencies) are met and follow the instructions available for both [NVidia](https://github.com/AUTOMATIC1111/stable-diffusion-webui/wiki/Install-and-Run-on-NVidia-GPUs) (recommended) and [AMD](https://github.com/AUTOMATIC1111/stable-diffusion-webui/wiki/Install-and-Run-on-AMD-GPUs) GPUs.

Alternatively, use online services (like Google Colab):

- [List of Online Services](https://github.com/AUTOMATIC1111/stable-diffusion-webui/wiki/Online-Services)

### Installation on Windows 10/11 with NVidia-GPUs using release package
1. Download `sd.webui.zip` from [v1.0.0-pre](https://github.com/AUTOMATIC1111/stable-diffusion-webui/releases/tag/v1.0.0-pre) and extract it's contents.
2. Run `update.bat`.
3. Run `run.bat`.
> For more details see [Install-and-Run-on-NVidia-GPUs](https://github.com/AUTOMATIC1111/stable-diffusion-webui/wiki/Install-and-Run-on-NVidia-GPUs)

### Automatic Installation on Windows
1. Install [Python 3.10.6](https://www.python.org/downloads/release/python-3106/) (Newer version of Python does not support torch), checking "Add Python to PATH".
2. Install [git](https://git-scm.com/download/win).
3. Download the stable-diffusion-webui repository, for example by running `git clone https://github.com/AUTOMATIC1111/stable-diffusion-webui.git`.
4. Run `webui-user.bat` from Windows Explorer as normal, non-administrator, user.

### Automatic Installation on Linux
1. Install the dependencies:
```bash
# Debian-based:
sudo apt install wget git python3 python3-venv
# Red Hat-based:
sudo dnf install wget git python3
# Arch-based:
sudo pacman -S wget git python3
```
2. Navigate to the directory you would like the webui to be installed and execute the following command:
```bash
bash <(wget -qO- https://raw.githubusercontent.com/AUTOMATIC1111/stable-diffusion-webui/master/webui.sh)
```
3. Run `webui.sh`.
4. Check `webui-user.sh` for options.
### Installation on Apple Silicon

Find the instructions [here](https://github.com/AUTOMATIC1111/stable-diffusion-webui/wiki/Installation-on-Apple-Silicon).

## Contributing
Here's how to add code to this repo: [Contributing](https://github.com/AUTOMATIC1111/stable-diffusion-webui/wiki/Contributing)

## Documentation

The documentation was moved from this README over to the project's [wiki](https://github.com/AUTOMATIC1111/stable-diffusion-webui/wiki).

For the purposes of getting Google and other search engines to crawl the wiki, here's a link to the (not for humans) [crawlable wiki](https://github-wiki-see.page/m/AUTOMATIC1111/stable-diffusion-webui/wiki).

## Credits
Licenses for borrowed code can be found in `Settings -> Licenses` screen, and also in `html/licenses.html` file.

- Stable Diffusion - https://github.com/CompVis/stable-diffusion, https://github.com/CompVis/taming-transformers
- k-diffusion - https://github.com/crowsonkb/k-diffusion.git
- GFPGAN - https://github.com/TencentARC/GFPGAN.git
- CodeFormer - https://github.com/sczhou/CodeFormer
- ESRGAN - https://github.com/xinntao/ESRGAN
- SwinIR - https://github.com/JingyunLiang/SwinIR
- Swin2SR - https://github.com/mv-lab/swin2sr
- LDSR - https://github.com/Hafiidz/latent-diffusion
- MiDaS - https://github.com/isl-org/MiDaS
- Ideas for optimizations - https://github.com/basujindal/stable-diffusion
- Cross Attention layer optimization - Doggettx - https://github.com/Doggettx/stable-diffusion, original idea for prompt editing.
- Cross Attention layer optimization - InvokeAI, lstein - https://github.com/invoke-ai/InvokeAI (originally http://github.com/lstein/stable-diffusion)
- Sub-quadratic Cross Attention layer optimization - Alex Birch (https://github.com/Birch-san/diffusers/pull/1), Amin Rezaei (https://github.com/AminRezaei0x443/memory-efficient-attention)
- Textual Inversion - Rinon Gal - https://github.com/rinongal/textual_inversion (we're not using his code, but we are using his ideas).
- Idea for SD upscale - https://github.com/jquesnelle/txt2imghd
- Noise generation for outpainting mk2 - https://github.com/parlance-zz/g-diffuser-bot
- CLIP interrogator idea and borrowing some code - https://github.com/pharmapsychotic/clip-interrogator
- Idea for Composable Diffusion - https://github.com/energy-based-model/Compositional-Visual-Generation-with-Composable-Diffusion-Models-PyTorch
- xformers - https://github.com/facebookresearch/xformers
- DeepDanbooru - interrogator for anime diffusers https://github.com/KichangKim/DeepDanbooru
- Sampling in float32 precision from a float16 UNet - marunine for the idea, Birch-san for the example Diffusers implementation (https://github.com/Birch-san/diffusers-play/tree/92feee6)
- Instruct pix2pix - Tim Brooks (star), Aleksander Holynski (star), Alexei A. Efros (no star) - https://github.com/timothybrooks/instruct-pix2pix
- Security advice - RyotaK
- UniPC sampler - Wenliang Zhao - https://github.com/wl-zhao/UniPC
- TAESD - Ollin Boer Bohan - https://github.com/madebyollin/taesd
- LyCORIS - KohakuBlueleaf
- Initial Gradio script - posted on 4chan by an Anonymous user. Thank you Anonymous user.
- (You)
