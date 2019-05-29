---
layout: default
title: Lists & Tuples
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
	
<h3>Lists and Tuples</h3>
<h4>Lists</h4>
<p>From all the coumpound data types lists are the most versatile data type that used to group the values together. A list is writing all the values by separating with commas and enclosed in square brackets. Lists are ordered means elements of list have indexes and they can be changeable. Lists allow dupicate members, it means we can have same values multiple times in a list.</p>
<h4>Tuples</h4>
<p>Tuples also sequence of values or elements just like lists but the elements of a tuple are immutable(can not be changeable). Elements of a tuple are comma-spearated values enclosed in parentheses. For tupes parentheses is just optional you can define a tuple directly writing comma-separated values without parentheses.</p>
<!--Code block -->
<p>Creating a list</p>
<figure class="highlight">
<pre><code class="language-python" data-lang="python">
list1 = [1, 2, 3]
print(list1)<br />
<b>Ouput:</b>
[1, 2, 3]
</code></pre>
</figure>
<p>In a list the elements can be of same data-type or different data-type. For example a list can have some elements as integers, some elements as floats, and some elements can be even strings. A list can have another list as an element. Let's see an example</p>
<!--Code block -->
<figure class="highlight">
<pre><code class="language-python" data-lang="python">
list1 = [1, 2.64, "a string", [1, 2, 3]]
print(list1)<br />
<b>Ouput:</b>
[1, 2.64, "a string", [1, 2, 3]]
</code></pre>
</figure>

<h4>Accessing values in a list</h4>
<p>Like Strings we can access the elements by indices. The first element in a list will have index 0, second element will have index 1, and so on. To access the elements of a list we use a slice operator ([] or [:]). This [] can be used to select a single element and [:] This can be used to select a sequence of elements.</p>
<!--Code block -->
<figure class="highlight">
<pre><code class="language-python" data-lang="python">
list1 = [1, 2.64, "a string", [1, 2, 3]]
print("Single element list[1]: ", list1[1])
print("Sequence of elements list[1:4]: ", list[1:4])<br />
<b>Ouput:</b>
2.64
[2.64, "a string", [1, 2, 3]]
</code></pre>
</figure>

<h4>Updation of a list</h4>
<p>One can update the elements of a list by assigning new value to that particular element index which we want to update. We can update single or multiple elements of a list at a time. We can update list by adding new elements to the list using append() function which we can discuss in the subsequent sections.</p>
<!--Code block -->
<figure class="highlight">
<pre><code class="language-python" data-lang="python">
list1 = [1, 2.64, "a string", [1, 2, 3]]
print("Initial list: ", list1)
list1[0] = 5
print("Updating the first element: ", list1)
list1[1:4] = [1, 2, 3]
print("updating list from index1 to index3 :", list1)<br />
<b>Ouput:</b>
[1, 2.64, "a string", [1, 2, 3]]
[5, 2.64, 'a string', [1, 2, 3]]
[5, 1, 2, 3]
</code></pre>
</figure>

<h4>Delete elements of a list</h4>
<p>Inorder to delete an element from the list we use del statement by selecting the index of the element.If you do not know the index of the elemnt you can directly remove using the lement itself with remove() function which we discuss in the later sections.</p>
<!--Code block -->
<figure class="highlight">
<pre><code class="language-python" data-lang="python">
list1 = [1, 2.64, "a string", [1, 2, 3]]
print("Initial list: ", list1)
del list1[0]
print("Deleting the first element at index0: ", list1)<br />
<b>Ouput:</b>
[1, 2.64, "a string", [1, 2, 3]]
[2.64, 'a string', [1, 2, 3]]
</code></pre>
</figure>

<h4>Use of Basic Operators</h4>
<p>In python most of the basic operators are most useful for the manipulation of elements of the list. Let's see the operations with examples</p>
<ul>
	<li><b>Concatenation( Using + )</b> - concatenation means adding new elements of second list from the end of the first list.<br		/> 
<!--Code block -->
<figure class="highlight">
<pre><code class="language-python" data-lang="python">
list1 = [1, 2, 3]
list2 = [4, 5, 6]
print("concatenating list1 and list2: ", list1+list2)<br />
<b>Ouput:</b>
concatenating list1 and list2: [1, 2, 3, 4, 5, 6]
</code></pre>
</figure>
	</li>
	<li><b>Repetition (using * )</b> - In repetition we can define a list with all elements same but repeating manny times.</br>
<!--Code block -->
<figure class="highlight">
<pre><code class="language-python" data-lang="python">
print("Repeting single element 5 times in a list: ", [4]*5)<br />
<b>Ouput:</b>
Repeting single element 5 times in a list: [4, 4, 4, 4, 4]
</code></pre>
</figure>
	</li>
	<li><b>Membership operator</b><br />
<!--Code block -->
<figure class="highlight">
<pre><code class="language-python" data-lang="python">
x = [1, 2, 3]

print("Is 4 present in list? : ", 4 in x)
print("Is 3 present in list? : ", 3 in x)
<br />
<b>Ouput:</b>
Is 4 present in list? : False
Is 3 present in list? : True
</code></pre>
</figure>
	</li>
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








