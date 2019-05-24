---
layout: default
title: Variables
description: "Introduction to the python variables"

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
X = 10
name = "siva"
y = 4.5673
<span class="k">print</span><span class="p">(</span><span class="s">x)</span>
<span class="k">print</span><span class="p">(</span><span class="s">name)</span>
<span class="k">print</span><span class="p">(</span><span class="s">y)</span><br />

<span class="kn">Output:</span><br />
10
siva
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
<p>In python you have the ease of assigning a value to multiple variables. It can be done in two ways.</p>
<p>One way is assigning single same value to multiple variables. In this case all the variables refer to the same memory location.</p>
Assigning same value to multiple variables
<figure class="highlight"><pre><code class="language-python" data-lang="python">
<span class="kn">a = b = c = 5</span>
    </code></pre></figure>
 <p>Second way is assigning multiple values to multiple variables in a single line. Here all the variables will refer to different memory locations.</p>
 Assigning different values to different variables
 <figure class="highlight"><pre><code class="language-python" data-lang="python">
 <span class="kn">a, b, c = 1, 1.5, "a string"</span>
 </code></pre></figure>
 <p>Here variable a is assined with integer value 1, b is assigned with float value 1.5 and variable c is assigned with string value "a string"./p>
<p>Python has 5 standard data types. They are - </p>
<div align="center">
	<ol >
	<li>Number (int, float)</li>
	<li>String</li>
	<li>List</li>
	<li>Tuple</li>
	<li>Dictionary</li>
	</ol>
</div>
<p>We will discuss about each of the data type in brief. We will go into the deep discussion about each of them in later lessons of this course. Let's begin the introduction about each of the above............</p>
<h3>1) Numbers</h3>
<p>Numbers means numeric values. There are for different types that python supports-</p>
<div align="center">
<ul>
	<li>int (5, -5, 110, -110 etc.)</li>
	<li>long int (123456789L, 0154L, etc.)</li>
	<li>float (1.5, 3.14, 6.7567, etc.)</li>
	<li>complex (3.14j, 1+5j, 3-2j, etc)</li>
</ul>
</div>
<h3>2) String</h3>
<p>Strings in python are continuous set of characters that repreented in a single or double quotation-marks. Each character in a string will have indexes starting from zero. So we can select a substring from a string using the indexes. The index values will start from 0,1,2 etc. from the beginning and -1,-2,-3, etc. from the end of the string. We will select a substring using slice operator([start index : end index]).</p>
<figure class="highlight"><pre><code class="language-python" data-lang="python">
str = "this is a string example!"
print(str)
print(str[0:5])
<span class="kn">Output:</span>
this is a string example!
this i
</code></pre></figure>
<h3>3) List </h3>
<p>Lists are compound data-types. A list contains values separated by commas and enclosed within square brackets([]). In other programming languages like C, C++, java the lists or arrays must contain same data-types but in python all the values can be different data-types. Same as strings all the values in a list can be accessed using the slice operator with indexes starting at zero.</p>
<figure class="highlight"><pre><code class="language-python" data-lang="python">
list1 = [1, 2, 3, 1.567, "string"]
print(list1)
print(list1[2:4])
<span class="kn">Output:</span>
[1, 2, 3, 1.567, "string"]
[3, 1.567, "string"]
</code></pre></figure>
<h3>4) Tuple</h3>
<p>Tuple is a data-type very much similar to a list. But the operation that are going to perform on a tuple and a list will be different. We will discuss the differences in later chapters. The main difference is a list will be represented by using square brackets but a tuple will be enclosed in parentheses( () ).</p>
<figure class="highlight"><pre><code class="language-python" data-lang="python">
tuple1 = [1, 2, 3, 1.567, "string"]
print(tuple1)
print(tuple1[2:4])
<span class="kn">Output:</span>
(1, 2, 3, 1.567, "string")
(3, 1.567, "string")
</code></pre></figure>

<h3>5) Dictionary</h3>
<p>Dictionaries are a special kind of data-types which consists a key-value pair. A key can be any data type but mostly we will use numbers or strings. Value can be any data-type. A Dictionary should be enclosed in curly braces({}) and values can be assigned using square braces([])</p>
<figure class="highlight"><pre><code class="language-python" data-lang="python">
dict = {}
dict['a'] = "first key-value pair"
dict[2] = "second key-value pair"
print(dict)
print(dict['a'])
print(dict[2])
<span class="kn">Output:</span>
{'a': "first key-value pair", 2: "second key-value pair"}
first key-value pair
second key-value pair
</code></pre></figure>
<p>Dictionaries have no concept of indexing or ordering. The elements of dictionary are unordered.</p>
<br /> <br />
<p>That's it for this lesson.I hope you have enjoyed it. If you want to give any suggestions please let us know in the comments section.</p>
<p>Have a great day!</p>
<ul class="pagination justify-content-center">
  <li class="page-item"><a class="page-link" href="/pages/introduction2/">Previous</a></li>
  <li class="page-item "><a class="page-link" href="/projects/project1">0</a></li>
  <li class="page-item"><a class="page-link" href="/pages/introduction2/">1</a></li>
  <li class="page-item active"><a class="page-link" href="/pages/variables/">2</a></li>
  <li class="page-item"><a class="page-link" href="#">3</a></li>
  <li class="page-item"><a class="page-link" href="#">4</a></li>
  <li class="page-item"><a class="page-link" href="#">5</a></li>
  <li class="page-item"><a class="page-link" href="#">6</a></li>
  <li class="page-item"><a class="page-link" href="#">7</a></li>
  <li class="page-item"><a class="page-link" href="#">Next</a></li>
 </ul>

</div>
      
      
</div>
</div>
</div>
