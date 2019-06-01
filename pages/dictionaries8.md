---
layout: default
title: Dictionaries
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
		<a href="/pages/operators5/"><li class="list-group-item">Operators</li></a>
		<a href="/pages/lists_tuples6/"><li class="list-group-item">Lists and Tuples</li></a>
		<a href="/pages/sets7/"><li class="list-group-item">Sets</li></a>
		<a href="/projects/dictionaries8/"><li class="list-group-item active">Dictionaries</li></a>
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

<div class="article">

<h3>Dictionary</h3>
<p>Python dictionary is a poowerful data type which sometimes in other languages called associative memories. Unlike lists or tuples which are sequences indexed by a range of numbers, dictionaries are indexed by keys which can be any type; strings, numbers or tuples.
Let's see some properties of dictionaries.......</p>
<ul>
<li>Keys in dictionary should be immutable.</li>
<li>elements should be in <i>key:value</i> pairs.</li>
<li>All the keys in a dictionary should be unique.</li>
<li>Vlaues cab be of any data-type.</li>
</ul>
<p>Due to the immutable property of keys we cannnot use list as a key as the elements of a list can be changed using
index assignments or slicing assignments. A dictionary can be created by placing key:value pairs in
curly braces with comma separated.</p>
<!--Code block -->
<p>Creating a dictionary</p>
<figure class="highlight">
<pre><code class="language-python" data-lang="python">
dict1 = {1:1, 2:4, 3:9, 4:16}
print(dict1)<br />
<b>Ouput:</b>
{1: 1, 2: 4, 3: 9, 4: 16}
</code></pre>
</figure>

<h4>Accesing elements in dictionary</h4>
<ul>
<li>One can access the elements of a dictionary using it's key name inside sqare brackets.<br />
<!--Code block -->
<figure class="highlight">
<pre><code class="language-python" data-lang="python">
dict1 = {1:1, 2:4, 3:9, 4:16}
print(dict1[3])
print(dict1[4])<br />
<b>Ouput:</b>
9
16
</code></pre>
</figure>
</li>
<li>In python to access the elements of a dictionary there exists a built-in method get(). It will give the same results as above.<br />
<!--Code block -->
<figure class="highlight">
<pre><code class="language-python" data-lang="python">
dict1 = {1:1, 2:4, 3:9, 4:16}
print(dict1.get(3))
print(dict1.get(4))<br />
<b>Ouput:</b>
9
16
</code></pre>
</figure>
</li>
<li>If the key which we want to access doesnot exist in the dictionary, it will throw a keyerror.<br />
<!--Code block -->
<figure class="highlight">
<pre><code class="language-python" data-lang="python">
dict1 = {1:1, 2:4, 3:9, 4:16}
print(dict1.get(5))<br />
<b>Ouput:</b>
KeyError: 5
</code></pre>
</figure>
</li>
<li><b>Accessing elements through loops</b> - We can access all the keys or all the values using loops and methods like dict.keys() and 
	dict.values(). Let's see example for both.<br />
<!--Code block -->
<figure class="highlight">
<pre><code class="language-python" data-lang="python">
dict1 = {1:1, 2:4, 3:9, 4:16}
print("Printing all keys")
for x in dict1:
    print(x)
print("Printing all values")
for x in dict1:
    print(dict[x])
    
print("Printing all keys using dict.keys()")
for x in dict1.keys():
    print(x)
print("Printing all values using dict.values()")
for x in dict1.values():
    print(x)<br />
<b>Ouput:</b>
Printing all keys
1
2
3
4
Printing all values
1
4
9
16
Printing all keys using dict.keys()
1
2
3
4
Printing all values using dict.values()
1
4
9
16
</code></pre>
</figure>
</li>
</ul>

<h4>Updating dictionary</h4>
<ul>
<li><b>Modifying elements:</b> - We can modify the existing elements by assigning new value to the specific key of the element we want to modify<br />
<!--Code block -->
<figure class="highlight">
<pre><code class="language-python" data-lang="python">
dict1 = {1:1, 2:4, 3:9, 4:16}
dict1[2] = 5
print(dict1)<br />
<b>Ouput:</b>
{1: 1, 2: 5, 3: 9, 4: 16}
</code></pre>
</figure>
</li>
	<li><b>Adding new element</b> - We can add a new element with new key by just assigning a value to the ew key in square braces of the dictionary.<br />
<!--Code block -->
<figure class="highlight">
<pre><code class="language-python" data-lang="python">
dict1 = {1:1, 2:4, 3:9, 4:16}
dict1[5] = 25
print(dict1)<br />
<b>Ouput:</b>
{1: 1, 2: 4, 3: 9, 4: 16, 5: 25}
</code></pre>
</figure>
	</li>
</ul>

<h4>Deleting elements</h4>
<p>There are several methods and functions to remove elements from a dictionary.</p>
<ul>
<li> <b>del dict[key]</b> - It will delete the element with the key specified.<br />
<!--Code block -->
<figure class="highlight">
<pre><code class="language-python" data-lang="python">
dict1 = {1:1, 2:4, 3:9, 4:16}
del dict1[2]
print(dict1)<br />
<b>Ouput:</b>
{1: 1, 3: 9, 4: 16}
</code></pre>
</figure>	
</li>
<li><b>del dict</b> - It will delete the complete dictionary. If you try to access the dictionary after deleting it, it will throw a nameerror.<br />
<!--Code block -->
<figure class="highlight">
<pre><code class="language-python" data-lang="python">
dict1 = {1:1, 2:4, 3:9, 4:16}
del dict1
print(dict1)<br />
<b>Ouput:</b>
NameError: name 'dict1' is not defined
</code></pre>
</figure>
</li>
<li><b>dict.pop(key)</b> - This will delete and return the value of the element with the specified key. Unlike pop() method in lists here we have to give a parameter with key.<br />
<!--Code block -->
<figure class="highlight">
<pre><code class="language-python" data-lang="python">
dict1 = {1:1, 2:4, 3:9, 4:16}
x = dict1.pop(2)
print(dict1)
print(x)<br />
<b>Ouput:</b>
{1: 1, 3: 9, 4: 16}
4
</code></pre>
</figure>
</li>
<li><b>dict.popitem()</b> - this will delete and return the key:value pair. There is no need to specify which key-value pair should be deleted. It deletes the last entry of the dictionary. In python version 3.7 it will delete random key-value pair.<br />
<!--Code block -->
<figure class="highlight">
<pre><code class="language-python" data-lang="python">
dict1 = {1:1, 2:4, 3:9, 4:16}
x = dict1.popitem()
print(dict1)
print(x)<br />
<b>Ouput:</b>
{1: 1, 2:4, 3: 9}
(4,16)
</code></pre>
</figure>
</li>
<li><b>dict.clear()</b> - It will delete all the entries(key-value pairs) from the dictionary.<br />
<!--Code block -->
<figure class="highlight">
<pre><code class="language-python" data-lang="python">
dict1 = {1:1, 2:4, 3:9, 4:16}
dict1.clear()
print(dict1)<br />
<b>Ouput:</b>
{}
</code></pre>
</figure>
</li>
</ul>


<p>That's it for this lesson. I hope you all liked it. If you want to give any suggestion please feel free to let us know them through the comment section. Have a great day!</p>


  <ul class="pagination justify-content-center">
  <li class="page-item"><a class="page-link" href="/pages/sets7/">Previous</a></li>
  <li class="page-item"><a class="page-link" href="/pages/lists_tuples6/">6</a></li>
  <li class="page-item"><a class="page-link" href="/pages/sets7/">7</a></li>
  <li class="page-item active"><a class="page-link" href="/pages/dictionaries8/">8</a></li>
  <li class="page-item"><a class="page-link" href="#">9</a></li>
  <li class="page-item"><a class="page-link" href="#">10</a></li>
  <li class="page-item"><a class="page-link" href="#">11</a></li>
  <li class="page-item"><a class="page-link" href="#">12</a></li>
  <li class="page-item"><a class="page-link" href="#">13</a></li>
  <li class="page-item"><a class="page-link" href="#">14</a></li>
  <li class="page-item"><a class="page-link" href="#">Next</a></li>
  </ul>
  
  
</div>
 
</div>
</div>
</div>
