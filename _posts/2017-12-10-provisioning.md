---
layout: post
title: 프로비저닝(Provisioning)이란
---

프로비저닝(Provisioning)이란
===================

이 포스트에서는 **프로비저닝<Provisioning>** 이 어떠한 개념인지 파악하고 근래 엔지니어들이 사용하고 있는 **프로비저닝<Provisioning>** 의 기술엔 어떤 것들이 있는지 몇 가지 정도만 파악해 본다.

----------

1. 옆팀 대리가 프로비저닝이란 말을 계속 쓰는데 그게 뭘까?
-------------------------------
> **사전적 의미**
> - 뜻 : 준비, 설비
> - 어구 : make provision : 준비하다.

프로비전(:Provision)의 사전적 의미부터 알아보자. 일단 프로비전! 영어로는 Provision이라고 표기한다.
구글 번역기도 좋지만 일단 내가 다니는 회사의 번역기로 변역해보자.(읭?)
아래의 URL에 가서 Provision을 찾아보면 다음과 같이 나온다.
> **카카오 어학 사전 URL : **http://alldic.daum.net/search.do?q=provision



2. 그럼 IT 엔지니어 혹은 종사자가 쓰는 프로비저닝의 뜻은?
-------------
#### **내 너에게 프로비저닝(Provisioning)을 알려주마!!**
IT에서 업무 혹은 서비스에 사용될 인프라(infra : 서버, DB 등 혹은 그 외에 많은 물리적 시스템) 리소스(자원)을 비즈니스의 요구사항에 맞추어 사용할 수 있도록 어떠한 행위를 취하는 것(결국 어떠한 행동)을 말한다.

관련하여 몇 가지 종류가 있다.

**서버자원 프로비저닝 (Server Resource Provisioning)**
우리가 흔히 서버라고 부르는 것들의 CPU, 메모리, Disk 등의 Resource를 적지적소에 배치하여 운영할 수 있도록 준비하는 일련의 행위 ( = provisioning)

** OS 프로비저닝 (OperatingSystem Provisioning)**
운영체제(OS)를 서버에 설치 및 설정하며 나아가 서비스를 위한 OS가 구동되는 것을 준비하는 일련의 행위 ( = provisioning )

**소프트웨어 프로비저닝 (Software Provisioning)**
소프트웨어를 서버에 설치 및 설정을 진행하여 필요한 부분에 대한 세팅하여 해당 소프트웨어를 실행할 수 있게 준비하는 일련의 행위 ( = provisioning)

**스토리지 프로비저닝 (Storage Provisioning)**
IT인프라에서 가장 근간이 되는 스토리지의 효율을 높일 수 있도록 준비하는 일련의 행위 ( = provisioning)

**계정 프로비저닝 (Account Provisioning)**
회사의 구성원이 조직에 배치 되거나 직무가 변경되어 HR담당자와 IT관리자는 e메일, 전사 ERP등과 같이 조직원에게 필요한 어플리케이션 혹은 그에 준하는 시스템에 필요한 계정을 생성하거나 권한 설정을 진행하는데 이러한 행위를 쉽게 할 수 있도록 준비하는 일련의 행위 ( = provisioning )

위와 같이 프로비저닝(일련의 준비 행위)를 작업자 (기획자가 될수도 있고 개발자가 될수도 있고 SE가 될 수도 있다.) 가 수동으로 진행하면 **수동 프로비저닝** 어떠한 자동화 툴을 이용하여 진행하면 **자동 프로비저닝** 이라고 한다.

잘 생각해보면 수동 프로비저닝보다 자동 프로비저닝이 훨씬 좋다는 것을 굳이 설명하지 않아도 알 수 있을거라 생각한다.
그 이유는? 아무리 클라우드(Cloud)가 대세가 되고 편한 환경이 도래해도 결국 대규모 (소규모라도 해당된다)의 시스템을 유지/보수 하려면 시간이 많이 들기 때문에 당연히 **자동 프로비저닝**이 더 편하고 훨씬 작업자의 정신 건강에 이롭다.

요즘 대두되고 있는 가상화 시스템, 클라우드 컴퓨팅 환경에서는 IT 인프라 Resource를 할당, 배치, 배포등과 같은 일련의 작업이 필요한 경우가 많은데 위에서 언급했듯이 **프로비저닝(Provisioning), 특히 자동 프로비저닝**을 활용하면 손 쉽게 구성을 할 수 있다.

#### <i class="icon-pencil"></i> **주인장의 한줄 의견**
> **한줄 의견 : **말이 되게 어려운데.. 그냥 어떠한 업무든 그 업무를 하기 위해 환경을 구성하는 IT업계의 단어... 



Generate basic ansible script file <기본 파일 생성>
-------------------
#### **기본 파일 생성**
하단의 기본 파일은 Ansible(앤서블) 프로젝트를 구성하고 있는 필수적이며 가장 기본적인 파일들이다.
**필히 생성**해 주어야 하며 해당 필수 파일들을 얼마나 잘 구성하느냐에 따라 규모 큰 Ansible 프로젝트 일수록관리하기 쉬워진다는 걸 숙지해야 한다.

#### <i class="icon-file"></i> 생성할 파일 목록 (Table of files to generate)
디렉터리 경로(path)       | 파일명(with extension : 확장자)
-------- | ---
/inventories/hadoop_develop/| hots
/inventories/haddop_production/| hosts
Pipe     | $1

> - Full access to **Google Drive** or **Dropbox** is required to be able to import any document in StackEdit. Permission restrictions can be configured in the settings.
> - Imported documents are downloaded in your browser and are not transmitted to a server.
> - If you experience problems saving your documents on Google Drive, check and optionally disable browser extensions, such as Disconnect.

#### <i class="icon-refresh"></i> Open a document

You can open a document from <i class="icon-provider-gdrive"></i> **Google Drive** or the <i class="icon-provider-dropbox"></i> **Dropbox** by opening the <i class="icon-refresh"></i> **Synchronize** sub-menu and by clicking **Open from...**. Once opened, any modification in your document will be automatically synchronized with the file in your **Google Drive** / **Dropbox** account.

#### <i class="icon-refresh"></i> Save a document

You can save any document by opening the <i class="icon-refresh"></i> **Synchronize** sub-menu and by clicking **Save on...**. Even if your document is already synchronized with **Google Drive** or **Dropbox**, you can export it to a another location. StackEdit can synchronize one document with multiple locations and accounts.

#### <i class="icon-refresh"></i> Synchronize a document

Once your document is linked to a <i class="icon-provider-gdrive"></i> **Google Drive** or a <i class="icon-provider-dropbox"></i> **Dropbox** file, StackEdit will periodically (every 3 minutes) synchronize it by downloading/uploading any modification. A merge will be performed if necessary and conflicts will be detected.

If you just have modified your document and you want to force the synchronization, click the <i class="icon-refresh"></i> button in the navigation bar.

> **Note:** The <i class="icon-refresh"></i> button is disabled when you have no document to synchronize.

#### <i class="icon-refresh"></i> Manage document synchronization

Since one document can be synchronized with multiple locations, you can list and manage synchronized locations by clicking <i class="icon-refresh"></i> **Manage synchronization** in the <i class="icon-refresh"></i> **Synchronize** sub-menu. This will let you remove synchronization locations that are associated to your document.

> **Note:** If you delete the file from **Google Drive** or from **Dropbox**, the document will no longer be synchronized with that location.

----------


Publication
-------------

Once you are happy with your document, you can publish it on different websites directly from StackEdit. As for now, StackEdit can publish on **Blogger**, **Dropbox**, **Gist**, **GitHub**, **Google Drive**, **Tumblr**, **WordPress** and on any SSH server.

#### <i class="icon-upload"></i> Publish a document

You can publish your document by opening the <i class="icon-upload"></i> **Publish** sub-menu and by choosing a website. In the dialog box, you can choose the publication format:

- Markdown, to publish the Markdown text on a website that can interpret it (**GitHub** for instance),
- HTML, to publish the document converted into HTML (on a blog for example),
- Template, to have a full control of the output.

> **Note:** The default template is a simple webpage wrapping your document in HTML format. You can customize it in the **Advanced** tab of the <i class="icon-cog"></i> **Settings** dialog.

#### <i class="icon-upload"></i> Update a publication

After publishing, StackEdit will keep your document linked to that publication which makes it easy for you to update it. Once you have modified your document and you want to update your publication, click on the <i class="icon-upload"></i> button in the navigation bar.

> **Note:** The <i class="icon-upload"></i> button is disabled when your document has not been published yet.

#### <i class="icon-upload"></i> Manage document publication

Since one document can be published on multiple locations, you can list and manage publish locations by clicking <i class="icon-upload"></i> **Manage publication** in the <i class="icon-provider-stackedit"></i> menu panel. This will let you remove publication locations that are associated to your document.

> **Note:** If the file has been removed from the website or the blog, the document will no longer be published on that location.

----------


Markdown Extra
--------------------

StackEdit supports **Markdown Extra**, which extends **Markdown** syntax with some nice features.

> **Tip:** You can disable any **Markdown Extra** feature in the **Extensions** tab of the <i class="icon-cog"></i> **Settings** dialog.

> **Note:** You can find more information about **Markdown** syntax [here][2] and **Markdown Extra** extension [here][3].


### Tables

**Markdown Extra** has a special syntax for tables:

Item     | Value
-------- | ---
Computer | $1600
Phone    | $12
Pipe     | $1

You can specify column alignment with one or two colons:

| Item     | Value | Qty   |
| :------- | ----: | :---: |
| Computer | $1600 |  5    |
| Phone    | $12   |  12   |
| Pipe     | $1    |  234  |


### Definition Lists

**Markdown Extra** has a special syntax for definition lists too:

Term 1
Term 2
:   Definition A
:   Definition B

Term 3

:   Definition C

:   Definition D

	> part of definition D


### Fenced code blocks

GitHub's fenced code blocks are also supported with **Highlight.js** syntax highlighting:

```
// Foo
var bar = 0;
```

> **Tip:** To use **Prettify** instead of **Highlight.js**, just configure the **Markdown Extra** extension in the <i class="icon-cog"></i> **Settings** dialog.

> **Note:** You can find more information:

> - about **Prettify** syntax highlighting [here][5],
> - about **Highlight.js** syntax highlighting [here][6].


### Footnotes

You can create footnotes like this[^footnote].

  [^footnote]: Here is the *text* of the **footnote**.


### SmartyPants

SmartyPants converts ASCII punctuation characters into "smart" typographic punctuation HTML entities. For example:

|                  | ASCII                        | HTML              |
 ----------------- | ---------------------------- | ------------------
| Single backticks | `'Isn't this fun?'`            | 'Isn't this fun?' |
| Quotes           | `"Isn't this fun?"`            | "Isn't this fun?" |
| Dashes           | `-- is en-dash, --- is em-dash` | -- is en-dash, --- is em-dash |


### Table of contents

You can insert a table of contents using the marker `[TOC]`:

[TOC]


### MathJax

You can render *LaTeX* mathematical expressions using **MathJax**, as on [math.stackexchange.com][1]:

The *Gamma function* satisfying $\Gamma(n) = (n-1)!\quad\forall n\in\mathbb N$ is via the Euler integral

$$
\Gamma(z) = \int_0^\infty t^{z-1}e^{-t}dt\,.
$$

> **Tip:** To make sure mathematical expressions are rendered properly on your website, include **MathJax** into your template:

```
<script type="text/javascript" src="https://cdn.mathjax.org/mathjax/latest/MathJax.js?config=TeX-AMS_HTML"></script>
```

> **Note:** You can find more information about **LaTeX** mathematical expressions [here][4].


### UML diagrams

You can also render sequence diagrams like this:

```sequence
Alice->Bob: Hello Bob, how are you?
Note right of Bob: Bob thinks
Bob-->Alice: I am good thanks!
```

And flow charts like this:

```flow
st=>start: Start
e=>end
op=>operation: My Operation
cond=>condition: Yes or No?

st->op->cond
cond(yes)->e
cond(no)->op
```

> **Note:** You can find more information:

> - about **Sequence diagrams** syntax [here][7],
> - about **Flow charts** syntax [here][8].

### Support StackEdit

[![](https://cdn.monetizejs.com/resources/button-32.png)](https://monetizejs.com/authorize?client_id=ESTHdCYOi18iLhhO&summary=true)

  [^stackedit]: [StackEdit](https://stackedit.io/) is a full-featured, open-source Markdown editor based on PageDown, the Markdown library used by Stack Overflow and the other Stack Exchange sites.


  [1]: http://math.stackexchange.com/
  [2]: http://daringfireball.net/projects/markdown/syntax "Markdown"
  [3]: https://github.com/jmcmanus/pagedown-extra "Pagedown Extra"
  [4]: http://meta.math.stackexchange.com/questions/5020/mathjax-basic-tutorial-and-quick-reference
  [5]: https://code.google.com/p/google-code-prettify/
  [6]: http://highlightjs.org/
  [7]: http://bramp.github.io/js-sequence-diagrams/
  [8]: http://adrai.github.io/flowchart.js/



