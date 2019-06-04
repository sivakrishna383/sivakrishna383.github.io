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
		<a href="/pages/loops9/"><li class="list-group-item">Loops</li></a>
		<ul>
			<a href="/pages/loops9/#ifelse"><li class="list-group-item">If...Else</li></a>
			<a href="/pages/loops9/#while"><li class="list-group-item">While</li></a>
			<a href="/pages/loops9/#for"><li class="list-group-item">For</li></a>
		</ul>
		<a href="/pages/functions10/"><li class="list-group-item active">Functions</li></a>
		<a href="#"><li class="list-group-item">Arrays</li></a>
	</ol>
</div>

<div class="article">

<h3>Functions</h3>
<p>A function is a block  of code with single or multiple statements in it that can be executed
whenever you call it by it's name. You can pass data to a function which are called arguments or parameters
for the function. A function can be written in a way to return data as a result.</p>

<h4>Basic syntax of function</h4>
<p>There are some rules to write a function in python.</p>
<ul>
<li>A function block must begin with <b>def</b> keyword followed by function name and parentheses(()) and a colon(:).</li>
<li>Input arguments to a function should be given in parentheses.</li>
<li>A docstring is there as the first statement of the function which is optinal.</li>
<li>All the statements inside a function must have same indentation.</li>
<li>In the end of the function a <b>return</b> statement will be there with the 
data that needs to returns to the caller of the function. It is optional if you don't want to return any data.</li>
</ul>

<!--Code block -->
<p><b>Syntax</b></p>
<figure class="highlight">
<pre><code class="language-python" data-lang="python">
def func_name(arguments):
    """ function docstring """
    statements
    return data
</code></pre>
</figure>

<p><b>Example of a function</b></p>
<!--Code block -->
<figure class="highlight">
<pre><code class="language-python" data-lang="python">
def printhello():
    print("Hello world! This is a function with zero input arguments")

printhello()
<br />
<b>Ouput:</b>
Hello world! This is a function with zero input arguments
</code></pre>
</figure>

<h4>Passing input arguments</h4>
<p>Unlike other programming languages in python input arguments will be passed into a function
by pass by reference only. It means if you change or update the input parameter inside the function 
it will update outside of the function where the calling function presents. Let's see with an example.</p>
<!--Code block -->
<figure class="highlight">
<pre><code class="language-python" data-lang="python">
def arguments(list1):
    list1.append(4)
    print("list changed values inside the function: ", list1)

list2 = [1, 2, 3]
arguments(list2)
print("list values outside the function: ", list2)
<br />
<b>Ouput:</b>
list changed values inside the function: [1, 2, 3, 4]
list values outside the function: [1, 2, 3, 4]
</code></pre>
</figure>
<p>In the above function we passed a list to the function. The variable names are different but both
reference to the same list memory. So if we update the list in the function it will also
update the list variable outside the function.</p>
<p>Let's see an example where the values will update in the function but not update outside the function. We can achieve
by initializing the variable again inside the function.</p>
<!--Code block -->
<figure class="highlight">
<pre><code class="language-python" data-lang="python">
def arguments(list1):
    list1 = [1, 2, 3]
    list1.append(4)
    print("list changed values inside the function: ", list1)

list1 = [1, 2, 3]
arguments(list1)
print("list values outside the function: ", list1)
<br />
<b>Ouput:</b>
list changed values inside the function:  [1, 2, 3, 4]           
list values outside the function:  [1, 2, 3]
</code></pre>
</figure>

<h4>Examples of passing arguments</h4>
<ul>
<li> Passing the arguments in the same order - <br />
<!--Code block -->
<figure class="highlight">
<pre><code class="language-python" data-lang="python">
def printname(first_name, last_name):
    print("Welcome", first_name, last_name)

printname("Robert","Downy")
<br />
<b>Ouput:</b>
Welcome Robert Downy
</code></pre>
</figure>
</li>

<li>Passing arguments by defining when calling the function. <br /> 
<!--Code block -->
<figure class="highlight">
<pre><code class="language-python" data-lang="python">
def printname(first_name, last_name, age):
    print("Welcome", first_name, last_name, "Your age is", age)

printname(first_name = "Robert", age = 50, last_name = "Downy")
<br />
<b>Ouput:</b>
Welcome Robert Downy Your age is 50  
</code></pre>
</figure>
</li>
<li>Some arguments can be defined when defining the function <br />
<!--Code block -->
<figure class="highlight">
<pre><code class="language-python" data-lang="python">
def printname(first_name, last_name, age=40):
    print("Welcome", first_name, last_name, "Your age is", age)

printname(first_name = "Robert", age = 50, last_name = "Downy")
printname(first_name = "Robert", last_name = "Downy jr")
<br />
<b>Ouput:</b>
Welcome Robert Downy Your age is 50                              
Welcome Robert Downy jr Your age is 40
</code></pre>
</figure>
</li>
</ul>
<h4>Variable-length arguments</h4>
<p>In some cases you need to send different number of arguments to a function each 
time a function called. In that case we will use variable-length arguments. There will
be a single keyword defined inside the function definition for all the variables you want to pass.These variable length arguments will be taken inside
a variable with asterisk(*) before it's name. If there are keyword arguments also then this
arguments should be placed at the end.Let's see it in an example.</p>
<!--Code block -->
<figure class="highlight">
<pre><code class="language-python" data-lang="python">
def squares(*numbers):
    square = [i**2 for i in numbers]
    print(square)
squares(1, 2, 3, 4, 5)
squares(1, 2, 3, 4, 5, 6, 7, 8)
<br />
<b>Ouput:</b>
[1, 4, 9, 16, 25]                                                
[1, 4, 9, 16, 25, 36, 49, 64]
</code></pre>
</figure>

<!--Code block -->
<figure class="highlight">
<pre><code class="language-python" data-lang="python">
def addnums(start, *numbers):
    for i in numbers:
        start = start+i
    print("sum of all the numbers",start)
addnums(10, 20, 30, 40, 50)
addnums(10, 20, 30, 40, 50, 60, 70, 80)
<br />
<b>Ouput:</b>
sum of all the numbers 150
sum of all the numbers 360
</code></pre>
</figure>

<h4>Lambda Functions</h4>
<p>Unlike normal functions lambda function take multiple input arguments but give a single 
output value in the form of an expression. It doesnot contain multiple statements.Let's see an example</p>
<!--Code block -->
<figure class="highlight">
<pre><code class="language-python" data-lang="python">
mult = lambda a,b : a * b;

print("multiplication of 17 and 15:", mult(17, 15))
print("multiplication of 12 and 15:", mult(12, 15))
<br />
<b>Ouput:</b>
multiplication of 17 and 15: 255
multiplication of 12 and 15: 180
</code></pre>
</figure>

<h4>Return statement</h4>
<p>In python we can return a single variable it can be any datatype.</p>
<!--Code block -->
<figure class="highlight">
<pre><code class="language-python" data-lang="python">
def squares(list1):
    square = [i**2 for i in list1]
    return square
print("squares of elements of the list:[1, 2, 3, 4]  are ", squares([1, 2, 3, 4]))
print("squares of elements of the list:[1, 2, 3, 4, 5, 6]  are ", squares([1, 2, 3, 4, 5, 6]))
<br />
<b>Ouput:</b>
squares of elements of the list:[1, 2, 3, 4]  are  [1, 4, 9, 16]  
squares of elements of the list:[1, 2, 3, 4, 5, 6]  are  [1, 4, 9, 16, 25, 36] 
</code></pre>
</figure>

<h4>Scope of variables</h4>
<p>Two types of variables are there in any programming language. <b>1) Local Variables 2) Global variables</b>.</p>
<p><b>1) Local variables:</b> Variables that are defined inside a function are called local variables
and those type of variables cannot be accessed outside the function.</p>
<p><b>1) Global variables:</b> Variables that are defined outside the function are called global variables
and those type of variables can be accessed anywhere in the program.</p>
<!--Code block -->
<figure class="highlight">
<pre><code class="language-python" data-lang="python">
square = 1
def squares(list1):
    square = [i**2 for i in list1]
    print("Local variable square value : ", square)
print("Global variable square value: ", square)
<br />
<b>Ouput:</b>
Local variable square value :  [1, 4, 9, 16]                            
Global variable square value:  1
</code></pre>
</figure>

<h4>Recursion</h4>
<p>Python accepts the recursion nature of the function. Recursion means a function calls itself
Let's see an example</p>

<!--Code block -->
<figure class="highlight">
<pre><code class="language-python" data-lang="python">
def factorial(n):
    if(n>1):
      return n * factorial(n-1)
    else:
      return 1
print("Factorial of 5 using recursion: ", factorial(5))
print("Factorial of 6 using recursion: ", factorial(6))
print("Factorial of 7 using recursion: ", factorial(7))
print("Factorial of 8 using recursion: ", factorial(8))
print("Factorial of 9 using recursion: ", factorial(9))
<br />
<b>Ouput:</b>F
Factorial of 5 using recursion:  120                             
Factorial of 6 using recursion:  720                             
Factorial of 7 using recursion:  5040                            
Factorial of 8 using recursion:  40320                           
Factorial of 9 using recursion:  362880
</code></pre>
</figure>

<p>That's it for this lesson. I hope you all liked it. If you want to give any suggestion please feel free to let us know them through the comment section. Have a great day!</p>


  <ul class="pagination justify-content-center">
  <li class="page-item"><a class="page-link" href="/pages/loops9/">Previous</a></li>
  <li class="page-item"><a class="page-link" href="/pages/lists_tuples6/">6</a></li>
  <li class="page-item"><a class="page-link" href="/pages/sets7/">7</a></li>
  <li class="page-item"><a class="page-link" href="/pages/dictionaries8/">8</a></li>
  <li class="page-item"><a class="page-link" href="/pages/loops9/">9</a></li>
  <li class="page-item active"><a class="page-link" href="/pages/functions10/">10</a></li>
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
