[guide-for-SDXL](https://github.com/suncommq/guide-for-SDXL)
# Stable Diffusion 가이드 | 스테이블 디퓨전 설치 및 사용법

이 저장소에서는 **Stable Diffusion** 설치, 사용법, 프롬프트 엔지니어링 및 모델 튜닝 방법을 다룹니다.  
Stable Diffusion 설치 방법  
스테이블 디퓨전 프롬프트 예제  
 AI 이미지 생성 팁 & 노하우  

## 주요 내용
- Stable Diffusion 설치 
- Web UI 사용법 (AUTOMATIC1111)
- LoRA & ControlNet 튜닝 가이드
- 최고의 프롬프트 작성법
- AI 아트 생성 꿀팁

# \<Stable Diffusion Practical Guide Table of Contents\> 

[Prompt-example page view](https://www.sdexample.com/p/prompt-collection.html)

[google keep](https://keep.google.com/)

Thank you for visiting my blog. I will create this blog so that anyone interested in image generation AI can learn the basics of image generation AI software Stable Diffusion.

Released in August 2022 based on Stability AI, Stable Diffusion is free for anyone to use and can generate 'all kinds of images' with machine learning-based inference. It can be said to be the foresight of mankind that has learned images and aesthetics from all over the world. However, if you don't know how to use it, it will be difficult to get satisfactory results, and it can also become an evil technology that harms others.  
I will write in as much detail as possible so that you can understand and properly utilize AI technology, a tool that can produce high-quality digital illustrations faster. I hope you will use it as a 'convenient blog' that helps you learn functions you didn't know about and learn 'tips' in a short period of time in the form of a manual.  
I hope you will study, take notes, and share it with your colleagues.

We welcome middle and high school students who want to study this field professionally, as well as those who want to 'make pretty pictures' as a hobby, 'those who want to make it a hobby after retirement', and those who have pure aesthetic and intellectual curiosity. This blog can also be used by office workers who want to display their talents in various opportunities, such as when creating key visuals for presentations that convey a worldview and have an impact, when creating illustrations containing messages for coworkers, superiors, and managers, when creating comics featuring unique characters of companies and local governments, and when creating concept art. Let's study.

There are several versions of the image generation model Stable Diffusion. This article mainly explains the creation of digital illustrations using Stable Diffusion XL (SDXL) and AUTOMATIC1111/Stable Diffusion WebUi.

It is not intended for those who are familiar with GPU, Python, or machine learning-related technologies, and it does not assume expensive equipment investments. From the perspective of 'allowing basic knowledge, skills, and expressions to be used for a long time,' we prioritize 'easy-to-learn methods'. We prioritize avoiding parts that readers can easily make mistakes in and including 'tips' that can improve production quality so that readers can obtain practical and stable results.

Therefore, in my blog, we use SDXL and Google Colaboratory (Colab) as standard environments for easy reference even for beginners or casual users, and explain assuming an environment where GPU is not necessary.  
Anyone with a Google account can experience the image generation AI even without prior knowledge or environment construction skills. In addition, even if you have no programming knowledge at all, you can acquire the know-how to create your own comfortable environment by modifying the script yourself.

On the other hand, creators who utilize image generation AI must comply with laws and regulations, and the ethics of 'not causing trouble to others', risk management, and accountability.

While creating the blog for you, I actually checked the accuracy and operation of the content, but I cannot guarantee the accuracy of expression, future changes, changes in the external environment, etc.  
Chapter 1 Let's learn about image generation AI  
[1-1 Let's create images with AI](https://sdexample.com/2025/02/1-1-lets-create-image-with-ai.html)  
[1-2 The birth and evolution of image generation AI](https://www.sdexample.com/2025/02/1-2-birth-and-evolution-of-image.html)  
[1-3 Let's think about the 'definition of AI' at the present time](https://www.sdexample.com/2025/02/1-3-lets-think-about-definition-of-ai.html)  
[1-4 Let's learn about artificial neural networks](https://www.sdexample.com/2025/02/1-4-lets-learn-about-artificial-neural.html)  
[1-5 Let's learn about the principle of image generation by the diffusion model](https://www.sdexample.com/2025/02/1-5-lets-learn-about-principle-of-image.html)

Chapter 2 Let's start building the environment  
[2-1 Let's prepare the environment to use Stable Diffusion](https://www.sdexample.com/2025/02/2-1-lets-prepare-environment-to-use.html)  
[2-2 Let's build the environment using Google Colab](https://www.sdexample.com/2025/02/2-2-setting-up-environment-to-try-in.html)  
2-3 Let's build the Stability Matrix in the local environment  
[2-4 Let's create images with simple words](https://sdexample.com/2025/02/2-4-create-images-with-simple-words.html)  
[2-5 Download the model](https://www.sdexample.com/2025/02/2-5-download-model.html)  
[2-6 Download the VAE](https://www.sdexample.com/2025/02/2-6-download-vae.html)

Chapter 3 Let's create images with prompts  
[3-1 Create images as you think using prompts](https://www.sdexample.com/2025/02/3-1-use-prompts-to-create-images-of.html)  
[3-2 Build negative prompts](https://www.sdexample.com/2025/02/3-2-build-negative-prompts.html)  
[3-3 Let's create images 'as you think'](https://www.sdexample.com/2025/02/3-3-lets-create-image-as-you-think.html)  
[3-4 Let's increase the resolution of the image](https://www.sdexample.com/2025/02/3-4-increase-resolution-of-image.html)  
[3-5 Let's adjust various parameters](https://www.sdexample.com/2025/02/3-5-lets-adjust-various-parameters.html)  
[3-6 Let's test various prompts](https://www.sdexample.com/2025/02/3-6-lets-test-various-prompts.html)

Chapter 4 Let's create images using images  
[4-1 You can do it with img2img Let's figure out what's there](https://www.sdexample.com/2025/03/4-1-lets-figure-out-what-you-can-do.html)  
[4-2 Let's create an image using Sketch](https://www.sdexample.com/2025/03/4-2-lets-create-image-using-sketch.html)  
[4-3 Let's edit an image using Inpaint](https://www.sdexample.com/2025/03/4-3-lets-edit-image-with-inpaint.html)  
[4-4 Apply Inpaint to modify an image](https://www.sdexample.com/2025/03/4-4-modify-images-using-inpaint.html)  
[4-5 Extend an image using Outpainting](https://www.sdexample.com/2025/03/4-5-expand-image-with-outpaingting.html)  
[4-6 Increase the resolution of an image using img2img](https://www.sdexample.com/2025/03/4-6-increase-image-resolution-with.html)  
[4-7 Let's upscale with the extension function](https://www.sdexample.com/2025/03/4-7-lets-upscale-with-extension.html)

Chapter 5 Let's use ControlNet  
5-1 Let's learn about ControlNet  
5-2 Download and prepare ControlNet  
5-3 Create an image using ControlNet  
5-4 Understand the role of the preprocessor

Chapter 6 Let's create and use LoRA  
6-1 Let's learn what we can do with additional learning  
6-2 Let's create an image using LoRA  
6-3 Create your own dedicated painting style LoRA  
6-4 Let's create various types of LoRA  
6-5 Let's evaluate the learning content

Chapter 7 Let's use the image generation AI more

Use and caution of image generation AI  
AUTOMATIC1111/WebUI Recommended extension Function

Related Terms

---

* # [Stable Diffusion WebUI Installation Errors & Solutions Summary](https://www.sdexample.com/2025/02/stable-diffusion-webui-installation.html)

* # [Stable Diffusion WebUI를 Python 3.10 환경으로 변경하는 방법](https://www.sdexample.com/2025/02/stable-diffusion-webui-python-310.html)

---

# 스테이블 디퓨젼 프롬프트 작성 가이드

* 주제 (Theme):  
  \- 주제를 명확하게 정의하여 이미지의 전체적인 분위기와 목적을 설정합니다.  
    \- 예: "가을의 숲속 풍경" 또는 "미래 도시의 야경"  
    
* 이미지 종류 (Type of Image):  
  \- 이미지의 유형을 구체적으로 명시합니다. 예를 들어, 사진, 일러스트, 캐릭터 디자인 등.  
    \- 예: "사실적인 사진", "만화 스타일 일러스트", "캐릭터 디자인"  
    
* 스타일 (Style):  
  \- 이미지의 스타일을 구체적으로 기술합니다. 예를 들어, 사실적, 추상적, 빈티지, 현대적 등.  
    \- 예: "사실적인", "추상적인", "레트로 빈티지", "현대 미니멀리즘"  
    
* 해상도 (Resolution):  
  \- 원하는 해상도를 명확히 합니다. DPI나 픽셀 단위로 해상도를 지정할 수 있습니다.  
    \- 예: "300 DPI", "1920x1080 픽셀"  
    
* 색상 (Color):  
  \- 색상 팔레트나 특정 색상을 명시합니다. 분위기에 맞는 색상 조합을 제안합니다.  
    \- 예: "따뜻한 색조 (오렌지, 빨강, 노랑)", "차가운 색조 (파랑, 녹색)", "흑백"  
    
* 조명 (Lighting):  
  \- 조명의 유형과 위치를 설명하여 이미지의 명암과 분위기를 조절합니다.  
    \- 예: "부드러운 자연광", "강렬한 스포트라이트", "어두운 그림자"

-  최적화된 조합 작성 방법

  1\. 주제와 스타일의 일관성 유지:

    \- 주제와 스타일이 서로 잘 어울리도록 합니다. 예를 들어, 미래 도시를 표현하는 주제라면 현대적이고 미래지향적인 스타일이 잘 어울립니다.

      \- 예: 주제 "미래 도시"와 스타일 "현대적, 미래지향적"


  2\. 색상 팔레트 선택:

    \- 색상은 이미지의 감정과 분위기를 결정하는 중요한 요소입니다. 주제와 스타일에 맞는 색상 팔레트를 선택하여 일관성을 유지합니다.

      \- 예: 따뜻한 색조는 감성적이고 따뜻한 느낌을, 차가운 색조는 차분하고 이성적인 느낌을 줄 수 있습니다.


  3\. 해상도와 이미지 종류:

    \- 이미지의 목적에 따라 해상도를 조절합니다. 인쇄용 이미지는 높은 해상도가 필요하고, 웹용 이미지는 상대적으로 낮은 해상도로도 충분합니다.

      \- 예: 인쇄용 브로슈어에서는 300 DPI, 웹 배너에서는 72 DPI


  4\. 조명과 그림자의 조화:

    \- 조명은 이미지의 명암과 깊이를 결정하는 요소입니다. 원하는 분위기에 맞는 조명을 선택하고, 그림자를 적절히 활용하여 입체감을 부여합니다.

      \- 예: 따뜻한 분위기를 원한다면 부드러운 자연광을 사용하고, 드라마틱한 효과를 원한다면 강렬한 스포트라이트를 사용할 수 있습니다.


   3\. 최적화된 조합 예시


  예시 1: 따뜻한 겨울 저녁

      markdown

    \-  주제: 따뜻한 겨울 저녁

    \- 이미지 종류: 사실적인 사진

    \- 스타일: 따뜻하고 포근한

    \- 해상도: 1920x1080 픽셀

    \- 색상: 따뜻한 색조 (오렌지, 빨강, 갈색)

    \- 조명: 부드러운 자연광, 벽난로 불빛

    


  예시 2: 미래의 도시 풍경

      markdown

    \- 주제: 미래의 도시 풍경

    \- 이미지 종류: 사실적인 사진

    \- 스타일: 현대적, 미래지향적

    \- 해상도: 4K 해상도 (3840x2160 픽셀)

    \- 색상: 차가운 색조 (파랑, 은색)

    \- 조명: 강렬한 네온 조명, 어두운 그림자

 

---

#  이미지 생성 도구 추천

[Toolzu](https://toolzu.com/image/combiner/)  
\- 미리 제작된 템플릿을 사용하여 사진을 결합할 수 있는 온라인 이미지 결합 도구입니다.  
\- 이미지를 세로 또는 가로로 배치하고, 크기를 조정하며, 독특한 테두리와 색상을 추가할 수 있습니다.

[Dzine.AI](https://www.dzine.ai/tools/combine-images-with-ai/)  
\- 인공지능을 활용한 이미지 병합 도구로, 쉽게 이미지를 결합할 수 있습니다.  
\- 직관적인 드래그 앤 드롭 기능, 스타일 선택 및 광범위한 편집 도구를 제공합니다.

[LightX](https://www.lightxeditor.com/photo-editing/blend-images-online/)  
\- 여러 이미지를 간단히 블렌드할 수 있는 온라인 사진 블렌더 도구입니다.  
\- 불투명도, 레이어링 및 필터를 조정하여 원본 해상도와 품질을 유지하면서 이미지를 결합할 수 있습니다.

---

# 스테이블 디퓨젼과 관련된 최신 정보와 다양한 예제를 얻기 위해 참여할 수 있는 몇 가지 커뮤니티를 소개합니다.

[디시인사이드 스테이블 디퓨전 마이너 갤러리](https://gall.dcinside.com/mgallery/board/lists/?id=stablediffusion&form=MG0AV3)

* 이 갤러리는 스테이블 디퓨젼에 대한 다양한 정보와 예제를 공유하는 커뮤니티입니다. 사용자들이 직접 생성한 이미지와 프롬프트를 공유하고, 문제 해결을 위한 토론도 활발히 이루어집니다.

[스테이블 디퓨전 위키](https://gall.dcinside.com/mgallery/board/view/?id=stablediffusion&no=5)

* 스테이블 디퓨젼에 대한 다양한 정보를 제공하는 위키 페이지입니다. 설치 방법, 프롬프트 작성 가이드, 모델 학습 방법 등 유용한 정보를 찾을 수 있습니다.

[스테이블 디퓨전 빠른 시작 가이드](https://gall.dcinside.com/mgallery/board/view/?id=stablediffusion&no=3)

* 스테이블 디퓨젼을 처음 사용하는 사용자들을 위한 빠른 시작 가이드입니다. 기본적인 사용법부터 고급 기능까지 다양한 정보를 제공합니다.

[Reddit \- Stable Diffusion](https://www.reddit.com/r/StableDiffusion/):

* 스테이블 디퓨젼에 대한 다양한 정보와 예제를 공유하는 글로벌 커뮤니티입니다. 사용자들이 직접 생성한 작품을 공유하고, 팁과 트릭을 나누며, 문제 해결을 위한 토론이 활발히 이루어집니다.

[Discord \- Stable Diffusion](https://discord.com/invite/stablediffusion):

* 스테이블 디퓨젼 사용자들이 실시간으로 소통할 수 있는 디스코드 서버입니다. 다양한 주제의 채널이 있으며, 최신 뉴스와 업데이트, 문제 해결, 예제 공유 등 다양한 활동이 이루어지고 있습니다.

[Twitter \- \#StableDiffusion](https://twitter.com/search?q=%23StableDiffusion&src=typed_query):

* 트위터에서 \#StableDiffusion 해시태그를 사용하여 관련된 최신 소식과 사용자들이 생성한 이미지를 볼 수 있습니다. 이를 통해 다양한 아이디어와 예제를 얻을 수 있습니다.

[GitHub \- Stable Diffusion Projects](https://github.com/CompVis/stable-diffusion):

* 스테이블 디퓨젼 관련 프로젝트와 코드를 공유하는 깃허브 페이지입니다. 오픈 소스 프로젝트에 기여하거나, 다른 사용자들이 공유한 코드를 참고하여 자신의 프로젝트를 발전시킬 수 있습니다.

---

## **추가 학습 자료**

* **Stable Diffusion 공식 문서**: [https://stablediffusionweb.com/](https://stablediffusionweb.com/)  
* **AUTOMATIC1111 Web UI 설정 가이드**: [GitHub](https://github.com/AUTOMATIC1111/stable-diffusion-webui/wiki)  
* **ComfyUI 튜토리얼**: [ComfyUI Docs](https://github.com/comfyanonymous/ComfyUI/wiki)

## **Stable Diffusion 설치 및 실행**

### **1\) 로컬 설치 방법**

로컬에서 Stable Diffusion을 실행하려면 아래 방법 중 하나를 선택할 수 있습니다.

* **AUTOMATIC1111 Web UI** (추천)  
  * 사용하기 쉬운 인터페이스 제공  
  * 다양한 기능 및 플러그인 지원  
  * 설치 방법: [GitHub 링크](https://github.com/AUTOMATIC1111/stable-diffusion-webui)  
* **ComfyUI** (노드 기반 편집기)  
  * 노드 그래프 방식으로 이미지 생성 가능  
  * 설치 방법: [GitHub 링크](https://github.com/comfyanonymous/ComfyUI)  
* **Diffusers (Hugging Face 라이브러리 활용)**  
  * Python 코드로 직접 모델 실행 가능  
  * 설치 방법: [Hugging face 링크](https://huggingface.co/docs/diffusers/ko/installation)

### **2\) Colab을 이용한 실행**

로컬에 설치하지 않고 구글 Colab에서 실행할 수도 있습니다.

* **AUTOMATIC1111 Colab 버전**: [Colab 링크](https://colab.research.google.com/github/TheLastBen/fast-stable-diffusion/blob/main/fast_stable_diffusion_AUTOMATIC1111.ipynb)  
* **ComfyUI Colab 버전**: [Colab 링크](https://colab.research.google.com/drive/1kuilnPPH_kpWAwgsR_btSLDtMcUs5mVp?usp=sharing)

---

# Stable Diffusion의 다양한 모델과 그 특징

Stable Diffusion은 텍스트 설명을 기반으로 이미지를 생성하는 딥 러닝 모델로, 여러 버전이 출시되면서 성능과 기능이 향상되어 왔습니다. 주요 버전과 그 특징은 다음과 같습니다:

* ### 1\. Stable Diffusion 1.4

    \- 출시일: 2022년 8월  
    \- 특징: CompVis에서 출시한 초기 버전으로, 512x512 픽셀 해상도의 이미지를 생성할 수 있습니다.

* ### 2\. Stable Diffusion 1.5

    \- 출시일: 2022년 10월  
    \- 특징: RunwayML에서 출시한 버전으로, 이전 버전과 유사한 기능을 제공합니다.

* ### 3\. Stable Diffusion 2.0

    \- 출시일: 2022년 11월  
    \- 특징: 새로운 데이터셋으로 처음부터 재훈련되었으며, 768x768 픽셀 해상도의 이미지를 생성할 수 있습니다.

* ### 4\. Stable Diffusion 2.1

    \- 출시일: 2022년 12월  
    \- 특징: 2.0 버전을 기반으로 한 개선된 버전입니다.

* ### 5\. Stable Diffusion XL 1.0 (SDXL 1.0)

    \- 출시일: 2023년 7월  
    \- 특징: 35억 개의 파라미터를 보유한 대형 모델로, 이전 버전보다 약 3.5배 큰 규모입니다. 1024x1024 픽셀 해상도의 고품질 이미지를 생성할 수 있습니다.

* ### 6\. Stable Diffusion XL Turbo (SDXL Turbo)

    \- 출시일: 2023년 11월  
    \- 특징: SDXL 1.0을 기반으로 증류(distillation) 기법을 적용하여, 더 적은 확산 단계(diffusion steps)로 빠르게 이미지를 생성할 수 있습니다.

* ### 7\. Stable Diffusion 3.0

    \- 출시일: 2024년 2월 (초기 프리뷰)  
    \- 특징: 800M에서 80억 개의 파라미터를 가진 다양한 모델로 구성된 모델 패밀리입니다. 새로운 아키텍처인 Rectified Flow Transformer를 도입하여 성능을 향상시켰습니다.

* ### 8\. Stable Diffusion 3.5

    \- 출시일: 2024년 10월  
    \- 특징: 80억 개의 파라미터를 가진 Large 모델, 이를 증류한 Large Turbo 모델, 그리고 25억 개의 파라미터를 가진 Medium 모델 등 다양한 버전으로 제공됩니다. 이미지 생성의 품질과 속도가 크게 향상되었습니다.

---

# Stable Diffusion 모델을 활용하기 위한 권장 시스템 사양. 

각 버전에 따라 요구되는 하드웨어 사양이 다를 수 있으므로, 아래 정보를 참고하시어 최적의 환경을 구축하시기 바랍니다.

* 1\. Stable Diffusion 1.x 시리즈

  \- GPU 메모리: 최소 4GB의 VRAM이 필요하며, 6GB 이상의 VRAM을 권장합니다.

  \- 예시: NVIDIA GTX 1660 또는 RTX 2060 이상

* 2\. Stable Diffusion 2.x 시리즈

  \- GPU 메모리: 최소 6GB의 VRAM이 필요하며, 8GB 이상의 VRAM을 권장합니다.

  \- 예시: NVIDIA RTX 3060 또는 RTX 3070 이상

* 3\. Stable Diffusion XL 1.0 (SDXL 1.0)

  \- GPU 메모리: 최소 8GB의 VRAM이 필요하며, 12GB 이상의 VRAM을 권장합니다.

  \- 예시: NVIDIA RTX 3080 또는 RTX 3090 이상

* 4\. Stable Diffusion XL Turbo (SDXL Turbo)

  \- GPU 메모리: 최소 8GB의 VRAM이 필요하며, 12GB 이상의 VRAM을 권장합니다.

  \- 예시: NVIDIA RTX 3080 또는 RTX 3090 이상

* 5\. Stable Diffusion 3.0 및 3.5

  \- GPU 메모리: 최소 10GB의 VRAM이 필요하며, 16GB 이상의 VRAM을 권장합니다.

  \- 예시: NVIDIA RTX 3090 또는 RTX 4090 이상

* 공통 권장 사양:

  \- CPU: Intel Core i7 10세대 이상 또는 AMD Ryzen 7 3700X 이상

  \- RAM: 16GB 이상 (32GB 권장)

  \- 저장 공간: SSD 500GB 이상

  \- 운영체제: Windows 10 64-bit, Ubuntu 20.04 LTS 또는 macOS 11.0 이상

* 참고 사항:

  \- Stable Diffusion은 GPU 성능에 크게 의존하므로, VRAM 용량이 충분한 고성능 GPU를 사용하는 것이 중요합니다.

  \- 로컬 환경에서의 실행이 어려운 경우, \[[Stable Diffusion Online](https://stablediffusionweb.com/ko)\]과 같은 웹 기반 서비스를 활용하여 모델을 사용할 수 있습니다.

  시스템 사양은 모델의 복잡도와 해상도에 따라 달라질 수 있으므로, 사용하려는 모델과 작업에 맞게 시스템을 구성하시기 바랍니다. 


---

#### 관련기사

[Stability AI Announces Stable Diffusion XL 1.0, Featured on Amazon Bedrock](https://youtu.be/lPuJojDe5Q0)

[안드로이드 스마트폰 최초 LoRA 기술 구동 |  스테이블 디퓨전](https://youtu.be/mNdeC4V9m9I)

---

#### **학술정보**

구글 스칼라 스테이블 디퓨젼 학술 정보 검색  
[Google scholar](https://scholar.google.com/scholar?hl=ko&as_sdt=0%2C5&as_ylo=2025&q=stable+diffusion+model&btnG=)

---
  

