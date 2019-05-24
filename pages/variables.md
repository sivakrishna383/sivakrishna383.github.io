---
layout: default
title: Introduction
description: "Introduction to the python programming language"

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

<div class="container">
	<div class="row">
		<div class="col-lg-8 col-lg-offset-2 col-md-10 col-md-offset-1">
			<button type="button" class="btn btn-outline-primary" data-toggle="collapse" data-target="#toc">Table Of Contents</button>
  <div id="toc" class="collapse" align="left" style="margin-left: 20%; line-height: 1.6; font-size: 20px;">
      <h1>Table of Contents</h1>
	<ol class="list-group list-group-flush">
		<a href="/projects/project1"><li class="list-group-item">Python Home</li></a>
		<a href="/pages/introduction2/"><li class="list-group-ite">Introduction</li></a>
		<a href="#"><li class="list-group-item active">Variables</li></a>
		<a href="#"><li class="list-group-item">Numbers</li></a>
		<a href="#"><li class="list-group-item">Strings</li></a>
		<a href="#"><li class="list-group-item">Operators</li></a>
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
      
      <div class="main_cntent">
          <p>Variables are memory locations to store some values. It means that when you create a variable you are allocating some space in memory to store a value. The reserved memory will be depend on the datatype of the variable you assign.</p>
          <p>Unlike other programming languages in python there is no need of defining the data type of the variables. A  variable will be created when you first assign a value to it. The value can be any datatype. This means you can assign an integer value of 10 to a variable x by just assigning as x=5.</p>
          Examples of variable assignment
          <figure class="highlight"><pre><code class="language-python" data-lang="python">
X = 10<br />
name = "siva"<br />
y = 4.5673<br />
<span class="k">print</span><span class="p">(</span><span class="s">x)</span><br />
<span class="k">print</span><span class="p">(</span><span class="s">name)<br />
<span class="k">print</span><span class="p">(</span><span class="s">y)<br />

<span class="kn">Output:</span><br />
10<br />
siva<br />
4.5673
 </code></pre></figure>
 <p>The data type of a variable can be change at any time. For suppose at first you have iitialised a variable x=5, later in your code you initialise x="some name", then x will take the datatype integer until you assign the string data-type to x. See it in the below example.</p>
<figure class="highlight"><pre><code class="language-python" data-lang="python">
x = 5
print(x)
x = "some name!"
print(x)<br />
<span class="kn">Output: </span>
5
some name!
</code></pre></figure> 
<p>Here in the first print statement the x variable is having the iteger value 5. After the print statement we have assigned the variable x with a string value. So in the next print statement variable x is having the value of string. </p>

<h3>Multiple Assignments</h3>

</div>
      
      
      
      </div>
	</div>
</div>
