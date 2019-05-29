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
	
<h3>Lists</h3>
<p>From all the coumpound data types lists are the most versatile data type that used to group the values together. A list is writing all the values by separating with commas and enclosed in square brackets. Lists are ordered means elements of list have indexes and they can be changeable. Lists allow dupicate members, it means we can have same values multiple times in a list.</p>

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

<h4>Built-in Functions</h4>
<ul>
	<li><b>len(list)</b> - It gives the total number of elements in a list.<br />
<!--Code block -->
<figure class="highlight">
<pre><code class="language-python" data-lang="python">
x = [1, 2, 3, 4, 5, 6, 7, 8, 9, 10]
print("Length of the list : ", len(x))
<br />
<b>Ouput:</b>
Length of the list : 10
</code></pre>
</figure>
	</li>
	<li><b>cmp(list1, list2)</b> - It compares all the elements of two lists. If all the elements of two lists are same it will 
		return 0. If all the elements of list1 are greater than list2 then it will return 1. In Else case it will return -1. 
		Number values can be easily checked but in strings each character will be checked so 'q' is greater than 'a'. Let's see 
		an example.<br />
<!--Code block -->
<figure class="highlight">
<pre><code class="language-python" data-lang="python">
list1 = [1, 2, "abc"]
list2 = [1, 2, "def"]
list3 = [1, 2, 3]
list4 = [1, 2, 3]
print("List2 is greater than list1: ", cmp(list1, list2))
print("List2 is greater than list1: ", cmp(list2, list1))
print("List3 and list4 have all elements same: ", cmp(list3, list4))
<br />
<b>Ouput:</b>
-1
1
0
</code></pre>
</figure>
	</li>
	<li><b>max(list)</b> - To use this all the elements of a list should be of same data-type(integers or strings or floats). From 
		all the elements of a list it will give the maximum element. IF all elements are strings it will give maximum element 
		based on alphabetical order.<br />
<!--Code block -->
<figure class="highlight">
<pre><code class="language-python" data-lang="python">
list1 = [1, 2, 3, 76, 7, 23, 97, 723, 232]
list2 = ['abcd', 'defg', 'hijk']
print("maximum of list1 : "max(list1))
print("maximum of list2 : "max(list2))
<br />
<b>Ouput:</b>
723
hijk
</code></pre>
</figure>
	</li>
	<li><b>min(list)</b> - It is similar to the max() function. It will give the minimum value from all the elemnts of the list and 
		all the elements should be of same datatype.<br />
<!--Code block -->
<figure class="highlight">
<pre><code class="language-python" data-lang="python">
list1 = [1, 2, 3, 76, 7, 23, 97, 723, 232]
list2 = ['abcd', 'defg', 'hijk']
print("minimum of list1 : "min(list1))
print("minimum of list2 : "min(list2))
<br />
<b>Ouput:</b>
1
abcd
</code></pre>
</figure>
	</li>
	<li><b>list(sequence)</b> - It converts any sequence or any datatype into a list. Let's see few examples.<br />
<!--Code block -->
<figure class="highlight">
<pre><code class="language-python" data-lang="python">
str = "This is a string"
print("converting a string into a list: ", list(str))
tuple1 = (1,2,3,4)
print("converting a tuple into a list: ", list(tuple1))
<br />
<b>Ouput:</b>
['t', 'h', 'i', 's', ' ', 'i', 's', ' ', 'a', ' ', 's', 't', 'r', 'i', 'n', 'g']
[1, 2, 3, 4]
</code></pre>
</figure>
	</li>
</ul>

<h4>Built-in methods</h4>
	<ul>
		<li><b>list.append(element)</b> - It will be used to append a new element at the end of the list. The new element can be a single object or asequence of objects but it can be treated as a single element after the append function applied.<br>
<!--Code block -->
<figure class="highlight">
<pre><code class="language-python" data-lang="python">
list1 = [1, 2, 3]
list1.append(4)
print("appending a single element: ", list1)
list1.append([5, 6, 7])
print("appending another list: ", list1)
<br />
<b>Ouput:</b>
appending a single element: [1, 2, 3, 4]
appending another list: [1, 2, 3, 4, 5, 6, 7]
</code></pre>
</figure>
		</li>
		<li><b>list.count(element)</b> - It will return the total number of time an element present in the list.<br>
<!--Code block -->
<figure class="highlight">
<pre><code class="language-python" data-lang="python">
list1 = [1, 2, 3, 5, 1, 3, 7, 1, 3, 4, 5, 6, 3]
print("Number of times 3 occur in the list: ", list1.count(3))
<br />
<b>Ouput:</b>
Number of times 3 occur in the list: 4
</code></pre>
</figure>
		</li>
		<li><b>list.extend(sequence)</b> - similar to the append() method but here if sequence is appended all the elements of the sequence will be appended as elements of the list and not as a single element.<br>
<!--Code block -->
<figure class="highlight">
<pre><code class="language-python" data-lang="python">
list1 = [1, 2, 3]
list2 = [4, 5, 6]
print("extending list1 with elements of list2: ", list1.extend(list2))
<br />
<b>Ouput:</b>
extending list1 with elements of list2: [1, 2, 3, 4, 5, 6]
</code></pre>
</figure>
		</li>
		<li><b>list.index(ele)</b> - It will return the first index of the element where it found.<br>
<!--Code block -->
<figure class="highlight">
<pre><code class="language-python" data-lang="python">
list1 = [1, 2, 3, 5, 1, 3, 7, 1, 3, 4, 5, 6, 3]
print("First occurence of element 3 is at index: ", list1.index(3))
<br />
<b>Ouput:</b>
First occurence of element 3 is at index: 2
</code></pre>
</figure>
		</li>
		<li><b>list.insert(index, ele)</b> - It inserts an element at a given index in the list.It just adds new element at given index and the previous elemnt will be shifted to next index number.<br>
<!--Code block -->
<figure class="highlight">
<pre><code class="language-python" data-lang="python">
list1 = [1, 2, 3, 5]
list1.insert(2, 4)
print("Inserting new element at index2: ", list1)
<br />
<b>Ouput:</b>
Inserting new element at index2:  [1, 2, 4, 3, 5]
</code></pre>
</figure>
		</li>
		<li><b>list.pop(index)</b> - It will return element at given index and delete permanently from the list. Index argument is optional. If no argument given then the last element of the list will be popped out.<br>
<!--Code block -->
<figure class="highlight">
<pre><code class="language-python" data-lang="python">
list1 = [1, 2, 3, 5]
print("Popping out element at index2: ", list1.pop(2))
<br />
<b>Ouput:</b>
Popping out element at index2: 3
</code></pre>
</figure>
		</li>
		<li><b>list.remove(ele)</b> - removes the element that is given from the list. If the given element not present in the list it will throw a value-error saying the element not found.<br>
<!--Code block -->
<figure class="highlight">
<pre><code class="language-python" data-lang="python">
list1 = [1, 2, 3, 5]
list1.remove(5)
print("removing element 5 from list: ", list1)
<br />
<b>Ouput:</b>
removing element 5 from list: [1, 2, 3]
</code></pre>
</figure>
		</li>
		<li><b>list.reverse()</b> - Reverse the positions of all the elements in the list. First element goes to last in new list.<br>
<!--Code block -->
<figure class="highlight">
<pre><code class="language-python" data-lang="python">
list1 = [1, 2, 3, 5]
list1.reverse()
print("reversing all the elements: ", list1)
<br />
<b>Ouput:</b>
[5, 3, 2, 1]
</code></pre>
</figure>
		</li>
		<li><b>list.sort()</b> - It does not return any value but it arranges all the elements of list in ascending order.<br>
<!--Code block -->
<figure class="highlight">
<pre><code class="language-python" data-lang="python">
list1 = [10, 4, 7, 2, 1, 90, 32]
list1.sort()
print("Sorting all the elements: ", list1)
<br />
<b>Ouput:</b>
[1, 2, 4, 7, 10, 32, 90]
</code></pre>
</figure>
		</li>
	</ul>

<h3>Tuples</h3>
<p>Tuples also sequence of values or elements just like lists but the elements of a tuple are immutable(can not be changeable). Elements of a tuple are comma-spearated values enclosed in parentheses. For tupes parentheses is just optional you can define a tuple directly writing comma-separated values without parentheses.</p>
<!--Code block -->
<p>Creating a tuple</p>
<figure class="highlight">
<pre><code class="language-python" data-lang="python">
tuple1 = (1, 2, 3)
tuple2 = 4, 5, 6
print(tuple1)
print(tuple2)<br />
<b>Ouput:</b>
(1, 2, 3)
(4, 5, 6)
</code></pre>
</figure>

<h4>Operations on tuples</h4>
<p>Unlike lists tuples are immutable and we can not change the data, but we can access the data. There are few operations that can apply on tuples. Let's see with examples</p>
<ul>
	<li><b>Accessing Values</b><br />
<!--Code block -->
<p>Creating a tuple</p>
<figure class="highlight">
<pre><code class="language-python" data-lang="python">
tuple1 = (1, 2, 3)
print(tuple1[0])
print(tuple1)<br />
<b>Ouput:</b>
1
(1, 2, 3)
</code></pre>
</figure>
	</li>
	<li><b>Updating tuples</b> -  We cannnot modify the elements but we can add element by concatenation.<br /> 
<!--Code block -->
<p>Creating a tuple</p>
<figure class="highlight">
<pre><code class="language-python" data-lang="python">
tuple1 = (1, 2, 3)
tuple2 = 4, 5, 6
print("Concatenating tuple1 and tuple2 : ",tuple1+tuple2)<br />
<b>Ouput:</b>
Concatenating tuple1 and tuple2 : (1, 2, 3, 4, 5, 6)
</code></pre>
</figure>
	</li>
	<li><b>Deleting tuples</b> - Individual elements cannot be deleted due to the immutable nature of the tuple. But instead we can delete the complete tuple using del statement. After deleting we cannot access the tuple.<br />
<!--Code block -->
<p>Creating a tuple</p>
<figure class="highlight">
<pre><code class="language-python" data-lang="python">
tuple1 = (1, 2, 3)
del tuple1
print(tuple1)<br />
<b>Ouput:</b>
NameError: name 'tup' is not defined
</code></pre>
</figure>
	</li>
	<li><b>len(tuple)</b><br />
<!--Code block -->
<p>Creating a tuple</p>
<figure class="highlight">
<pre><code class="language-python" data-lang="python">
tuple1 = (1, 2, 3)
print(len(tuple1))<br />
<b>Ouput:</b>
3
</code></pre>
</figure>
	</li>
	<li><b>Repetition</b><br />
<!--Code block -->
<p>Creating a tuple</p>
<figure class="highlight">
<pre><code class="language-python" data-lang="python">
print("Repeting an element four times: ", ('hello')*4)<br />
<b>Ouput:</b>
Repeting an element four times: ('hello', 'hello', 'hello', 'hello')
</code></pre>
</figure>
	</li>
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








