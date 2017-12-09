---
layout: post
title:  "provisioning"
date:   2017-12-1 15:07:19
categories: [tutorial]
comments: true
---

<h1 id="프로비저닝provisioning이란">프로비저닝(Provisioning)이란</h1>

<p>이 포스트에서는 <strong>프로비저닝</strong> 이 어떠한 개념인지 파악하고 근래 엔지니어들이 사용하고 있는 <strong>프로비저닝</strong> 의 기술엔 어떤 것들이 있는지 몇 가지 정도만 파악해 본다.</p>

<hr>



<h2 id="1-옆팀-대리가-프로비저닝이란-말을-계속-쓰는데-그게-뭘까">1. 옆팀 대리가 프로비저닝이란 말을 계속 쓰는데 그게 뭘까?</h2>

<blockquote>
  <p><strong>사전적 의미</strong> <br>
  - 뜻 : 준비, 설비 <br>
  - 어구 : make provision : 준비하다.</p>
</blockquote>

<p>프로비전(:Provision)의 사전적 의미부터 알아보자. 일단 프로비전! 영어로는 Provision이라고 표기한다. <br>
구글 번역기도 좋지만 일단 내가 다니는 회사의 번역기로 변역해보자.(읭?) <br>
아래의 URL에 가서 Provision을 찾아보면 다음과 같이 나온다.</p>

<blockquote>
  <p><strong>카카오 어학 사전 URL : </strong><a href="http://alldic.daum.net/search.do?q=provision">http://alldic.daum.net/search.do?q=provision</a></p>
</blockquote>



<h2 id="2-그럼-it-엔지니어-혹은-종사자가-쓰는-프로비저닝의-뜻은">2. 그럼 IT 엔지니어 혹은 종사자가 쓰는 프로비저닝의 뜻은?</h2>



<h4 id="내-너에게-프로비저닝provisioning을-알려주마"><strong>내 너에게 프로비저닝(Provisioning)을 알려주마!!</strong></h4>

<p>IT에서 업무 혹은 서비스에 사용될 인프라(infra : 서버, DB 등 혹은 그 외에 많은 물리적 시스템) 리소스(자원)을 비즈니스의 요구사항에 맞추어 사용할 수 있도록 어떠한 행위를 취하는 것(결국 어떠한 행동)을 말한다.</p>

<p>관련하여 몇 가지 종류가 있다.</p>

<p><strong>서버자원 프로비저닝 (Server Resource Provisioning)</strong> <br>
우리가 흔히 서버라고 부르는 것들의 CPU, 메모리, Disk 등의 Resource를 적지적소에 배치하여 운영할 수 있도록 준비하는 일련의 행위 ( = provisioning)</p>

<p><em>* OS 프로비저닝 (OperatingSystem Provisioning)*</em> <br>
운영체제(OS)를 서버에 설치 및 설정하며 나아가 서비스를 위한 OS가 구동되는 것을 준비하는 일련의 행위 ( = provisioning )</p>

<p><strong>소프트웨어 프로비저닝 (Software Provisioning)</strong> <br>
소프트웨어를 서버에 설치 및 설정을 진행하여 필요한 부분에 대한 세팅하여 해당 소프트웨어를 실행할 수 있게 준비하는 일련의 행위 ( = provisioning)</p>

<p><strong>스토리지 프로비저닝 (Storage Provisioning)</strong> <br>
IT인프라에서 가장 근간이 되는 스토리지의 효율을 높일 수 있도록 준비하는 일련의 행위 ( = provisioning)</p>

<p><strong>계정 프로비저닝 (Account Provisioning)</strong> <br>
회사의 구성원이 조직에 배치 되거나 직무가 변경되어 HR담당자와 IT관리자는 e메일, 전사 ERP등과 같이 조직원에게 필요한 어플리케이션 혹은 그에 준하는 시스템에 필요한 계정을 생성하거나 권한 설정을 진행하는데 이러한 행위를 쉽게 할 수 있도록 준비하는 일련의 행위 ( = provisioning )</p>

<p>위와 같이 프로비저닝(일련의 준비 행위)를 작업자 (기획자가 될수도 있고 개발자가 될수도 있고 SE가 될 수도 있다.) 가 수동으로 진행하면 <strong>수동 프로비저닝</strong> 어떠한 자동화 툴을 이용하여 진행하면 <strong>자동 프로비저닝</strong> 이라고 한다.</p>

<p>잘 생각해보면 수동 프로비저닝보다 자동 프로비저닝이 훨씬 좋다는 것을 굳이 설명하지 않아도 알 수 있을거라 생각한다. <br>
그 이유는? 아무리 클라우드(Cloud)가 대세가 되고 편한 환경이 도래해도 결국 대규모 (소규모라도 해당된다)의 시스템을 유지/보수 하려면 시간이 많이 들기 때문에 당연히 <strong>자동 프로비저닝</strong>이 더 편하고 훨씬 작업자의 정신 건강에 이롭다.</p>

<p>요즘 대두되고 있는 가상화 시스템, 클라우드 컴퓨팅 환경에서는 IT 인프라 Resource를 할당, 배치, 배포등과 같은 일련의 작업이 필요한 경우가 많은데 위에서 언급했듯이 <strong>프로비저닝(Provisioning), 특히 자동 프로비저닝</strong>을 활용하면 손 쉽게 구성을 할 수 있다.</p>



<h4 id="주인장의-한줄-의견"><i class="icon-pencil"></i> <strong>주인장의 한줄 의견</strong></h4>

<blockquote>
  <p><strong>한줄 의견 : </strong>말이 되게 어려운데.. 그냥 어떠한 업무든 그 업무를 하기 위해 환경을 구성하는 IT업계의 단어… </p>
</blockquote>



<h2 id="generate-basic-ansible-script-file-기본-파일-생성">Generate basic ansible script file &lt;기본 파일 생성&gt;</h2>



<h4 id="기본-파일-생성"><strong>기본 파일 생성</strong></h4>

<p>하단의 기본 파일은 Ansible(앤서블) 프로젝트를 구성하고 있는 필수적이며 가장 기본적인 파일들이다. <br>
<strong>필히 생성</strong>해 주어야 하며 해당 필수 파일들을 얼마나 잘 구성하느냐에 따라 규모 큰 Ansible 프로젝트 일수록관리하기 쉬워진다는 걸 숙지해야 한다.</p>



<h4 id="생성할-파일-목록-table-of-files-to-generate"><i class="icon-file"></i> 생성할 파일 목록 (Table of files to generate)</h4>

<table>
<thead>
<tr>
  <th>디렉터리 경로(path)</th>
  <th>파일명(with extension : 확장자)</th>
</tr>
</thead>
<tbody><tr>
  <td>/inventories/hadoop_develop/</td>
  <td>hots</td>
</tr>
<tr>
  <td>/inventories/haddop_production/</td>
  <td>hosts</td>
</tr>
<tr>
  <td>Pipe</td>
  <td>$1</td>
</tr>
</tbody></table>


<blockquote>
  <ul>
  <li>Full access to <strong>Google Drive</strong> or <strong>Dropbox</strong> is required to be able to import any document in StackEdit. Permission restrictions can be configured in the settings.</li>
  <li>Imported documents are downloaded in your browser and are not transmitted to a server.</li>
  <li>If you experience problems saving your documents on Google Drive, check and optionally disable browser extensions, such as Disconnect.</li>
  </ul>
</blockquote>



<h4 id="open-a-document"><i class="icon-refresh"></i> Open a document</h4>

<p>You can open a document from <i class="icon-provider-gdrive"></i> <strong>Google Drive</strong> or the <i class="icon-provider-dropbox"></i> <strong>Dropbox</strong> by opening the <i class="icon-refresh"></i> <strong>Synchronize</strong> sub-menu and by clicking <strong>Open from…</strong>. Once opened, any modification in your document will be automatically synchronized with the file in your <strong>Google Drive</strong> / <strong>Dropbox</strong> account.</p>



<h4 id="save-a-document"><i class="icon-refresh"></i> Save a document</h4>

<p>You can save any document by opening the <i class="icon-refresh"></i> <strong>Synchronize</strong> sub-menu and by clicking <strong>Save on…</strong>. Even if your document is already synchronized with <strong>Google Drive</strong> or <strong>Dropbox</strong>, you can export it to a another location. StackEdit can synchronize one document with multiple locations and accounts.</p>



<h4 id="synchronize-a-document"><i class="icon-refresh"></i> Synchronize a document</h4>

<p>Once your document is linked to a <i class="icon-provider-gdrive"></i> <strong>Google Drive</strong> or a <i class="icon-provider-dropbox"></i> <strong>Dropbox</strong> file, StackEdit will periodically (every 3 minutes) synchronize it by downloading/uploading any modification. A merge will be performed if necessary and conflicts will be detected.</p>

<p>If you just have modified your document and you want to force the synchronization, click the <i class="icon-refresh"></i> button in the navigation bar.</p>

<blockquote>
  <p><strong>Note:</strong> The <i class="icon-refresh"></i> button is disabled when you have no document to synchronize.</p>
</blockquote>



<h4 id="manage-document-synchronization"><i class="icon-refresh"></i> Manage document synchronization</h4>

<p>Since one document can be synchronized with multiple locations, you can list and manage synchronized locations by clicking <i class="icon-refresh"></i> <strong>Manage synchronization</strong> in the <i class="icon-refresh"></i> <strong>Synchronize</strong> sub-menu. This will let you remove synchronization locations that are associated to your document.</p>

<blockquote>
  <p><strong>Note:</strong> If you delete the file from <strong>Google Drive</strong> or from <strong>Dropbox</strong>, the document will no longer be synchronized with that location.</p>
</blockquote>

<hr>



<h2 id="publication">Publication</h2>

<p>Once you are happy with your document, you can publish it on different websites directly from StackEdit. As for now, StackEdit can publish on <strong>Blogger</strong>, <strong>Dropbox</strong>, <strong>Gist</strong>, <strong>GitHub</strong>, <strong>Google Drive</strong>, <strong>Tumblr</strong>, <strong>WordPress</strong> and on any SSH server.</p>



<h4 id="publish-a-document"><i class="icon-upload"></i> Publish a document</h4>

<p>You can publish your document by opening the <i class="icon-upload"></i> <strong>Publish</strong> sub-menu and by choosing a website. In the dialog box, you can choose the publication format:</p>

<ul>
<li>Markdown, to publish the Markdown text on a website that can interpret it (<strong>GitHub</strong> for instance),</li>
<li>HTML, to publish the document converted into HTML (on a blog for example),</li>
<li>Template, to have a full control of the output.</li>
</ul>

<blockquote>
  <p><strong>Note:</strong> The default template is a simple webpage wrapping your document in HTML format. You can customize it in the <strong>Advanced</strong> tab of the <i class="icon-cog"></i> <strong>Settings</strong> dialog.</p>
</blockquote>



<h4 id="update-a-publication"><i class="icon-upload"></i> Update a publication</h4>

<p>After publishing, StackEdit will keep your document linked to that publication which makes it easy for you to update it. Once you have modified your document and you want to update your publication, click on the <i class="icon-upload"></i> button in the navigation bar.</p>

<blockquote>
  <p><strong>Note:</strong> The <i class="icon-upload"></i> button is disabled when your document has not been published yet.</p>
</blockquote>



<h4 id="manage-document-publication"><i class="icon-upload"></i> Manage document publication</h4>

<p>Since one document can be published on multiple locations, you can list and manage publish locations by clicking <i class="icon-upload"></i> <strong>Manage publication</strong> in the <i class="icon-provider-stackedit"></i> menu panel. This will let you remove publication locations that are associated to your document.</p>

<blockquote>
  <p><strong>Note:</strong> If the file has been removed from the website or the blog, the document will no longer be published on that location.</p>
</blockquote>

<hr>



<h2 id="markdown-extra">Markdown Extra</h2>

<p>StackEdit supports <strong>Markdown Extra</strong>, which extends <strong>Markdown</strong> syntax with some nice features.</p>

<blockquote>
  <p><strong>Tip:</strong> You can disable any <strong>Markdown Extra</strong> feature in the <strong>Extensions</strong> tab of the <i class="icon-cog"></i> <strong>Settings</strong> dialog.</p>
  
  <p><strong>Note:</strong> You can find more information about <strong>Markdown</strong> syntax <a href="http://daringfireball.net/projects/markdown/syntax" title="Markdown">here</a> and <strong>Markdown Extra</strong> extension <a href="https://github.com/jmcmanus/pagedown-extra" title="Pagedown Extra">here</a>.</p>
</blockquote>



<h3 id="tables">Tables</h3>

<p><strong>Markdown Extra</strong> has a special syntax for tables:</p>

<table>
<thead>
<tr>
  <th>Item</th>
  <th>Value</th>
</tr>
</thead>
<tbody><tr>
  <td>Computer</td>
  <td>$1600</td>
</tr>
<tr>
  <td>Phone</td>
  <td>$12</td>
</tr>
<tr>
  <td>Pipe</td>
  <td>$1</td>
</tr>
</tbody></table>


<p>You can specify column alignment with one or two colons:</p>

<table>
<thead>
<tr>
  <th align="left">Item</th>
  <th align="right">Value</th>
  <th align="center">Qty</th>
</tr>
</thead>
<tbody><tr>
  <td align="left">Computer</td>
  <td align="right">$1600</td>
  <td align="center">5</td>
</tr>
<tr>
  <td align="left">Phone</td>
  <td align="right">$12</td>
  <td align="center">12</td>
</tr>
<tr>
  <td align="left">Pipe</td>
  <td align="right">$1</td>
  <td align="center">234</td>
</tr>
</tbody></table>




<h3 id="definition-lists">Definition Lists</h3>

<p><strong>Markdown Extra</strong> has a special syntax for definition lists too:</p>

<dl>
<dt>Term 1</dt>
<dt>Term 2</dt>
<dd>Definition A</dd>

<dd>Definition B</dd>

<dt>Term 3</dt>
<dd>
<p>Definition C</p>
</dd>

<dd>
<p>Definition D</p>

<blockquote>
  <p>part of definition D</p>
</blockquote>
</dd>
</dl>



<h3 id="fenced-code-blocks">Fenced code blocks</h3>

<p>GitHub’s fenced code blocks are also supported with <strong>Highlight.js</strong> syntax highlighting:</p>



<pre class="prettyprint"><code class=" hljs cs"><span class="hljs-comment">// Foo</span>
<span class="hljs-keyword">var</span> bar = <span class="hljs-number">0</span>;</code></pre>

<blockquote>
  <p><strong>Tip:</strong> To use <strong>Prettify</strong> instead of <strong>Highlight.js</strong>, just configure the <strong>Markdown Extra</strong> extension in the <i class="icon-cog"></i> <strong>Settings</strong> dialog.</p>
  
  <p><strong>Note:</strong> You can find more information:</p>
  
  <ul>
  <li>about <strong>Prettify</strong> syntax highlighting <a href="https://code.google.com/p/google-code-prettify/">here</a>,</li>
  <li>about <strong>Highlight.js</strong> syntax highlighting <a href="http://highlightjs.org/">here</a>.</li>
  </ul>
</blockquote>



<h3 id="footnotes">Footnotes</h3>

<p>You can create footnotes like this<a href="#fn:footnote" id="fnref:footnote" title="See footnote" class="footnote">1</a>.</p>



<h3 id="smartypants">SmartyPants</h3>

<p>SmartyPants converts ASCII punctuation characters into “smart” typographic punctuation HTML entities. For example:</p>

<table>
<thead>
<tr>
  <th></th>
  <th>ASCII</th>
  <th>HTML</th>
</tr>
</thead>
<tbody><tr>
  <td>Single backticks</td>
  <td><code>'Isn't this fun?'</code></td>
  <td>‘Isn’t this fun?’</td>
</tr>
<tr>
  <td>Quotes</td>
  <td><code>"Isn't this fun?"</code></td>
  <td>“Isn’t this fun?”</td>
</tr>
<tr>
  <td>Dashes</td>
  <td><code>-- is en-dash, --- is em-dash</code></td>
  <td>– is en-dash, — is em-dash</td>
</tr>
</tbody></table>




<h3 id="table-of-contents">Table of contents</h3>

<p>You can insert a table of contents using the marker <code>[TOC]</code>:</p>

<p><div class="toc">
<ul>
<li><a href="#프로비저닝provisioning이란">프로비저닝(Provisioning)이란</a><ul>
<li><a href="#1-옆팀-대리가-프로비저닝이란-말을-계속-쓰는데-그게-뭘까">1. 옆팀 대리가 프로비저닝이란 말을 계속 쓰는데 그게 뭘까?</a></li>
<li><a href="#2-그럼-it-엔지니어-혹은-종사자가-쓰는-프로비저닝의-뜻은">2. 그럼 IT 엔지니어 혹은 종사자가 쓰는 프로비저닝의 뜻은?</a><ul>
<li><ul>
<li><a href="#내-너에게-프로비저닝provisioning을-알려주마">내 너에게 프로비저닝(Provisioning)을 알려주마!!</a></li>
<li><a href="#주인장의-한줄-의견"> 주인장의 한줄 의견</a></li>
</ul>
</li>
</ul>
</li>
<li><a href="#generate-basic-ansible-script-file-기본-파일-생성">Generate basic ansible script file &lt;기본 파일 생성&gt;</a><ul>
<li><ul>
<li><a href="#기본-파일-생성">기본 파일 생성</a></li>
<li><a href="#생성할-파일-목록-table-of-files-to-generate"> 생성할 파일 목록 (Table of files to generate)</a></li>
<li><a href="#open-a-document"> Open a document</a></li>
<li><a href="#save-a-document"> Save a document</a></li>
<li><a href="#synchronize-a-document"> Synchronize a document</a></li>
<li><a href="#manage-document-synchronization"> Manage document synchronization</a></li>
</ul>
</li>
</ul>
</li>
<li><a href="#publication">Publication</a><ul>
<li><ul>
<li><a href="#publish-a-document"> Publish a document</a></li>
<li><a href="#update-a-publication"> Update a publication</a></li>
<li><a href="#manage-document-publication"> Manage document publication</a></li>
</ul>
</li>
</ul>
</li>
<li><a href="#markdown-extra">Markdown Extra</a><ul>
<li><a href="#tables">Tables</a></li>
<li><a href="#definition-lists">Definition Lists</a></li>
<li><a href="#fenced-code-blocks">Fenced code blocks</a></li>
<li><a href="#footnotes">Footnotes</a></li>
<li><a href="#smartypants">SmartyPants</a></li>
<li><a href="#table-of-contents">Table of contents</a></li>
<li><a href="#mathjax">MathJax</a></li>
<li><a href="#uml-diagrams">UML diagrams</a></li>
<li><a href="#support-stackedit">Support StackEdit</a></li>
</ul>
</li>
</ul>
</li>
</ul>
</div>
</p>



<h3 id="mathjax">MathJax</h3>

<p>You can render <em>LaTeX</em> mathematical expressions using <strong>MathJax</strong>, as on <a href="http://math.stackexchange.com/">math.stackexchange.com</a>:</p>

<p>The <em>Gamma function</em> satisfying <script type="math/tex" id="MathJax-Element-1">\Gamma(n) = (n-1)!\quad\forall n\in\mathbb N</script> is via the Euler integral</p>



<p><script type="math/tex; mode=display" id="MathJax-Element-2">
\Gamma(z) = \int_0^\infty t^{z-1}e^{-t}dt\,.
</script></p>

<blockquote>
  <p><strong>Tip:</strong> To make sure mathematical expressions are rendered properly on your website, include <strong>MathJax</strong> into your template:</p>
</blockquote>



<pre class="prettyprint"><code class=" hljs xml"><span class="hljs-tag">&lt;<span class="hljs-title">script</span> <span class="hljs-attribute">type</span>=<span class="hljs-value">"text/javascript"</span> <span class="hljs-attribute">src</span>=<span class="hljs-value">"https://cdn.mathjax.org/mathjax/latest/MathJax.js?config=TeX-AMS_HTML"</span>&gt;</span><span class="javascript"></span><span class="hljs-tag">&lt;/<span class="hljs-title">script</span>&gt;</span></code></pre>

<blockquote>
  <p><strong>Note:</strong> You can find more information about <strong>LaTeX</strong> mathematical expressions <a href="http://meta.math.stackexchange.com/questions/5020/mathjax-basic-tutorial-and-quick-reference">here</a>.</p>
</blockquote>



<h3 id="uml-diagrams">UML diagrams</h3>

<p>You can also render sequence diagrams like this:</p>



<div class="sequence-diagram"><svg height="267.5" version="1.1" width="378.3249979019165" xmlns="http://www.w3.org/2000/svg" xmlns:xlink="http://www.w3.org/1999/xlink" style="overflow: hidden; position: relative; left: -0.5px; top: -0.0664063px;"><desc>Created with Raphaël 2.1.2</desc><defs><path stroke-linecap="round" d="M5,0 0,2.5 5,5z" id="raphael-marker-block"></path><marker id="raphael-marker-endblock55-obj21" markerHeight="5" markerWidth="5" orient="auto" refX="2.5" refY="2.5"><use xlink:href="#raphael-marker-block" transform="rotate(180 2.5 2.5) scale(1,1)" stroke-width="1.0000" fill="#000" stroke="none"></use></marker><marker id="raphael-marker-endblock55-obj27" markerHeight="5" markerWidth="5" orient="auto" refX="2.5" refY="2.5"><use xlink:href="#raphael-marker-block" transform="rotate(180 2.5 2.5) scale(1,1)" stroke-width="1.0000" fill="#000" stroke="none"></use></marker></defs><rect x="10" y="20" width="50.61666679382324" height="39.5" rx="0" ry="0" fill="none" stroke="#000000" style="" stroke-width="2"></rect><rect x="20.000001907348633" y="30" width="30.616666793823242" height="19.5" rx="0" ry="0" fill="#ffffff" stroke="none" style=""></rect><text style="text-anchor: middle; font-family: Andale\ Mono, monospace; font-size: 16px;" x="35.30833339691162" y="39.75" text-anchor="middle" font-family="Andale Mono, monospace" font-size="16px" stroke="none" fill="#000000"><tspan dy="5.25">Alice</tspan></text><rect x="10" y="208" width="50.61666679382324" height="39.5" rx="0" ry="0" fill="none" stroke="#000000" style="" stroke-width="2"></rect><rect x="20.000001907348633" y="218" width="30.616666793823242" height="19.5" rx="0" ry="0" fill="#ffffff" stroke="none" style=""></rect><text style="text-anchor: middle; font-family: Andale\ Mono, monospace; font-size: 16px;" x="35.30833339691162" y="227.75" text-anchor="middle" font-family="Andale Mono, monospace" font-size="16px" stroke="none" fill="#000000"><tspan dy="5.25">Alice</tspan></text><path style="" fill="none" stroke="#000000" d="M35.30833339691162,59.5L35.30833339691162,208" stroke-width="2"></path><rect x="183.9416627883911" y="20" width="46.266666412353516" height="39.5" rx="0" ry="0" fill="none" stroke="#000000" style="" stroke-width="2"></rect><rect x="193.94166564941406" y="30" width="26.266666412353516" height="19.5" rx="0" ry="0" fill="#ffffff" stroke="none" style=""></rect><text style="text-anchor: middle; font-family: Andale\ Mono, monospace; font-size: 16px;" x="207.07499599456787" y="39.75" text-anchor="middle" font-family="Andale Mono, monospace" font-size="16px" stroke="none" fill="#000000"><tspan dy="5.25">Bob</tspan></text><rect x="183.9416627883911" y="208" width="46.266666412353516" height="39.5" rx="0" ry="0" fill="none" stroke="#000000" style="" stroke-width="2"></rect><rect x="193.94166564941406" y="218" width="26.266666412353516" height="19.5" rx="0" ry="0" fill="#ffffff" stroke="none" style=""></rect><text style="text-anchor: middle; font-family: Andale\ Mono, monospace; font-size: 16px;" x="207.07499599456787" y="227.75" text-anchor="middle" font-family="Andale Mono, monospace" font-size="16px" stroke="none" fill="#000000"><tspan dy="5.25">Bob</tspan></text><path style="" fill="none" stroke="#000000" d="M207.07499599456787,59.5L207.07499599456787,208" stroke-width="2"></path><rect x="45.30833053588867" y="74.75" width="151.76666259765625" height="19.5" rx="0" ry="0" fill="#ffffff" stroke="none" style=""></rect><text style="text-anchor: middle; font-family: Andale\ Mono, monospace; font-size: 16px;" x="121.19166469573975" y="84.5" text-anchor="middle" font-family="Andale Mono, monospace" font-size="16px" stroke="none" fill="#000000"><tspan dy="5.25">Hello Bob, how are you?</tspan></text><path style="" fill="none" stroke="#000000" d="M35.30833339691162,99C35.30833339691162,99,173.80599196885305,99,202.0735804859778,99" stroke-width="2" marker-end="url(#raphael-marker-endblock55-obj21)" stroke-dasharray="0"></path><rect x="227.07499599456787" y="119" width="78.11666870117188" height="29.5" rx="0" ry="0" fill="none" stroke="#000000" style="" stroke-width="2"></rect><rect x="232.0749969482422" y="124" width="68.11666870117188" height="19.5" rx="0" ry="0" fill="#ffffff" stroke="none" style=""></rect><text style="text-anchor: middle; font-family: Andale\ Mono, monospace; font-size: 16px;" x="266.1333303451538" y="133.75" text-anchor="middle" font-family="Andale Mono, monospace" font-size="16px" stroke="none" fill="#000000"><tspan dy="5.25">Bob thinks</tspan></text><rect x="64.56666564941406" y="163.75" width="113.25" height="19.5" rx="0" ry="0" fill="#ffffff" stroke="none" style=""></rect><text style="text-anchor: middle; font-family: Andale\ Mono, monospace; font-size: 16px;" x="121.19166469573975" y="173.5" text-anchor="middle" font-family="Andale Mono, monospace" font-size="16px" stroke="none" fill="#000000"><tspan dy="5.25">I am good thanks!</tspan></text><path style="" fill="none" stroke="#000000" d="M207.07499599456787,188C207.07499599456787,188,68.57733742262644,188,40.30974890550168,188" stroke-width="2" marker-end="url(#raphael-marker-endblock55-obj27)" stroke-dasharray="6,2"></path></svg></div>

<p>And flow charts like this:</p>



<div class="flow-chart"><svg height="404.78125190734863" version="1.1" width="173.0250015258789" xmlns="http://www.w3.org/2000/svg" xmlns:xlink="http://www.w3.org/1999/xlink" style="overflow: hidden; position: relative; top: -0.816406px;"><desc>Created with Raphaël 2.1.2</desc><defs><marker id="raphael-marker-endblock33-obj36" markerHeight="3" markerWidth="3" orient="auto" refX="1.5" refY="1.5"><use xlink:href="#raphael-marker-block" transform="rotate(180 1.5 1.5) scale(0.6,0.6)" stroke-width="1.6667" fill="black" stroke="none"></use></marker><marker id="raphael-marker-endblock33-obj37" markerHeight="3" markerWidth="3" orient="auto" refX="1.5" refY="1.5"><use xlink:href="#raphael-marker-block" transform="rotate(180 1.5 1.5) scale(0.6,0.6)" stroke-width="1.6667" fill="black" stroke="none"></use></marker><marker id="raphael-marker-endblock33-obj38" markerHeight="3" markerWidth="3" orient="auto" refX="1.5" refY="1.5"><use xlink:href="#raphael-marker-block" transform="rotate(180 1.5 1.5) scale(0.6,0.6)" stroke-width="1.6667" fill="black" stroke="none"></use></marker><marker id="raphael-marker-endblock33-obj40" markerHeight="3" markerWidth="3" orient="auto" refX="1.5" refY="1.5"><use xlink:href="#raphael-marker-block" transform="rotate(180 1.5 1.5) scale(0.6,0.6)" stroke-width="1.6667" fill="black" stroke="none"></use></marker></defs><rect x="0" y="0" width="51.766666412353516" height="39.5" rx="20" ry="20" fill="#ffffff" stroke="#000000" style="" stroke-width="2" class="flowchart" id="st" transform="matrix(1,0,0,1,49.1292,19.7563)"></rect><text style="text-anchor: start; font-family: sans-serif; font-size: 14px; font-weight: normal;" x="10" y="19.75" text-anchor="start" font-family="sans-serif" font-size="14px" stroke="none" fill="#000000" id="stt" class="flowchartt" font-weight="normal" transform="matrix(1,0,0,1,49.1292,19.7563)"><tspan dy="5.25">Start</tspan></text><rect x="0" y="0" width="105.25" height="39.5" rx="0" ry="0" fill="#ffffff" stroke="#000000" style="" stroke-width="2" class="flowchart" id="op" transform="matrix(1,0,0,1,22.3875,129.0125)"></rect><text style="text-anchor: start; font-family: sans-serif; font-size: 14px; font-weight: normal;" x="10" y="19.75" text-anchor="start" font-family="sans-serif" font-size="14px" stroke="none" fill="#000000" id="opt" class="flowchartt" font-weight="normal" transform="matrix(1,0,0,1,22.3875,129.0125)"><tspan dy="5.25">My Operation</tspan></text><path style="font-family: sans-serif; font-weight: normal;" fill="#ffffff" stroke="#000000" d="M35.50625038146973,17.753125190734863L0,35.50625038146973L71.01250076293945,71.01250076293945L142.0250015258789,35.50625038146973L71.01250076293945,0L0,35.50625038146973" stroke-width="2" font-family="sans-serif" font-weight="normal" id="cond" class="flowchart" transform="matrix(1,0,0,1,4,222.5125)"></path><text style="text-anchor: start; font-family: sans-serif; font-size: 14px; font-weight: normal;" x="40.50625038146973" y="35.50625038146973" text-anchor="start" font-family="sans-serif" font-size="14px" stroke="none" fill="#000000" id="condt" class="flowchartt" font-weight="normal" transform="matrix(1,0,0,1,4,222.5125)"><tspan dy="5.250001907348633">Yes or No?</tspan><tspan dy="18" x="40.50625038146973"></tspan></text><rect x="0" y="0" width="45.41666603088379" height="39.5" rx="20" ry="20" fill="#ffffff" stroke="#000000" style="" stroke-width="2" class="flowchart" id="e" transform="matrix(1,0,0,1,52.3042,363.2813)"></rect><text style="text-anchor: start; font-family: sans-serif; font-size: 14px; font-weight: normal;" x="10" y="19.75" text-anchor="start" font-family="sans-serif" font-size="14px" stroke="none" fill="#000000" id="et" class="flowchartt" font-weight="normal" transform="matrix(1,0,0,1,52.3042,363.2813)"><tspan dy="5.25">End</tspan></text><path style="font-family: sans-serif; font-weight: normal;" fill="none" stroke="#000000" d="M75.01250076293945,59.25625038146973C75.01250076293945,59.25625038146973,75.01250076293945,112.66337957978249,75.01250076293945,126.01516187936068" stroke-width="2" marker-end="url(#raphael-marker-endblock33-obj36)" font-family="sans-serif" font-weight="normal"></path><path style="font-family: sans-serif; font-weight: normal;" fill="none" stroke="#000000" d="M75.01250076293945,168.51250076293945C75.01250076293945,168.51250076293945,75.01250076293945,208.16660070419312,75.01250076293945,219.5129398475401" stroke-width="2" marker-end="url(#raphael-marker-endblock33-obj37)" font-family="sans-serif" font-weight="normal"></path><path style="font-family: sans-serif; font-weight: normal;" fill="none" stroke="#000000" d="M75.01250076293945,293.5250015258789C75.01250076293945,293.5250015258789,75.01250076293945,346.93213072419167,75.01250076293945,360.28391302376986" stroke-width="2" marker-end="url(#raphael-marker-endblock33-obj38)" font-family="sans-serif" font-weight="normal"></path><text style="text-anchor: start; font-family: sans-serif; font-size: 14px; font-weight: normal;" x="80.01250076293945" y="303.5250015258789" text-anchor="start" font-family="sans-serif" font-size="14px" stroke="none" fill="#000000" font-weight="normal"><tspan dy="5.250007629394531">yes</tspan></text><path style="font-family: sans-serif; font-weight: normal;" fill="none" stroke="#000000" d="M146.0250015258789,258.0187511444092C146.0250015258789,258.0187511444092,171.0250015258789,258.0187511444092,171.0250015258789,258.0187511444092C171.0250015258789,258.0187511444092,171.0250015258789,104.01250076293945,171.0250015258789,104.01250076293945C171.0250015258789,104.01250076293945,75.01250076293945,104.01250076293945,75.01250076293945,104.01250076293945C75.01250076293945,104.01250076293945,75.01250076293945,119.3859453201294,75.01250076293945,126.02174853719771" stroke-width="2" marker-end="url(#raphael-marker-endblock33-obj40)" font-family="sans-serif" font-weight="normal"></path><text style="text-anchor: start; font-family: sans-serif; font-size: 14px; font-weight: normal;" x="151.0250015258789" y="248.01875114440918" text-anchor="start" font-family="sans-serif" font-size="14px" stroke="none" fill="#000000" font-weight="normal"><tspan dy="5.249998092651367">no</tspan></text></svg></div>

<blockquote>
  <p><strong>Note:</strong> You can find more information:</p>
  
  <ul>
  <li>about <strong>Sequence diagrams</strong> syntax <a href="http://bramp.github.io/js-sequence-diagrams/">here</a>,</li>
  <li>about <strong>Flow charts</strong> syntax <a href="http://adrai.github.io/flowchart.js/">here</a>.</li>
  </ul>
</blockquote>



<h3 id="support-stackedit">Support StackEdit</h3>

<p><a href="https://monetizejs.com/authorize?client_id=ESTHdCYOi18iLhhO&amp;summary=true"><img src="https://cdn.monetizejs.com/resources/button-32.png" alt="" title=""></a></p>

<div class="footnotes"><hr><ol><li id="fn:footnote">Here is the <em>text</em> of the <strong>footnote</strong>. <a href="#fnref:footnote" title="Return to article" class="reversefootnote">↩</a></li></ol></div>



