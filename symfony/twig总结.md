
<h1>twig笔记</h1>
<h2>twig中的定义了3中特殊语法</h2>
<p>{{ ... }}   说些什么，输出一个<code>变量值</code>或者一个表达式的结果显示到模板上，e.g:{{ hello }}

</p>
<p>{% ... %}   做些什么，可在该标签里做一些逻辑运算，并将结果输出到模板上，e.g:for循环{% for item in navigation %}

</p>
<p>{#  #}      注释
</p>
<h2>变量</h2>
<p>程序会传递给模板若干变量，你需要在模板里输出他们。例如输出 $hello
</p>
<pre><code class="lang-javascript">  {{ hello }}</code></pre>
<p>如果传递给模板的是对象或者数组，你可以<code>使用点 . 来输出对象的属性或者方法</code>，或者数组的成员。或者你可以使用下标的方式。
</p>
<pre><code class="lang-javascript">  {{ foo.bar }}
  {{ foo[bar] }}</code></pre>
<p>如果你访问的值不存在就会返回null。TWIG有一整套的流程来确认值是否存在。

</p>
<p>for.bar会进行以下操作
。。。如果 foo是个数组，就尝试返回bar成员，如果不存在的话，往下继续
。。。如果foo是个对象，会尝试返回bar属性，如果不存在的话，往下继续
。。。会尝试运行bar方法，如果不存在的话，往下继续
。。。会尝试运行getBar方法，如果不存在的话，往下继续
。。。会尝试运行isBar方法，如果不存在的话，返回null

</p>
<p>for['bar'] 就简单很多了 for必须是个数组，尝试返回bar成员，如果不就返回null
</p>
<h2>全局变量</h2>
<p>twig定义了一些全局变量

</p>
<ul>
<li>_self  这个参看macro标签</li>
<li>_context 这个就是当前的环境</li>
<li>_charset: 当前的字符编码<h2>变量赋值</h2>
具体参见set标签</li>
</ul>
<pre><code class="lang-javascript">{% set foo = 'foo' %}
{% set foo = [1, 2] %}
{% set foo = {'foo': 'bar'} %}</code></pre>
<h2>过滤器 Firters</h2>
<p>twig中有多种内置过滤器，Twig也包含 filters，它可以在模板输出之前改变输出内容
变量可以被过滤器修饰。过滤器和变量用（|）分割开。过滤器也是可以有参数的。过滤器也可以被多重使用。
下面这例子就使用了两个过滤器。
</p>
<pre><code class="lang-javascript">{{ name|striptags|title }}</code></pre>
<h2>函数Function</h2>
<p>TWIG内置了一些函数
举个例子 返回一个0到3的数组，就使用 range函数
</p>
<pre><code class="lang-javascript">{% for i in range(0, 3) %}
    {{ i }},
{%endfor%}</code></pre>
<h2>流程控制</h2>
<p>支持for循环 和 if/elseif/else结构
</p>
<pre><code class="lang-javascript">&lt;h1&gt;Members&lt;/h1&gt;
&lt;ul&gt;
    {% for user in users %}
        &lt;li&gt;{{ user.username|e }}&lt;/li&gt;
    {% endfor %}
&lt;/ul&gt;
``

``` javascript
&lt;h1&gt;Members&lt;/h1&gt;
&lt;ul&gt;
{% if users|length &gt; 0 %}
    &lt;ul&gt;
        {% for user in users %}
            &lt;li&gt;{{ user.username|e }}&lt;/li&gt;
        {% endfor %}
    &lt;/ul&gt;
{% endif %}
&lt;/ul&gt;</code></pre>
<h2>判断</h2>
<h2>一个变量是否定义（存在）</h2>
<pre><code class="lang-javascript">{% if item is defined %}
    {% item.name %}
{% endif %}</code></pre>
<h2>一个变量是否为空</h2>
<pre><code class="lang-javascript">{% if item is null %}
    {# do something  #}
{% endif %}</code></pre>
<h2>多条件and，or用法</h2>
<p>twig中不识别 &amp;&amp; 、|| 等，只能使用and，or
</p>
<pre><code class="lang-javascript">{% if item is defined and item %}
    {{ item.id }}  
{% else %}
    &lt;h1&gt;还没有人留言或留言已经删除&lt;/h1&gt;
{% endif %}</code></pre>
<p>Edit By <a href="http://mahua.jser.me">MaHua</a></p>
</body></html>