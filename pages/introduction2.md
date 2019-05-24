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
		<a href="/pages/introduction2/"><li class="list-group-item active">Introduction</li></a>
		<a href="/pages/variables/"><li class="list-group-item">Variables</li></a>
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



<div class="maincontent">
      <p>Python is a widely using general purpose programming language. It was created by <b>Guido van Rossum</b> in 1991 and developed Python Software Foundation</p>
      <blockquote style="border-left: 5px solid #7dc246; margin: 10px 0;padding-left: 1.5rem; display: block;">
      	<p>
      		<strong>Fact:</strong>
      		Python is named after the comedy television show Monty Python’s Flying Circus. It was not named after the Python snake as it's name and logo looks similar.
      	</p>
      </blockquote>
      <h3>Applications of Python</h3>
      <ul>
      	<li><b>Web Development:-</b> There are some frameworks like Django and Flask for web development which are slely using python. They will help you write the backend code for a website which includes main functions like manage database and mapping urls etc.</li>

<li><b>Machine Learning:-</b> Machine learning is a way to write a logic or teach a machine so that the machine can learn and solve a particular problem on its own.There are plenty of python libraries available for machine learing which makes python as a most popular language for machine learning.</li>
      	<li><b>Data analysis:-</b> It is a part of machine learning and data science field. Data visualization and analization can also be developed in python.</li>
      	<li><b>Scripting:-</b> It is small programs written in python to automate regular and most frequently uing tasks.</li>
      	<li><b>Game development:-</b> One can develop games in Pygame which is based on python language.</li>
      	<li><b>Desktop Applications:-</b> There are libraries in python like TKinter or QT which are used to develop beatiful desktop applications using python.</li>
      </ul>
      <h3>Installing Python</h3>
      <p>Python installation is very simple, you can install it on any operating system such as Windows, Mac OS X, Ubuntu etc. Just follow the steps in this article<a href="https://realpython.com/installing-python/"></a>. In most of the linux based operating systems python may be already pre installed. You can check it by typing <b>python --version</b> in a terminal. It will show the result the python version which is installed on your pc or desktop.</p>
      <figure class="highlight"><pre><code class="language-python" data-lang="python">    <span class="kn">>>> python --version</span>
      <br /><span>Output should be like this</span>
<span class="kn"> Python 3.6.4</span>
    </code></pre></figure>
    <h3>Python Syntax</h3>
    <p>
	<figure class="highlight"><pre><code class="language-python" data-lang="python">    
<span class="kn">>>> print("Hello World!")</span>
<span class="kn">Hello World!</span>
    </code></pre></figure>
   </p>
   <h3>Indentation</h3>
   <p>Unlike other languages python must have indentation when writing a function or a loop. Other languages will use indentatio for readablity but in pythn it is necessary to have indentation. If you do not follow the default indentation rules it will throw an error</p>
   Correct Code with indentation
   <figure class="highlight"><pre><code class="language-python" data-lang="python">if 5 > 2:
&nbsp;&nbsp;print("True")<br />
<span class="kn">Output: True</span>
    </code></pre></figure>
    
  Code with no indentation
   <figure class="highlight"><pre><code class="language-python" data-lang="python">if 5 > 2:
print("True")<br />
<span class="kn">Output: IndentationError: expected an indented block</span>
    </code></pre></figure>
    
   <h3>Comments</h3>
   <p>Comments make a code more readable. Python has a simple way to represent a comment. A comment in python will start with a #, and the complete line after the hashtag symbol will be treated as a comment and that line will not be executed by the python.</p>
   Code with a Comment
   <figure class="highlight"><pre><code class="language-python" data-lang="python">
#This is a comment 
print("Hello world!")<br />
<span class="kn">Output: Hello world!</span>
    </code></pre></figure>
    
   <h3>MultiLine comments(Doc Strings)</h3>
   <p>Doc strings are special type in python that enables multiline or single line comments. Doc string will have triple quotes at the begining and end as well.</p>
   Code with a multiline docstring
   <figure class="highlight"><pre><code class="language-python" data-lang="python">"""This is a 
multiline docstring."""<br/>
print("Hello, World!")<br />
<span class="kn">Output: Hello world!</span>
    </code></pre></figure>
    <p>That's it for this lesson. I hope you get the basic introduction to the python language syntax. We will meet in the next lesson. Until then bye-bye!!!!!!!!!!!!!! <br/> Have a great day!</p>
  
  <ul class="pagination justify-content-center">
  <li class="page-item"><a class="page-link" href="/projects/project1">Previous</a></li>
  <li class="page-item "><a class="page-link" href="/projects/project1">0</a></li>
  <li class="page-item active"><a class="page-link" href="/pages/introduction2/">1</a></li>
  <li class="page-item"><a class="page-link" href="/pages/variables/">2</a></li>
  <li class="page-item"><a class="page-link" href="#">3</a></li>
  <li class="page-item"><a class="page-link" href="#">4</a></li>
  <li class="page-item"><a class="page-link" href="#">5</a></li>
  <li class="page-item"><a class="page-link" href="#">6</a></li>
  <li class="page-item"><a class="page-link" href="#">7</a></li>
  <li class="page-item"><a class="page-link" href="/pages/variables/">Next</a></li>
  </ul>
</div>
  
</div>
	</div>
</div>









