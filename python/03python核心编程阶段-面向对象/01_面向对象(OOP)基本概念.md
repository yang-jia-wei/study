<style> @media print{ .hljs{overflow: visible; word-wrap: break-word !important;} }</style></head><body><div class="markdown-body">
<h1 id="toc_0">面向对象(OOP)基本概念</h1>

<p><strong>面向对象编程</strong> —— <code>Object Oriented Programming</code> 简写 <code>OOP</code></p>

<h2 id="toc_1">目标</h2>

<ul>
<li>了解 <strong>面向对象</strong> 基本概念</li>
</ul>

<h2 id="toc_2">01. 面向对象基本概念</h2>

<ul>
<li>我们之前学习的编程方式就是 <strong>面向过程</strong> 的</li>
<li><strong>面相过程</strong> 和 <strong>面相对象</strong>，是两种不同的 <strong>编程方式</strong></li>
<li>对比 <strong>面向过程</strong> 的特点，可以更好地了解什么是 <strong>面向对象</strong></li>
</ul>

<h3 id="toc_3">1.1 过程和函数（科普）</h3>

<ul>
<li><strong>过程</strong> 是早期的一个编程概念</li>
<li><strong>过程</strong> 类似于函数，只能执行，但是没有返回值</li>
<li><strong>函数</strong> 不仅能执行，还可以返回结果</li>
</ul>

<h3 id="toc_4">1.2 面相过程 和 面相对象 基本概念</h3>

<h4 id="toc_5">1) <strong>面相过程</strong> —— <strong>怎么做</strong>？</h4>

<ol>
<li>把完成某一个需求的 <code>所有步骤</code> <code>从头到尾</code> 逐步实现</li>
<li>根据开发需求，将某些 <strong>功能独立</strong> 的代码 <strong>封装</strong> 成一个又一个 <strong>函数</strong></li>
<li>最后完成的代码，就是顺序地调用 <strong>不同的函数</strong></li>
</ol>

<p><strong>特点</strong></p>

<ol>
<li>注重 <strong>步骤与过程</strong>，不注重职责分工</li>
<li>如果需求复杂，代码会变得很复杂</li>
<li><strong>开发复杂项目，没有固定的套路，开发难度很大！</strong></li>
</ol>

<p><img src="media/15005969256819/001_%E9%9D%A2%E5%90%91%E8%BF%87%E7%A8%8B.png" alt="001_面向过程"/>￼</p>

<h4 id="toc_6">2) <strong>面向对象</strong> —— <strong>谁来做</strong>？</h4>

<blockquote>
<p>相比较函数，<strong>面向对象</strong> 是 <strong>更大</strong> 的 <strong>封装</strong>，根据 <strong>职责</strong> 在 <strong>一个对象中 封装 多个方法</strong></p>
</blockquote>

<ol>
<li>在完成某一个需求前，首先确定 <strong>职责</strong> —— <strong>要做的事情（方法）</strong></li>
<li>根据 <strong>职责</strong> 确定不同的 <strong>对象</strong>，在 <strong>对象</strong> 内部封装不同的 <strong>方法</strong>（多个）</li>
<li>最后完成的代码，就是顺序地让 <strong>不同的对象</strong> 调用 <strong>不同的方法</strong></li>
</ol>

<p><strong>特点</strong></p>

<ol>
<li>注重 <strong>对象和职责</strong>，不同的对象承担不同的职责</li>
<li>更加适合应对复杂的需求变化，<strong>是专门应对复杂项目开发，提供的固定套路</strong></li>
<li><strong>需要在面向过程基础上，再学习一些面向对象的语法</strong></li>
</ol>

<p><img src="media/15005969256819/001_%E6%A4%8D%E7%89%A9%E5%A4%A7%E6%88%98%E5%83%B5%E5%B0%B8.png" alt="001_植物大战僵尸"/>￼</p>

<p><img src="media/15005969256819/001_%E6%A4%8D%E7%89%A9%E5%A4%A7%E6%88%98%E5%83%B5%E5%B0%B8%E7%B1%BB%E5%9B%BE.png" alt="001_植物大战僵尸类图"/>￼</p>

</div></body>

</html>