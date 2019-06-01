---
layout: default
title: Sets
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
		<a href="/pages/sets7/"><li class="list-group-item active">Sets</li></a>
		<a href="/pages/dictionaries8/"><li class="list-group-item">Dictionaries</li></a>
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
  <h4>Sets</h4>
  <p>The concept of set is the most fundamental in mathematics. According to mathematics a set is a collection of distinct objects, considered as an object in its own right. A python set has the following main properties...........</p>
  <ul>
    <li>Elements or objects of a set are unordered.</li>
    <li>Elements or objects of a set are unindexed.</li>
    <li>No duplicate elements in a list.</li>
  </ul>
  <p>A set can be initialized by placing elements in curly braces with a comma seperator or simply by using built-in function <b>set()</b>. Like lists a set can have elements with different data-types. </p>
<!--Code block -->
<p>Creating a set</p>
<figure class="highlight">
<pre><code class="language-python" data-lang="python">
set1 = {1, 2, 3, 'string object', 2.567}
print(set1)<br />
<b>Ouput:</b>
{1, 2, 3, 'string object', 2.567}
</code></pre>
</figure>
<h3>Let's see some functions or operations on sets.</h3>
<h3>Accessing elements</h3>
<p>Since the set is unordered and unindexed one cannot access elements of a set by using indexes. But you can access elements using <i>for</i> loop by asking whether an element is prsent in a set by using the <i>in</i> keyword. As elements in a set are unordered it can access elements randomly.</p>
<!--Code block -->
<figure class="highlight">
<pre><code class="language-python" data-lang="python">
set1 = {1, 2, 3, 'string object', 2.567}
for i in set1:
    print(set1)<br />
<b>Ouput:</b>
1
2.567
2
3
set string
</code></pre>
</figure>
  
<h4>Updating or modifying a set</h4>
<p>Once a set is created we can not update the values of elements. But we can add new elements to the set. Inorder to add a new item to the set there is a built-in method <i>add()</i>. If you want to add multiple elements you can use another built-in function <i>update()</i>. In update() function you must enclose elements inside square-braces([ ])-list or flower-braces({ })-set or parenthesis(( ))-tuple. Let's see an example.</p>
<!--Code block -->
<figure class="highlight">
<pre><code class="language-python" data-lang="python">
set1 = {1, 2, 3, 'string object', 2.567}
print(set1)
set1.add(4)
print(set1)
set1.update({5,6})
print(set1)
set1.update([7,8])
print(set1)
set1.update((9,10))
print(set1)<br />
<b>Ouput:</b>
{1, 2.567, 2, 3, 'set string'}
{1, 2.567, 2, 3, 4, 'set string'}
{1, 2.567, 2, 3, 4, 5, 6, 'set string'}
{1, 2.567, 2, 3, 4, 5, 6, 7, 8, 'set string'}
{1, 2.567, 2, 3, 4, 5, 6, 7, 8, 9, 10, 'set string'}
</code></pre>
</figure>

<h4>Length Of the set</h4>
<p>It will give the total number of elements in a set.</p>
<!--Code block -->
<figure class="highlight">
<pre><code class="language-python" data-lang="python">
set1 = {1, 2, 3, 'string object', 2.567}
print(len(set1))<br />
<b>Ouput:</b>
5
</code></pre>
</figure>

<h4>Removing items</h4>
	<ul>
		<li><b>remove()</b> - using the remove method you can delete a specific element from the set. If 
      the element not present in the set it will raise a keyerror.<br>
<!--Code block -->
<figure class="highlight">
<pre><code class="language-python" data-lang="python">
set1 = {1, 2, 3, 'string object', 2.567}
set1.remove('string object')
print(set1)<br />
<b>Ouput:</b>
{1, 2.567, 2, 3}
</code></pre>
</figure>
		</li>
		<li><b>discard()</b> - It works same as remove() but it will not raise an error.<br>
<!--Code block -->
<figure class="highlight">
<pre><code class="language-python" data-lang="python">
set1 = {1, 2, 3, 'string object', 2.567}
set1.discard(4)
print(set1)<br />
<b>Ouput:</b>
{1, 2.567, 2, 3, 'string object'}
</code></pre>
</figure>
		</li>
		<li><b>pop()</b> - We can use pop() method also to remove an element from a set, but one 
      disadvantage because of the properties of a set is elements are unordered and unindexed. So using 
      pop() one element will be deleted but you will not know before which element can be deleted. This 
      method returns the deleted value or element.<br>
<!--Code block -->
<figure class="highlight">
<pre><code class="language-python" data-lang="python">
set1 = {1, 2, 3, 'string object', 2.567}
x = set1.pop()
print(x)
print(set1)<br />
<b>Ouput:</b>
1
{ 2.567, 2, 3, 'string object'}
</code></pre>
</figure>
		</li>
		<li><b>clear()</b> - By using this method all the elements of the set will be deleted. So it will 
      results our set into an empty set which has zero elements.<br>
 <!--Code block -->
<figure class="highlight">
<pre><code class="language-python" data-lang="python">
set1 = {1, 2, 3, 'string object', 2.567}
set1.clear()
print(set1)
print(len(set1))<br />
<b>Ouput:</b>
set()
0
</code></pre>
</figure>
		</li>
		<li><b>del set</b> - Using this keyword the set will be completely deleted and we can not access it 
      after deleting it. If you try to access after deleting a set it will throw an error saying name 
      set is not defined.<br>
 <!--Code block -->
<figure class="highlight">
<pre><code class="language-python" data-lang="python">
set1 = {1, 2, 3, 'string object', 2.567}
del set1
print(set1)<br />
<b>Ouput:</b>
NameError: name 'set1' is not defined
</code></pre>
</figure>
		</li>
	</ul>
<h4>Regular mathematical set methods</h4>
<p>In python there are different methods existing to apply general mathematical operations on sets.</p>
	<ul>
		<li><b>set1.difference(set2)</b> - It returns a set that contains items that only present in set1 and does not present in set2.<br /><img src="/img/set_difference.png" width="240" height="200"/>
<!--Code block -->
<figure class="highlight">
<pre><code class="language-python" data-lang="python">
set1 = {1, 2, 3, 4, 5, 6}
set2 = {3, 5, 7, 9, 11, 13}
print(set1.difference(set2))
print(set2.difference(set1))
<br />
<b>Ouput:</b>
{1, 2, 4, 6}
{9, 11, 13, 7}
</code></pre>
</figure>
		</li>
		<li><b>set1.intesection(set2)</b> - It returns a set that contains elements which are in common to the set1 and set2. This means new set will contain elements that are present in both set1 and set2.<br /><img src="/img/set_intersection.png"  width="240" height="200"/>
<!--Code block -->
<figure class="highlight">
<pre><code class="language-python" data-lang="python">
set1 = {1, 2, 3, 4, 5, 6}
set2 = {3, 5, 7, 9, 11, 13}
print(set1.intersection(set2))
<br />
<b>Ouput:</b>
{3, 5}
</code></pre>
</figure>
		</li>
		<li><b>set1.isdisjoint(set2)</b> - It returns True if both sets have atleast one element in common. It returns false if there are zero elements in common to both sets.
<!--Code block -->
<figure class="highlight">
<pre><code class="language-python" data-lang="python">
set1 = {1, 2, 3, 4, 5, 6}
set2 = {3, 5, 7, 9, 11, 13}
set3 = {10, 11, 12, 13, 14}
print(set1.isdisjoint(set2))
print(set1.isdisjoint(set3))
<br />
<b>Ouput:</b>
True
False
</code></pre>
</figure>
		</li>
		<li><b>set1.issubset(set2)</b> - It returns true if all the elements of set1 present in set2. In other cases it returns False.<br /><img src="/img/set_subset.png"  width="240" height="200"/>
<!--Code block -->
<figure class="highlight">
<pre><code class="language-python" data-lang="python">
set1 = {1, 2, 3}
set2 = {1, 2, 3, 5, 7, 9, 11, 13}
print(set1.issubset(set2))
print(set2.issubset(set1))
<br />
<b>Ouput:</b>
True
False
</code></pre>
</figure>
		</li>
		<li><b>set1.issuperset(set2)</b> - It returns true if all the elements of set2 present in set1. In other cases it returns False.<br /><img src="/img/set_superset.png"  width="240" height="200"/>
<!--Code block -->
<figure class="highlight">
<pre><code class="language-python" data-lang="python">
set1 = {1, 2, 3, 5, 7, 9, 11, 13}
set2 = {1, 2, 3}
print(set1.issuperset(set2))
print(set2.issuperset(set1))
<br />
<b>Ouput:</b>
True
False
</code></pre>
</figure>
		</li>
		<li><b>set1.symmetric_difference(set2)</b> - It returns a set containing all elements from both sets except the items which are present in both sets. It includes all elements by removing the intersection elements.<br /><img src="/img/set_symmetricdiff.png"  width="240" height="200"/>
<!--Code block -->
<figure class="highlight">
<pre><code class="language-python" data-lang="python">
set1 = {1, 2, 3, 5, 7, 9, 11, 13}
set2 = {1, 2, 3, 4, 5, 6, 7, 8}
print(set1.symmetric_difference(set2))
<br />
<b>Ouput:</b>
{4, 6, 8, 9, 11, 13}
</code></pre>
</figure>
		</li>
		<li><b>set1.union(set2)</b> - It returns a set containing all elements from both sets.It consider similar elements as a single element.<br /><img src="/img/set_union.png"  width="240" height="200"/> 
<!--Code block -->
<figure class="highlight">
<pre><code class="language-python" data-lang="python">
set1 = {1, 2, 3, 5, 7, 9, 11, 13}
set2 = {1, 2, 3, 4, 5, 6, 7, 8}
print(set1.union(set2))
<br />
<b>Ouput:</b>
{1, 2, 3, 4, 5, 6, 7, 8, 9, 11, 13}
</code></pre>
</figure>
		</li>

</ul>

<p>That's it for this lesson. I hope you all liked it. If you want to give any suggestion please feel free to let us know them through the comment section. Have a great day!</p>


  <ul class="pagination justify-content-center">
  <li class="page-item"><a class="page-link" href="/pages/lists_tuples6/">Previous</a></li>
  <li class="page-item "><a class="page-link" href="/projects/project1">0</a></li>
  <li class="page-item"><a class="page-link" href="/pages/introduction2/">1</a></li>
  <li class="page-item"><a class="page-link" href="/pages/variables/">2</a></li>
  <li class="page-item"><a class="page-link" href="/pages/numbers/">3</a></li>
  <li class="page-item"><a class="page-link" href="/pages/strings4">4</a></li>
  <li class="page-item"><a class="page-link" href="/pages/operators5/">5</a></li>
  <li class="page-item"><a class="page-link" href="/pages/lists_tuples6/">6</a></li>
  <li class="page-item active"><a class="page-link" href="/pages/sets7/">7</a></li>
  <li class="page-item"><a class="page-link" href="/pages/dictionaries8/">Next</a></li>
  </ul>
  
  
</div>





</div>
</div>
</div>
