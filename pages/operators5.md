---
layout: default
title: Operators
---

<!-- Page Header -->
<header class="intro-header" style="background-image: url('{{ site.baseurl }}/{% if page.header-img %}{{ page.header-img }}{% else %}{{ site.header-img }}{% endif %}')">
    <div class="container">
        <div class="row">
            <div class="col-lg-8 col-lg-offset-2 col-md-10 col-md-offset-1">
                <div class="site-heading" style="padding: 75px 0">
					{% if page.url == '/' %}
					{% if site.logo %}
					<img src= "{{ site.logo }}" style="height: 150px">
					{% endif %}	
					{% else %}{% endif %}	
                    <h1>{% if page.title %}{{ page.title }}{% else %}{{ site.title }}{% endif %}</h1>
                    <hr class="small">
                    <span class="subheading">{% if page.description %}{{ page.description }}{% else %}{{ site.description }}{% endif %}</span>
                </div>
            </div>
        </div>
    </div>
</header>

<!-- main content -->

<div class="container">
	<div class="row">
		<div class="col-lg-8 col-lg-offset-2 col-md-10 col-md-offset-1">
			<button type="button" class="btn btn-outline-primary" data-toggle="collapse" data-target="#toc">Table Of Contents</button>
  <div id="toc" class="collapse" align="left" style="margin-left: 20%; line-height: 1.6; font-size: 20px;">
      <h1>Table of Contents</h1>
	<ol class="list-group list-group-flush">
		<a href="/projects/project1"><li class="list-group-item">Python Home</li></a>
		<a href="/pages/introduction2/"><li class="list-group-item">Introduction</li></a>
		<a href="/pages/variables/"><li class="list-group-item">Variables</li></a>
		<a href="/pages/numbers/"><li class="list-group-item">Numbers</li></a>
		<a href="/pages/strings4"><li class="list-group-item">Strings</li></a>
		<a href="/pages/operators5/"><li class="list-group-item active">Operators</li></a>
		<a href="#"><li class="list-group-item">Lists and Tuples</li></a>
		<a href="#"><li class="list-group-item">Sets</li></a>
		<a href="#"><li class="list-group-item">Dictionaries</li></a>
		<a href="#"><li class="list-group-item">Loops</li></a>
		<ul>
			<a href="#"><li class="list-group-item">If...Else</li></a>
			<a href="#"><li class="list-group-item">While</li></a>
			<a href="#"><li class="list-group-item">For</li></a>
		</ul>
		<a href="#"><li class="list-group-item">Functions</li></a>
		<a href="#"><li class="list-group-item">Arrays</li></a>
	</ol>
      </div>



<div class="maincontent">
  <h3>Operators</h3>
  <p>Operators in python are special symbols that carryout operations between variables or values. For example 1+2=3 here 1,2 are operands and + is the operator symbol for addition. Python hass divided operators into different groups.</p>
	<ul>
		<li>Arithmetic operators</li>
		<li>Assignment operators</li>
		<li>Comparison operators</li>
		<li>Logical operators</li>
		<li>Identity operators</li>
		<li>Membership operators</li>
		<li>Bitwise operators</li>
	</ul>
  <h4>Arithmetic operators</h4>
	<ul>
		<li><b>Addition (+)</b> - Adds two operands on both sides of the operator.<br /> 	
<!--Code block -->
<figure class="highlight">
<pre><code class="language-python" data-lang="python">
a = 5
b = 2
print(5+2)<br />
<b>Ouput:</b>
7
</code></pre>
</figure>
		</li>
		<li><b>Subtraction (-)</b>subtract two operands on both sides of the operator. <br />
<!--Code block -->
<figure class="highlight">
<pre><code class="language-python" data-lang="python">
a = 5
b = 2
print(5-2)<br />
<b>Ouput:</b>
3
</code></pre>
</figure>
		</li>
		<li><b>Multiplication (*)</b> - multiplies two operands on both sides of the operator.
<!--Code block -->
<figure class="highlight">
<pre><code class="language-python" data-lang="python">
a = 5
b = 2
print(5*2)<br />
<b>Ouput:</b>
10
</code></pre>
</figure>
		</li>
		<li><b></b></li>
		<li><b></b></li>
		<li><b></b></li>
		<li><b></b></li>
	</ul>



  <ul class="pagination justify-content-center">
  <li class="page-item"><a class="page-link" href="/pages/strings4/">Previous</a></li>
  <li class="page-item "><a class="page-link" href="/projects/project1">0</a></li>
  <li class="page-item"><a class="page-link" href="/pages/introduction2/">1</a></li>
  <li class="page-item"><a class="page-link" href="/pages/variables/">2</a></li>
  <li class="page-item"><a class="page-link" href="/pages/numbers/">3</a></li>
  <li class="page-item"><a class="page-link" href="/pages/strings4">4</a></li>
  <li class="page-item active"><a class="page-link" href="/pages/operators5/">5</a></li>
  <li class="page-item"><a class="page-link" href="#">6</a></li>
  <li class="page-item"><a class="page-link" href="#">7</a></li>
  <li class="page-item"><a class="page-link" href="#">Next</a></li>
  </ul>
</div>
  
</div>
	</div>
</div>









