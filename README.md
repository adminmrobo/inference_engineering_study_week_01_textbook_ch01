# AI Lab Explainer — 추론 엔지니어링 시리즈

LLM 추론 서빙의 지연시간·처리량·단위 경제학 균형을 다루는 인터랙티브 교육 HTML 시리즈입니다. 모든 페이지는 그림·데이터·스크립트를 한 파일에 담아(base64) 빌드 없이 브라우저로 바로 열립니다.

**바로 보기:** https://adminmrobo.github.io/&lt;저장소&gt;/  ← 배포 후 실제 주소를 넣어 주세요

**저자:** 글 · 안상선 ((주)M-Robo 대표)
**라이선스:** CC BY-NC 4.0

**언어:** [한국어](#ko) · [English](#en) · [中文](#zh) · [日本語](#ja) · [Oʻzbekcha](#uz) · [Русский](#ru) · [Tiếng Việt](#vi)

---

<a id="ko"></a>
## 한국어

### 구성

| 편 | 파일 | 다루는 내용 | 난이도 |
|---|---|---|---|
| 첫 화면 | `index.html` | 시리즈 소개 · 미션 목록 · 진도 체크 | — |
| 교과서 1장 | `01_inference_prerequisites.html` | 공유 API vs 전용 GPU 손익분기, 도메인 파인튜닝과 증류, TTFT·TPS·P99 실습과 끝장 대결 | ★★★☆☆ |

**1장의 학습 경로** — 들어가는 것: 토큰 과금과 GPU 임대의 기초. 나오는 것: 손익분기점 계산법, 파인튜닝·증류의 차이, P99 꼬리 지연의 의미. 다음 질문: "배치와 큐잉을 더 들여다보려면?"

**핵심 숫자:** 월 지출 $780(전용 3B) vs $3,600(프론티어 API) · 손익분기 약 1,200만 토큰/일. 페이지 안의 모든 숫자는 슬라이더·버튼 실습과 같은 계산으로 그려집니다(설명용 모형 한계는 각 페이지 푸터 참고).

**각 편에 들어 있는 것:** 인터랙티브 실습 3종 · 확인 퀴즈 3문항 · 용어 툴팁 사전 · 지식 색인(온톨로지) · 서지 꾸러미(kg.json · JSON-LD · BibTeX · CSL-JSON 내려받기). (Colab 코드는 이 시리즈에서 준비 중입니다.)

### 언어 전환

- 최상단 메뉴의 🌐 선택 상자 또는 오른쪽 아래 🌐 배너에서 언어를 고릅니다. 고른 언어는 브라우저에 기억됩니다.
- 한국어 페이지에서는 브라우저 언어가 지원 언어면 자동 전환됩니다(번역판 주소로 들어오면 전환하지 않음). `?lang=xx`로도 열 수 있고, 없는 언어 파일은 자동으로 머뭅니다(HEAD 확인).

| 언어 | 1장 파일 | 첫 화면 |
|---|---|---|
| 한국어 | `01_inference_prerequisites.html` | `index.html` |
| English | `01_inference_prerequisites.en.html` | `index.en.html` |
| 中文 | `01_inference_prerequisites.zh.html` | `index.zh.html` |
| 日本語 | `01_inference_prerequisites.ja.html` | `index.ja.html` |
| Oʻzbekcha | `01_inference_prerequisites.uz.html` | `index.uz.html` |
| Русский | `01_inference_prerequisites.ru.html` | `index.ru.html` |
| Tiếng Việt | `01_inference_prerequisites.vi.html` | `index.vi.html` |

### 파일 구조

```
index.html / index.{en,zh,ja,uz,ru,vi}.html
01_inference_prerequisites.html / 01_inference_prerequisites.{en,zh,ja,uz,ru,vi}.html
og_01.png          공유 미리보기 이미지
README.md
```

### 데이터와 이미지

페이지 그림은 저자의 캐릭터 설정집(박사·조수·초파리 연구원·Money-Robo)을 16비트 픽셀아트로 생성하고 검수한 것입니다(글자·로고 없음). 시뮬레이션 수치는 교육용 모형이며 실제 요금·정책과 다를 수 있습니다.

### 용어 표기

「공유 추론」(토큰당 과금 서빙)과 「전용 배포」(GPU 시간 임대)는 시리즈 전체에서 고정해 씁니다. 「장부」는 비용 구조를 뜻하는 시리즈 고유 비유입니다.

### 라이선스

크리에이티브 커먼즈 저작자표시-비영리 4.0 국제 라이선스([CC BY-NC 4.0](https://creativecommons.org/licenses/by-nc/4.0/deed.ko)). 출처 표기 예: 「AI Lab Explainer — 추론 엔지니어링 시리즈」, 글 안상선.

---

<a id="en"></a>
## English

An interactive educational HTML series on balancing latency, throughput, and unit economics in LLM inference serving. Every page is a single self-contained HTML file (images, data, and scripts inlined as base64) — open it in a browser, no build step.

**Read online:** https://adminmrobo.github.io/&lt;repository&gt;/  ← insert your live URL after deploying

**Author:** Written by Ahn Sangsun (CEO, M-Robo Co., Ltd.)
**License:** CC BY-NC 4.0

**Languages:** [한국어](#ko) · [English](#en) · [中文](#zh) · [日本語](#ja) · [Oʻzbekcha](#uz) · [Русский](#ru) · [Tiếng Việt](#vi)

### Contents

| Part | File | Topic | Level |
|---|---|---|---|
| Home | `index.html` | Series intro · mission list · progress check | — |
| Textbook Ch.1 | `01_inference_prerequisites.html` | Shared API vs dedicated GPU break-even, domain fine-tuning and distillation, TTFT·TPS·P99 labs, and the showdown | ★★★☆☆ |

**Key numbers:** $780/month (dedicated 3B) vs $3,600 (frontier API) · break-even ≈ 12M tokens/day. Every number on the page is drawn by the same math as its slider/button lab (illustrative-mockup caveats in each footer).

**Inside each chapter:** 3 interactive labs · 3 check questions · term tooltip glossary · knowledge index (ontology) · bibliography bundle (kg.json · JSON-LD · BibTeX · CSL-JSON). (Colab notebooks are in preparation for this series.)

### Switching language

Pick a language from the 🌐 box in the top menu or the 🌐 banner at the bottom right; the choice is remembered. Korean pages auto-redirect when your browser language is supported (translation URLs never redirect). `?lang=xx` also works; missing files keep you where you are (HEAD check).

### Files

```
index.html / index.{en,zh,ja,uz,ru,vi}.html
01_inference_prerequisites.html / 01_inference_prerequisites.{en,zh,ja,uz,ru,vi}.html
og_01.png          share preview image
README.md
```

### Data & images

Artwork was generated as 16-bit pixel art from the author's character design sheet (the Doctor, the Assistant, the Fruit Fly Researcher, Money-Robo) and verified (no text, no logos). Simulation numbers are educational mock-ups and may differ from real pricing.

### License

Creative Commons Attribution-NonCommercial 4.0 International ([CC BY-NC 4.0](https://creativecommons.org/licenses/by-nc/4.0/deed.en)). Attribution example: "AI Lab Explainer — Inference Engineering series", by Ahn Sangsun.

---

<a id="zh"></a>
## 中文

关于 LLM 推理服务中延迟、吞吐量与单位经济学平衡的互动教学 HTML 系列。每页都是单个自包含 HTML 文件（图片、数据、脚本全部以 base64 内联），浏览器直接打开，无需构建。

**在线阅读：** https://adminmrobo.github.io/&lt;仓库&gt;/  ← 部署后请填入实际地址

**作者：** 作者 · Ahn Sangsun（M-Robo 株式会社代表）
**许可：** CC BY-NC 4.0

**语言：** [한국어](#ko) · [English](#en) · [中文](#zh) · [日本語](#ja) · [Oʻzbekcha](#uz) · [Русский](#ru) · [Tiếng Việt](#vi)

### 构成

| 部分 | 文件 | 内容 | 难度 |
|---|---|---|---|
| 首页 | `index.html` | 系列介绍 · 任务列表 · 进度打卡 | — |
| 教科书第1章 | `01_inference_prerequisites.html` | 共享 API vs 专用 GPU 盈亏平衡、领域微调与蒸馏、TTFT·TPS·P99 实验与终极对决 | ★★★☆☆ |

**关键数字：** 每月 $780（专用 3B） vs $3,600（前沿 API） · 盈亏平衡约 1,200万 token/日。页面所有数字都与滑块/按钮实验使用相同计算（说明性示意部分的限制见页脚）。

**每章包含：** 3 个互动实验 · 3 道确认测验 · 术语提示词典 · 知识索引（本体） · 文献知识包（kg.json · JSON-LD · BibTeX · CSL-JSON）。（本系列的 Colab 代码正在准备中。）

### 切换语言

在顶部菜单的 🌐 选择框或右下角 🌐 横幅中选择语言，选择会被记住。韩语页在浏览器语言受支持时自动跳转（翻译页地址不跳转）。也支持 `?lang=xx`；缺失的文件会留在原页（HEAD 检查）。

### 文件结构

```
index.html / index.{en,zh,ja,uz,ru,vi}.html
01_inference_prerequisites.html / 01_inference_prerequisites.{en,zh,ja,uz,ru,vi}.html
og_01.png          分享预览图
README.md
```

### 数据与图片

页面插图由作者的角色设定集生成 16 位像素画并经检收（无文字、无标识）。模拟数值为教学示意，可能与真实价格不同。

### 许可

知识共享 署名-非商业性使用 4.0 国际许可协议（[CC BY-NC 4.0](https://creativecommons.org/licenses/by-nc/4.0/deed.zh-hans)）。引用示例：「AI Lab Explainer — 推理工程系列」，Ahn Sangsun。

---

<a id="ja"></a>
## 日本語

LLM推論サービングのレイテンシ・スループット・単位経済学のバランスを扱うインタラクティブ教育HTMLシリーズ。各ページは図・データ・スクリプトをbase64で1ファイルに収めた自己完結HTMLで、ビルドなしでブラウザから直接開けます。

**オンラインで読む：** https://adminmrobo.github.io/&lt;リポジトリ&gt;/  ← 公開後に実際のURLを入れてください

**著者：** 文・アン・サンソン（株式会社M-Robo代表）
**ライセンス：** CC BY-NC 4.0

**言語：** [한국어](#ko) · [English](#en) · [中文](#zh) · [日本語](#ja) · [Oʻzbekcha](#uz) · [Русский](#ru) · [Tiếng Việt](#vi)

### 構成

| 回 | ファイル | 内容 | 難易度 |
|---|---|---|---|
| トップ | `index.html` | シリーズ紹介 · ミッション一覧 · 進度チェック | — |
| 教科書第1章 | `01_inference_prerequisites.html` | 共有API vs 専用GPUの損益分岐、ドメイン・ファインチューニングと蒸留、TTFT・TPS・P99の実習と決着戦 | ★★★☆☆ |

**主要な数字：** 月$780（専用3B） vs $3,600（フロンティアAPI） · 損益分岐 約1,200万トークン/日。ページ内の数字はすべてスライダー/ボタンの実習と同じ計算で描かれます（説明用の模型である点は各フッターを参照）。

**各回に入っているもの：** インタラクティブ実習3種 · 確認クイズ3問 · 用語ツールチップ辞書 · 知識インデックス（オントロジー） · 文献パッケージ（kg.json · JSON-LD · BibTeX · CSL-JSON）。（このシリーズのColabコードは準備中です。）

### 言語の切り替え

上部メニューの🌐セレクトか右下の🌐バナーで言語を選ぶと、選択は記憶されます。韓国語ページではブラウザ言語が対応言語なら自動切换します（翻訳版アドレスでは切り替えません）。`?lang=xx` も可能。存在しない言語ファイルはその場に留まります（HEAD確認）。

### ファイル構成

```
index.html / index.{en,zh,ja,uz,ru,vi}.html
01_inference_prerequisites.html / 01_inference_prerequisites.{en,zh,ja,uz,ru,vi}.html
og_01.png          共有プレビュー画像
README.md
```

### データと画像

頁の図は、著者のキャラクター設定集（博士・助手・ショウジョウバエ研究員・Money-Robo）を16ビット・ピクセルアートとして生成し検収したものです（文字・ロゴなし）。シミュレーション数値は教育用モデルで、実際の料金とは異なる場合があります。

### ライセンス

クリエイティブ・コモンズ 表示-非営利 4.0 国際（[CC BY-NC 4.0](https://creativecommons.org/licenses/by-nc/4.0/deed.ja)）。出典例：「AI Lab Explainer — 推論エンジニアリングシリーズ」、文・アン・サンソン。

---

<a id="uz"></a>
## Oʻzbekcha

LLM inferensiya servisning kechikish, oʻtkazish va birlik iqtisodi muvozanati haqidagi interaktiv taʼlim HTML seriyasi. Har bir sahifa — rasmlari, maʼlumotlari va skriptlari base64 bilan bitta faylga sigʻdirilgan mustaqil HTML; brauzerda qurilmasiz ochiladi.

**Onlayn oʻqish:** https://adminmrobo.github.io/&lt;repositoriy&gt;/  ← joylashtirgach, haqiqiy manzilni qoʻying

**Muallif:** Muallif · Ahn Sangsun (M-Robo kompaniyasi rahbari)
**Litsenziya:** CC BY-NC 4.0

**Tillar:** [한국어](#ko) · [English](#en) · [中文](#zh) · [日本語](#ja) · [Oʻzbekcha](#uz) · [Русский](#ru) · [Tiếng Việt](#vi)

### Tuzilish

| Qism | Fayl | Mavzu | Daraja |
|---|---|---|---|
| Bosh sahifa | `index.html` | Seriya tanishtirish · topshiriqlar · jarayon | — |
| Darslik 1-bob | `01_inference_prerequisites.html` | Umumiy API vs maxsus GPU muvozanati, doman fine-tuning va distillatsiya, TTFT·TPS·P99 amaliyoti va yakuniy jang | ★★★☆☆ |

**Asosiy raqamlar:** oyiga $780 (maxsus 3B) vs $3,600 (frontera API) · muvozanat ≈ 12 mln token/kun. Sahifadagi barcha raqamlar slider/tugma amaliyoti bilan bir xil hisobda chiziladi (tushuntirish uchun maket chegaralari footerda).

**Har bir bobga kirgan narsalar:** 3 ta interaktiv amaliyot · 3 ta nazorat savoli · atama maslahatlari lugʻati · bilish indeksi (ontologiya) · bibliografiya toʻplami (kg.json · JSON-LD · BibTeX · CSL-JSON). (Bu seriya uchun Colab kodlari tayyorlanmoqda.)

### Tilni almashtirish

Yuqori menyudagi 🌐 tanlov yoki oʻng pastdagi 🌐 banner orqali tilni tanlang; tanlov eslab qolinadi. Koreys sahifalarida brauzer tili qoʻllanadigan til boʻlsa avtomatik oʻtadi (tarjima manzillarida oʻtmaydi). `?lang=xx` ham ishlaydi; fayl topilmasa oʻsha sahifada qoladi (HEAD tekshiruvi).

### Fayllar

```
index.html / index.{en,zh,ja,uz,ru,vi}.html
01_inference_prerequisites.html / 01_inference_prerequisites.{en,zh,ja,uz,ru,vi}.html
og_01.png          ulashish oldindan koʻrinish rasmi
README.md
```

### Maʼlumot va rasmlar

Sahifa rasmlari muallifning qahramonlar toʻplami (Doktor, Yordamchi, Drozofila tadqiqotchisi, Money-Robo) asosida 16-bit piksel-art qilib yaratilgan va tekshirilgan (yozuv va logotipsiz). Simulyatsiya raqamlari taʼlimiy model boʻlib, real narxlardan farq qilishi mumkin.

### Litsenziya

Creative Commons Attribution-NonCommercial 4.0 International ([CC BY-NC 4.0](https://creativecommons.org/licenses/by-nc/4.0/deed.en)). Manba koʻrinishi: "AI Lab Explainer — Inferensiya muhandisligi seriyasi", Ahn Sangsun.

---

<a id="ru"></a>
## Русский

Интерактивная образовательная HTML-серия о балансе задержки, пропускной способности и юнит-экономики в LLM-сервинге. Каждая страница — один самодостаточный HTML-файл (картинки, данные и скрипты встроены в base64), открывается в браузере без сборки.

**Читать онлайн:** https://adminmrobo.github.io/&lt;репозиторий&gt;/  ← после публикации подставьте реальный адрес

**Автор:** Автор · Ан Сансон (генеральный директор M-Robo Co., Ltd.)
**Лицензия:** CC BY-NC 4.0

**Языки:** [한국어](#ko) · [English](#en) · [中文](#zh) · [日本語](#ja) · [Oʻzbekcha](#uz) · [Русский](#ru) · [Tiếng Việt](#vi)

### Состав

| Часть | Файл | Тема | Уровень |
|---|---|---|---|
| Титульная | `index.html` | О серии · список миссий · отметки прогресса | — |
| Глава 1 учебника | `01_inference_prerequisites.html` | Точка безубыточности общего API и выделенного GPU, дообучение и дистилляция на домене, практика TTFT·TPS·P99 и финальная дуэль | ★★★☆☆ |

**Ключевые числа:** $780 в месяц (выделенная 3B) против $3,600 (фронтир-API) · безубыток ≈ 12 млн токенов/день. Все числа на странице рисуются теми же расчётами, что и в практикумах с ползунками и кнопками (об ограничениях иллюстративных макетов — в подвале каждой страницы).

**Внутри каждой главы:** 3 интерактивных практикума · 3 проверочных вопроса · глоссарий с подсказками · индекс знаний (онтология) · библиографический пакет (kg.json · JSON-LD · BibTeX · CSL-JSON). (Colab-код для этой серии готовится.)

### Переключение языка

Выберите язык в 🌐-селекторе верхнего меню или в 🌐-баннере справа внизу; выбор запоминается. Корейские страницы автоматически переключаются, если язык браузера поддерживается (адреса переводных страниц не переключаются). Работает и `?lang=xx`; при отсутствии файла вы остаётесь на месте (HEAD-проверка).

### Файлы

```
index.html / index.{en,zh,ja,uz,ru,vi}.html
01_inference_prerequisites.html / 01_inference_prerequisites.{en,zh,ja,uz,ru,vi}.html
og_01.png          картинка для превью при репосте
README.md
```

### Данные и изображения

Рисунки созданы как 16-битный пиксель-арт по листу персонажей автора (Доктор, Ассистент, Исследователь-дрозофила, Money-Robo) и проверены (без текста и логотипов). Числа симуляций — учебные макеты и могут отличаться от реальных цен.

### Лицензия

Creative Commons «Атрибуция — Некоммерческое использование» 4.0 Международная ([CC BY-NC 4.0](https://creativecommons.org/licenses/by-nc/4.0/deed.ru)). Пример указания источника: «AI Lab Explainer — серия "Инженерия инференса"», Ан Сансон.

---

<a id="vi"></a>
## Tiếng Việt

Chuỗi HTML giáo dục tương tác về cân bằng độ trễ, thông lượng và kinh tế học đơn vị trong phục vụ suy luận LLM. Mỗi trang là một tệp HTML tự chứa duy nhất (hình, dữ liệu, kịch bản nhúng base64) — mở bằng trình duyệt, không cần build.

**Đọc trực tuyến:** https://adminmrobo.github.io/&lt;kho&gt;/  ← sau khi triển khai, hãy điền địa chỉ thật

**Tác giả:** Tác giả · Ahn Sangsun (Giám đốc điều hành, M-Robo Co., Ltd.)
**Giấy phép:** CC BY-NC 4.0

**Ngôn ngữ:** [한국어](#ko) · [English](#en) · [中文](#zh) · [日本語](#ja) · [Oʻzbekcha](#uz) · [Русский](#ru) · [Tiếng Việt](#vi)

### Cấu trúc

| Phần | Tệp | Nội dung | Độ khó |
|---|---|---|---|
| Trang đầu | `index.html` | Giới thiệu chuỗi · danh sách nhiệm vụ · đánh dấu tiến độ | — |
| Giáo trình Chương 1 | `01_inference_prerequisites.html` | Điểm hòa vốn API dùng chung vs GPU riêng, tinh chỉnh và chưng cất chuyên ngành, thực hành TTFT·TPS·P99 và trận đấu cuối | ★★★☆☆ |

**Số liệu then chốt:** $780/tháng (3B riêng) vs $3,600 (API tiên phong) · hòa vốn ≈ 12 triệu token/ngày. Mọi số liệu trên trang đều vẽ bằng cùng phép tính với phòng thực hành thanh trượt/nút (giới hạn mô hình minh họa xem chân trang).

**Bên trong mỗi chương:** 3 phòng thực hành tương tác · 3 câu hỏi kiểm tra · bảng chú giải thuật ngữ · chỉ mục tri thức (bản thể) · gói thư mục (kg.json · JSON-LD · BibTeX · CSL-JSON). (Mã Colab của chuỗi này đang chuẩn bị.)

### Đổi ngôn ngữ

Chọn ngôn ngữ ở hộp 🌐 trên menu đầu trang hoặc banner 🌐 dưới góc phải; lựa chọn được ghi nhớ. Trang tiếng Hàn tự chuyển khi ngôn ngữ trình duyệt được hỗ trợ (địa chỉ bản dịch không tự chuyển). `?lang=xx` cũng dùng được; tệp thiếu sẽ giữ bạn ở trang hiện tại (kiểm tra HEAD).

### Tệp

```
index.html / index.{en,zh,ja,uz,ru,vi}.html
01_inference_prerequisites.html / 01_inference_prerequisites.{en,zh,ja,uz,ru,vi}.html
og_01.png          ảnh xem trước khi chia sẻ
README.md
```

### Dữ liệu và hình ảnh

Hình trong trang là pixel-art 16-bit dựng từ bộ cài đặt nhân vật của tác giả (Tiến sĩ, Trợ lý, Nhà nghiên cứu Ruồi giấm, Money-Robo) và đã được nghiệm thu (không chữ, không logo). Số liệu mô phỏng là mô hình giáo dục, có thể khác giá thực tế.

### Giấy phép

Giấy phép Creative Commons Ghi công – Phi thương mại 4.0 Quốc tế ([CC BY-NC 4.0](https://creativecommons.org/licenses/by-nc/4.0/deed.vi)). Ví dụ ghi nguồn: «AI Lab Explainer — chuỗi Kỹ thuật suy luận», Ahn Sangsun.
