---
layout: default
title: Loops
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
		<a href="/pages/dictionaries8/"><li class="list-group-item">Dictionaries</li></a>
		<a href="/pages/loops9/"><li class="list-group-item  active">Loops</li></a>
		<ul>
			<a href="/pages/loops9/#ifelse"><li class="list-group-item  active">If...Else</li></a>
			<a href="/pages/loops9/#while"><li class="list-group-item  active">While</li></a>
			<a href="/pages/loops9/#for"><li class="list-group-item  active">For</li></a>
		</ul>
		<a href="#"><li class="list-group-item">Functions</li></a>
		<a href="#"><li class="list-group-item">Arrays</li></a>
	</ol>
</div>

<div class="article">

<h3>Loops</h3>
<p>In writing a large nuber of lines of code, at some point we may need to write aparticular block of code
several times to satisfy a special condition. Almost all the programming languages supports control structures which supports 
writing single blocks multiple times until a specific condition satisfied. Let's see some conditions that
python supports to use in loop coditions.
<ul>
<li>Equals x == y</li>
<li>Not equals x != y</li>
<li>Less than x < y</li>
<li>Greater than x > y</li>
<li>Less than or equal to x <= y</li>
<li>Greater than or equal to x >= y</li>
</ul>
</p>

<p>Python supports three types of loop strctures to make the coding simple.
<ul>
<li>If..Else loops</li>
<li>For loops</li>
<li>While loops</li>
</ul>
</p>

<h3 id="ifelse">1) If....Else loops</h3>
<h4>i) If loops</h4>
<!--Code block -->
<p>Example syntax of IF statement. As we have dicussed in previous sections to write a block of code indentation should be there.
If you fail to write the indentation it will throw an indentation error.</p>
<figure class="highlight">
<pre><code class="language-python" data-lang="python">
x = 10
y = 20
if x < y:
  print("x is less than y")
<br />
<b>Ouput:</b>
x is less than y
</code></pre>
</figure>
<p>In the above code we have used a <i>less than</i> condition to check whether value of x is less than y or not.
As x=10 and y=20, x is less than y the condition will be true and it will go into the loop and executes the print() statement.</p>

<h4>ii) If..else</h4>
<p>Python will execute the statements inside an if block if the condition is true. If the condition is false we want to execute some statements. So we write those statements inside an Else block.</p>
<!--Code block -->
<figure class="highlight">
<pre><code class="language-python" data-lang="python">
x = 20
y = 10
if x < y:
  print("x is less than y")
else:
  print("x is not less than y")
<br />
<b>Ouput:</b>
x is not less than y
</code></pre>
</figure>

<h4>iii) Nested loop (If...elif...else)</h4>
<p>If there are three or more possibilities for a condition we will write some statements when each possibility of the condition is true. 
We write first possibility in if block last possibility in else block and the remaining possibilities in an elif block. Lets see an example.</p>

<!--Code block -->
<figure class="highlight">
<pre><code class="language-python" data-lang="python">
x = 10
y = 10
if x < y:
  print("x is less than y")
elif x > y:
  print("x is greater than than y")
else:
  print("x is equal to y")
<br />
<b>Ouput:</b>
x is equal to y
</code></pre>
</figure>

<h4>One line blocks</h4>
<!--Code block -->
<figure class="highlight">
<pre><code class="language-python" data-lang="python">
x = 20
y = 10
print("x is greater than y") if x > y else print("x is not greater than y")
<br />
<b>Ouput:</b>
x is greater than y
</code></pre>
</figure>

<!--Code block -->
<figure class="highlight">
<pre><code class="language-python" data-lang="python">
x = 20
y = 10
print("x is greater than y") if x > y else print("x is equal to y") if x == y else print("x is greater than y")
 <br />
<b>Ouput:</b>
x is greater than y
</code></pre>
</figure>

<h4>Multiple conditions</h4>
<h4>1) And</h4>
<!--Code block -->
<p>The combined condition to be true both conditions must be true.</p>
<figure class="highlight">
<pre><code class="language-python" data-lang="python">
x = 20
y = 10
z = 5
if x > y and x > z:
  print("X is the largest number")
<br />
<b>Ouput:</b>
X is the largest number
</code></pre>
</figure>

<h4>2) Or</h4>
<!--Code block -->
<p>The combined condition to be true atleast one of the two conditions ust be true</p>
<figure class="highlight">
<pre><code class="language-python" data-lang="python">
x = 20
y = 10
z = 25
if x > y or x > z:
  print("X is the larger than atleast one number")
<br />
<b>Ouput:</b>
X is the larger than atleast one number
</code></pre>
</figure>

<h3 id="for">For loops</h3>
<!--Code block -->
<p><b>Basic syntax of the for loop</b></p>
<figure class="highlight">
<pre><code class="language-python" data-lang="python">
for variable in sequence:
  statements
<br /></code></pre>
</figure>

<p>For each iteration(step) the one item from the list will be assigned to the variable and then statements in the for block will be 
	executed. When all the elements are over the loop will break.</p>

<!--Code block -->
<figure class="highlight">
<pre><code class="language-python" data-lang="python">
list1 = [1, 2, 3, 4, 5]
for x in list1:
  print(x)
<br />
<b>Ouput:</b>
1
2
3
4
5
</code></pre>
</figure>
<p>One more way to represent the same loop.</p>
<!--Code block -->
<figure class="highlight">
<pre><code class="language-python" data-lang="python">
list1 = [1, 2, 3, 4, 5]
for x in range(len(list1)):
  print(list1[x])
<br />
<b>Ouput:</b>
1
2
3
4
5
</code></pre>
</figure>

<p><b>For loop through a string</b></p>
<!--Code block -->
<figure class="highlight">
<pre><code class="language-python" data-lang="python">
str = "This is a string"
for x in str:
  print(x)
<br />
<b>Ouput:</b>
T
h
i
s

i
s

a

s
t
r
i
n
g
</code></pre>
</figure>
<h4>Break  statement</h4>
<p>If we want to stop a loop after meeting a certain condition before all iterations end, we can use a break statement where we want to end a loop.</p>
<!--Code block -->
<figure class="highlight">
<pre><code class="language-python" data-lang="python">
list1 = [1, 2, 3, 4, 5]
for x in list1:
  if x == 4:
    break
  print(x)
<br />
<b>Ouput:</b>
1
2
3
</code></pre>
</figure>
<h4>Continue  statement</h4>
<p>If we want to skip the execution of statements in the loop block after meeting a certain condition before all iterations end, we can use a continue statement where we want to skip a loop.</p>
<!--Code block -->
<figure class="highlight">
<pre><code class="language-python" data-lang="python">
list1 = [1, 2, 3, 4, 5, 6]
for x in list1:
  if x == 4:
    cotinue
  print(x)
<br />
<b>Ouput:</b>
1
2
3
5
6
</code></pre>
</figure>

<h4>Pass  statement</h4>
<p>It works similar to continue statement, but unlike continue statement it will execute a null iteration and executes nothing. Let's see an example.</p>
<!--Code block -->
<figure class="highlight">
<pre><code class="language-python" data-lang="python">
list1 = [1, 2, 3, 4, 5]
for x in list1:
  if x == 4:
    pass
    print("pass statement")
  print(x)
<br />
<b>Ouput:</b>
1
2
3
pass statement
4
5
</code></pre>
</figure>


<h3 id="while">While loop</h3>
<p>While loop executes a block of statements as long as the given condition is true.</p>
<!--Code block -->
<figure class="highlight">
<pre><code class="language-python" data-lang="python">
while condition:
  statements
</code></pre>
</figure>


<p>An example of a while loop</p>
<!--Code block -->
<figure class="highlight">
<pre><code class="language-python" data-lang="python">
i = 0
while i < 10:
  print(i)
  i = i+1
<br />
<b>Ouput:</b>
0
1
2
3
4
5
6
7
8
9
</code></pre>
</figure>
<p>In while loops there is a chance that the loop may go to infinite loop if the condition always true. In that case you have to stop the output py pressing CTRL+C.</p>
<!--Code block -->
<figure class="highlight">
<pre><code class="language-python" data-lang="python">
i = 1
while i:
  print(i)
  i = i+1
<br />
<b>Ouput:</b>
0
1
2
3
4
5
6
7
8
9
Traceback (most recent call last):
KeyboardInterrupt
</code></pre>
</figure>


<p>That's it for this lesson. I hope you all liked it. If you want to give any suggestion please feel free to let us know them through the comment section. Have a great day!</p>


  <ul class="pagination justify-content-center">
  <li class="page-item"><a class="page-link" href="/pages/dictionaries8/">Previous</a></li>
  <li class="page-item"><a class="page-link" href="/pages/lists_tuples6/">6</a></li>
  <li class="page-item"><a class="page-link" href="/pages/sets7/">7</a></li>
  <li class="page-item"><a class="page-link" href="/pages/dictionaries8/">8</a></li>
  <li class="page-item active"><a class="page-link" href="/pages/loops9/">9</a></li>
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
