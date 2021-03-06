---
# try also 'default' to start simple
theme: unicorn
# random image from a curated Unsplash collection by Anthony
# like them? see https://unsplash.com/collections/94734566/slidev
background: https://source.unsplash.com/collection/94734566/1920x1080
# apply any windi css classes to the current slide
class: 'text-center'
# https://sli.dev/custom/highlighters.html
highlighter: shiki
# show line numbers in code blocks
lineNumbers: false
# some information about the slides, markdown enabled
info: |
  ## Slidev Starter Template
  Presentation slides for developers.

  Learn more at [Sli.dev](https://sli.dev)
# persist drawings in exports and build
drawings:
  persist: false
handle: 'tult'
website: 'https://rikkeisoft.com'
layout: 'intro'
introImage: '/avatar.jpeg'
---

# Website optimization

How to improve the performance of a website

<img src="/avatar.jpeg" class="absolute top-20 left-20 rounded-full w-80 h-80 object-cover p-2 bg-gradient-to-r from-fuchsia-700 to-purple-800 dark:from-white dark:to-purple-50">


---
layout: table-contents
gradientColors:
  - '#8EC5FC'
  - '#E0C3FC'
handle: tult
website: https://rikkeisoft.com
---

<style>
  figure img.rounded-full {
    @apply w-10 h-10
  }
</style>

# Table of contents

1. Why speed matters? 
2. What factors affect website load time?
3. Core web vitals?

<!--
You can have `style` tag in markdown to override the style for the current page.
Learn more: https://sli.dev/guide/syntax#embedded-styles
-->

<style>
h1 {
  background-color: #2B90B6;
  background-image: linear-gradient(45deg, #4EC5D4 10%, #146b8c 20%);
  background-size: 100%;
  -webkit-background-clip: text;
  -moz-background-clip: text;
  -webkit-text-fill-color: transparent;
  -moz-text-fill-color: transparent;
}
</style>


---
layout: new-section
handle: 'tult'
website: 'https://rikkeisoft.com'
sectionImage: '/section-illustration.svg'
---

# Why speed matters? 
Website load time affects the number of visitors.

---
layout: cover
handle: tult
website: https://rikkeisoft.com
---

# Why speed matters?

<div v-click>
  <cil-hand-point-right class="text-green-600" />
  The longer a webpage takes to load, the more it bounce rate will skyrocket 
  <mdi-rocket-launch class="text-red-600" /><br>
</div>
<div v-click>
  <cil-hand-point-right class="text-green-600" />
  The high bounce rate tells search engines that this page is useless, so its ranking will slip
  <lucide-trending-down class="text-red-600" />
</div>
<div v-click>
  <br>
  <div class="flex flex-row relative">
    <img class="w-3/5 object-contain" src="/did-you-know.webp" />
    <img class="absolute -right-36 -bottom-32 w-3/5 object-contain" src="/bounce-rate-statistics.webp" />
  </div>
</div>

<!--
Bounce rate l?? t??? l??? visitors ch??? xem 1 page duy nh???t c???a website sau ???? r???i ??i ngay
-->

---
layour: cover
handle: 'tult'
website: 'https://rikkeisoft.com'
--- 

# What factor affect website load time?

<div v-click="1">
  <ul>
    <li>User's internet connection</li>
    <li>Web server and user's computer</li>
    <li>The size of the resources that needed <fluent-target-arrow-24-regular class="text-red-600" v-click="2" /></li>
  </ul>
</div>

---
layout: new-section
handle: 'tult'
website: 'https://rikkeisoft.com'
sectionImage: '/section-illustration.svg'
---

# Core web vitals

The metrics to evaluate the user's experiences 

---
layout: cover
handle: tult
website: https://rikkeisoft.com
---


# Core web vitals 

<div>
  <img src="/core-web-vitals.png" />
</div>

<!-- Core web vitals l?? c??c metrics s??? d???ng ????? ????nh gi?? 3 kh??a c???nh khi load m???t website ???? l?? ....
T????ng ???ng v???i m???i kh??a c???nh l?? m???t metrics ????? ????nh gi?? chungs ???? l??  -->


---
layout: cover
handle: 'tult'
website: 'https://rikkeisoft.com'
---

# Cumulative Layout Shift (CLS)

CLS is the metrics to evaluate how much the page's content jumps around.

<div v-click class="flex flex-row justity-center">
  <video controls width="400" class="self-center">
      <source src="/CLS.webm"
              type="video/webm">
  </video>
</div>

<!-- for a better web app performance, a minimal CLS score is the best  -->

---
layout: cover
handle: 'tult'
website: 'https://rikkeisoft.com'
---

# What causes poor CLS ? 

<div class="relative">
  <img v-click-hide src="/poor-CLS.png" />
  <div v-after class="flex flex-row absolute top-1/2 left-1/4">
    <h1 class="ml-1">How to improve CLS ?</h1>
    <noto-thinking-face class="text-3xl mb-4 ml-2" />
  </div>
</div>

<!-- 
FOUT: flash of unstyled text 
FOIT: flash of invisible text
-->

---
layout: cover
handle: 'tult'
website: 'https://rikkeisoft.com'
---


# Tip #1
##  Always include width and height size attributes on images and video elements.

---
layout: cover
handle: 'tult'
website: 'https://rikkeisoft.com'
---

<div class="relative">
  <!-- <video controls="controls" width="400" height="auto" name="Demo cls">
    <source src="/public/demo-cls.mov">
  </video> -->
  <img src="/demo-cls.gif" width="400" height="auto" />
  <img src="/CLS-score.png" alt="cls score" class="absolute right-0 w-1/2 h-auto bottom-22">
</div>

---
layout: cover
handle: 'tult'
website: 'https://rikkeisoft.com'
---

```html
<!-- old best practice -->
<img src="avatar.png" width="640" height="360" alt="avatar">

<!-- response -->
<img src="avatar.png" alt="avatar">

<style>
  img {
    width: 100%;
    height: aut;
  }
</style>
```

<!-- 
Tr?????c ????y ng?????i ta d??ng width / height property ????? set thu???c t??nh ????? d??i v?? ????? r???ng cho ???nh -> browser c?? th??? preserve space cho ???nh tr?????c c??? khi ch??ng ??c t???i xong 
-->

---
layout: cover
handle: 'tult'
website: 'https://rikkeisoft.com'
---

<div class="relative">
  <!-- <video controls="controls" width="400" height="auto" name="Demo cls">
    <source src="/public/Demo-cls-after.mov">
  </video> -->
  <img src="/demo-cls-after.gif" width="400" height="auto" />
  <img src="/CLS-score-after.png" alt="cls score" class="absolute right-0 w-1/2 h-auto bottom-22">
</div>

<!-- - L??m th??? n??o ????? bi???t ??c element n??o khi???n ??i???m CLS b??? t??ng l??n ?  -->

---
layout: cover
handle: 'tult'
website: 'https://rikkeisoft.com'
---

# Find large layout shift elements

<img src="/find-cls-elements.png" alt="find-cls-element" width="480" height="auto">

---
layout: cover
handle: 'tult'
website: 'https://rikkeisoft.com'
---

# Approach to image loading

<ic-sharp-report-problem class="text-red-600" /> <span class="text-red-600 font-bold">Problem:</span> <span>Creating empty space in the site and users don't know what things will come out from there</span> <fxemoji-ghost class="text-xl" />

<div v-click>
<el-idea-alt class="text-green-600" /> <span class="text-green-600 font-bold">Solution:</span>
<iframe class="mt-2" width="560" height="315" src="https://www.youtube.com/embed/CPmNHj9a0JI" title="YouTube video player" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture" allowfullscreen></iframe>
</div>

<!--
Th???c hi???n lazy loading cho image. ?? t?????ng chung l?? s??? s??? d???ng 1 container bao l???y image. 
Trong th???i gian image ???????c load ho???c ??? ngo??i viewport -> s??? hi???n th??? n???i dung c???a container (background image, low quality image, ...)
- Layzy loading c?? th??? ???????c implement b???ng r???t nhi???u c??ch.
-->

---
layout: cover
handle: 'tult'
website: 'https://rikkeisoft.com'
---


# Tip #2 
## Reserve enough space for dynamic content like ads or promos.

---
layout: cover
handle: 'tult'
website: 'https://rikkeisoft.com'
---


# Tip #3
## Avoid inserting new content above existing content.

---
layout: cover
handle: tult
website: https://rikkeisoft.com
---

<div class="w-full items-center flex flex-col">
  <h1>Discussion time!!!</h1>
  <div class="text-3xl">
    <ph-smiley-bold class="text-green-400" /><ph-smiley-bold class="text-yellow-400" /><ph-smiley-bold class="text-red-400" />
  </div>
</div>

---
layout: cover
handle: 'tult'
website: 'https://rikkeisoft.com'
---

# Largest Contentful Paint (LCP)

LCP is the time when the largent content on the page is rendered.
<div class="w-full flex justify-center mt-4">
  <img src="/LCP.png" class="w-1/2 h-auto" />
</div>

---
layout: cover
handle: 'tult'
website: 'https://rikkeisoft.com'
---


<div>
  <img src="/poor_LCP.png" />
  <arrow v-click="1" x1="300" y1="500" x2="380" y2="420" color="red" width="3" arrowSize="1"  />
</div>


---
layout: new-section
handle: 'tult'
website: 'https://rikkeisoft.com'
sectionImage: '/section-illustration.svg'
---

# How the browser render a webpage

Deep dive into the rendering process and figure out where can be optimized.

---
layout: cover
handle: 'tult'
website: 'https://rikkeisoft.com'
---

# DOM

<div class="flex flex-row">
  <div class="w-2/3">
  <ul>
    <li>DOM stands for document object model.</li>
    <li>When browser encounters a HTML element, it creates a JavaScript object called a node.</li>
    <li>After create a node, the browser has to create a <span class="font-bold">tree-like structure</span> of created nodes.</li>
  </ul>
  </div>
  <div class="w-1/3 pl-4">
    <img class="object-contain" src="/DOM.png">
  </div>
</div>

---
layout: cover
andle: 'tult'
website: 'https://rikkeisoft.com'
---

# CSSOM

<div class="flex flex-row">
  <div class="w-2/3">
  <ul>
    <li>CSSOM stands for CSS object model.</li>
    <li>After the browser has done constructing the DOM, it'll read CSS from all the sources (external, embedded, inline, user-agent, etc.) to construct CSSOM.</li>
    <li>Each node in CSSOM tree contains the style information that will be applied to DOM elements that it target.</li>
  </ul>
  </div>
  <div class="w-1/3 pl-4">
    <img class="object-contain" src="/CSSOM.png">
  </div>
</div>


---
layout: cover
handle: 'tult'
website: 'https://rikkeisoft.com'
---

# Render tree

- This is **tree-like structure** constructed by combining DOM and CSSOM trees together. 
- The browser calculate the layout for each **visible elements** and paint them on the screen.

<div class="w-full flex justify-center mt-8">
  <img src="/render-tree.png" class="object-contain">
</div>

---
layout: cover
handle: 'tult'
website: 'https://rikkeisoft.com'
---

# Parsing

- **Parsing** is the process of reading HTML and constructing the DOM tree from it.
- The browser starts the parsing process as soon as it recevices few bytes of HTML document.
- Because of that, the browser can build the DOM tree **incrementally**.

<div class="w-full flex justify-center">
  <img class="object-contain" src="/Parsing.png">
</div>
<p class="text-center text-xs">Parse raw HTML codes into a DOM tree</p>

<!-- 
- Qu?? tr??nh parsing v?? x??y d???ng DOM tree g???i l?? DOM parsing 
- Ch????ng tr??nh th???c hi???n qu?? tr??nh tr??n g???i l?? DOM parser
- Ch???y demo trang web ??? ?????a ch??? /html/incremental.html ch???ng minh incremental. B???t throttling ????? gi???m t???c ????? m???ng
1. Ch?? ?? thanh cu???n c??ng ng??ng c??ng ng???n
2. T??ch ch???n capture screenshoots trong dev tools -> screenshoot ??? sau c?? nhi???u n???i dung h??n screenshoot ??? tr?????c
 -->

---
layout: cover
handle: 'tult'
website: 'https://rikkeisoft.com'
---

# External resources & parser-blocking script


- Whenever the browser encounters a external resouces, it'll start download that file <br> in background **except** for script files. Hence script files are called **parser-blocking**.
- DOM parsing is executed on the main thread and will not progress if that thread is busy.

<br>

<div class="flex flex-column justify-between items-center">
  <div>
    <cil-hand-point-right class="text-green-400" /> A script (JavaScript)
  </div>
  <div class="leading-10">
  <div v-click="1">
    <arrow x1="220" y1="290" x2="400" y2="260" color="#564" width="3" arrowSize="1"  />
    <p>Embedded scripts <ic-baseline-arrow-forward /> Executing the embedded codes on the main thread.</p>
  </div>
  <div v-click="2">
    <arrow x1="220" y1="300" x2="400" y2="310" color="#564" width="3" arrowSize="1"  />
    <p>External script file <ic-baseline-arrow-forward /> Halt the execution of the main thread <br> until that file is downloaded and executed</p>
  </div>
  </div>
</div>

<div v-click="3">
  <ic-baseline-question-mark class="text-red-400 text-2xl mt-8" /> Halting the DOM parsing while the script file is being downloaded is unnecessary (in most cases). What is the solution ?
</div>

<!-- 
- T???i sao ph???i halt the main thread cho ?????n khi file script ???????c download v?? th???c thi xong ? 
- V?? Browser cung c???p DOM API cho JavaScript runtime (React ho???t ?????ng b???ng c??ch n??y) -> n???u DOM parsing v?? script ???????c th???c thi ?????ng th???i 
th?? s??? c?? th??? g??y ra t??nh tr???ng race conditions 
-->

---
layout: cover
handle: tult
website: https://rikkeisoft.com
---

# Async & defer attributes

- HTML5 provides us `async` and `defer` attribute for `script` tag.
- With `async`, the parsing process won't be blocked while the file is being downloaded. And will be block right after the script file is ready to be executed.
- With `defer`, the script doesn't execute even when the file is fully downloaded. All `defer` scripts are executed once the DOM is fully constructed.

<!--
Ch???y demo cho blocking script ??? ?????a ch??? http://localhost:8088/html/parser-blocking.html
- L??u ??: throttling network 
- Ph???i demo ???????c c??ch ho???t ?????ng c???a async/await 
B?????c 1: Ch???y v???i script ?????u ti??n ko ?????t async/await -> render ??c 30 th??? th?? b??? block. Khi n??o console.log in ra "Hello world" th?? th???y b???t ?????u in ti???p 
B?????c 2: ?????t async v???i script ?????u ti??n -> Th???y browser in ???????c nhi???u h??n 30 th??? nh??ng script v???n ch??a th???y in "Hello world" -> ko b??? block
B?????c 3: Th???y script 2 in "Xin chao!!!" khi m?? c??i spiner tr??n tab c???a tr??nh duy???t ng???ng quay -> render xong h???t r???i m???i ch???y script 

- Demo test ??i???m lighthouse ????? th???y ???????c s??? kh??c bi???t c???a async v?? defer
-->

---
layout: cover
handle: tult
website: https://rikkeisoft.com
---

# Render-Blocking CSS

- Render tree is getting built incrementally as the DOM tree is getting constructed.
- The browser constructs the CSSOM tree from the stylesheet content
- The CSSOM tree construction is **not incremental**

<!--
- Khi browser g???p th??? style, browser s??? parser to??n b??? CSS v?? update CSSOM tree. Sau ???? n?? ti???p t???c qu?? tr??nh DOM parsing. T????ng t??? cho inline style
  
- ?????i v???i external stylesheet files. Kh??ng nh?? HTML file, n?? ph???i ?????i cho to??n b??? file stylesheet ???????c t???i v??? r???i m???i th???c hi???n parsing.(g)

- Khi to??n b??? CSS rules ??c process v?? CSSOM tree ???????c update th?? render tree ms ??c update v?? render giao di???n ra m??n h??nh. Trong th???i gian ???? th?? render tree b??? halt.

- Demo ??? trang http://localhost:8088/html/render-blocking.html
-->

---
layout: cover
handle: tult
website: https://rikkeisoft.com
---

# Script-Blocking CSS

<uiw-question-circle class="text-red-500 mt-8" /> Scenario where the browser start downloading the stylesheet file, then it encounter an external script file and start downloading it. 
The script file is downloaded before the stylesheet file ? In this case, should the browser start executing the script?

<div v-click class="mt-12">
  <ic-baseline-anchor class="text-green-600" /> In conclusion, the browser may fully downloaded the script but will not execute it unless all the stylesheets before it are parsed. Those stylesheets are called script-blocking.
</div>

<!--
- L?? do l?? v?? n???u script ??c t???i xong v?? th???c hi???n lu??n. N???u script access v??o thu???c t??nh CSS c???a 1 DOM node. Sau ???? stylesheet file ??c t???i xong v?? update l???i thu???c t??nh ???? th?? gi?? tr??? l???y ???????c tr?????c ???? s??? b??? sai. 
- Demo ??? trang http://localhost:8088/html/script-blocking.html

1. Nh??n v??o tab network, ph???n waterfall -> script file ???? t???i xong t??? tr?????c file stylesheet nh??ng ko th???y in ra "Hello world" 
2. Ph???i ?????n khi m??u ch??? ??c ?????i th?? m???i th???y in ra "Hello world"
-->

---
layout: cover
handle: tult
website: https://rikkeisoft.com
---

# General rules

1. Injecting stylesheet or required script files in the `<head>` tag of the HTML document. 
2. Use `rel="preload"` to instruct the browser to download key resources as soon as possible.
3. The best place to inject script files is the end of `<body>` tag.

<!--
- V?? HTML file ???????c parse l???n l?????t v?? vi???c download script file ko block DOM construction. N??n c??ng t???i s???m c??c file stylesheet th?? giao ??i???n ???????c render c??ng s???m
-->


---
layout: cover
handle: tult
website: https://rikkeisoft.com
---

<div class="w-full items-center flex flex-col">
  <h1>Discussion time!!!</h1>
  <div class="text-3xl">
    <ph-smiley-bold class="text-green-400" /><ph-smiley-bold class="text-yellow-400" /><ph-smiley-bold class="text-red-400" />
  </div>
</div>


---
layout: cover
handle: tult
website: https://rikkeisoft.com
---

# First Input Delay (FID)


<h3 v-click class="text-center mt-12 text-7xl">See ya next time <icon-park-outline-bye class="text-green-500 text-3xl" /></h3>
