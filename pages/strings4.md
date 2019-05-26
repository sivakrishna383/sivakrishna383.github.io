---
layout: default
title: Strings
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
		<a href="/pages/introduction2/"><li class="list-group-item active">Introduction</li></a>
		<a href="/pages/variables/"><li class="list-group-item">Variables</li></a>
		<a href="/pages/numbers/"><li class="list-group-item">Numbers</li></a>
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
<h3>Strings</h3>
<p>Strings are sequence of characters which are enclosed in single quotes ('<code><span>...</span></code>') or double quotes ("<code><span>...</span></code>"). We can use either of them as both will give the same result. We can create a python string directly by assigning a string value to a variable.Let's see an example.....</p>

<!--Code block -->
<figure class="highlight">
<pre><code class="language-python" data-lang="python">
 <span class="n">x</span> <span class="o">=</span> <span class="mi">"Hello This is a string"</span> <span class="c">#We are here assigning string to variable x.</span>
<span class="k">print</span><span class="p">(</span><span class="n">x</span><span class="p">)</span><br />
<b>Output:</b>
Hello This is a string
</code></pre>
</figure>

<p>In other programming languages there is a special data-type for characters but in python a charcter is a string of length one. </p>
<p>Okay! That's fine but how can we write a statement like <b>"yes, this is a quotation",He said</b>. Mmmm!!! That's a tricky one. But python has a solution for it. Let's see......</p>

<!--Code block -->
<figure class="highlight">
<pre><code class="language-python" data-lang="python">
 <span class="n">x</span> <span class="o">=</span> <span class="mi">"\"yes, this is a quotation\",He said"</span>
<span class="k">print</span><span class="p">(</span><span class="n">x</span><span class="p">)</span><br />
<b>Output:</b>
"yes, this is a quotation",He said
</code></pre>
</figure>

<p>In order to print a quotation mark inside a quotation we have used a back-slash(\). So if we use a back-slash python will consider it as a character in the string. So it will print with the other characters. If you want to use single quotes and double quotes in a single string, it is easy by using the back-slash technique. Let's see a little complicated example.</p>

<!--Code block -->
<figure class="highlight">
<pre><code class="language-python" data-lang="python">
 <span class="n">x</span> <span class="o">=</span> <span class="mi">"\"I don\'t want to continue the conversation\", He said"</span>
<span class="k">print</span><span class="p">(</span><span class="n">x</span><span class="p">)</span><br />
<b>Output:</b>
"I don't want to continue the conversation",He said
</code></pre>
</figure>

<h4>Accesing a substring</h4>
<p>In Strings all the characters in sequence start with index zero. So the first character in a string will have index 0, 
second character will have index 1 and so on. Let's take an example string <b>x = "Hello!"</b>, If you want to access the 
first "l" character from the string it is located at third character which is index 2. So you simple state x[2]
that will give the character "l". If you want to access a sequence of characters(a substring) from a string, 
You have to use a slice operator([start_index:end_index]) where start_index is the index of the starting character of the 
substring and end_index is the index+1 of the last character of the substring as the end_index excluded in python. Let's see an example.</p>

<!--Code block -->
<figure class="highlight">
<pre><code class="language-python" data-lang="python">
 <span class="n">x</span> <span class="o">=</span> <span class="mi">"Hey, This is a complete string!"</span>
<span class="k">print</span><span class="p">(</span><span class="n">x[15:23]</span><span class="p">)</span><br />
<span class="k">print</span><span class="p">(</span><span class="n">x[:15]</span><span class="p">)</span><span class="c">#leaving starting index empty means selecting from index zero</span><br />
<span class="k">print</span><span class="p">(</span><span class="n">x[15:]</span><span class="p">)</span><span class="c">#leaving end_index empty means selecting upto the last character</span><br /> 
<b>Output:</b>
complete
Hey, This is a 
complete string!
</code></pre>
</figure>

<p>We are selecting a substring <b>complete</b> so we have assigned the starting index as 15 and end index as 
23 which exlude and upto index 22 will be selected. In second case we left start_index empty that means select from the beginning
(index zero). In third case we left end_index empty that means select upto the last character</p>

<h4>What are negative indices?</h4>
<p>In python negative indices means selection in reverse order. So the last character in a string will have index -1, the second 
last character will have index -2 and so on.Let's see an example</p>

<!--Code block -->
<figure class="highlight">
<pre><code class="language-python" data-lang="python">
 <span class="n">x</span> <span class="o">=</span> <span class="mi">"Hey, This is a complete string!"</span>
<span class="k">print</span><span class="p">(</span><span class="n">x[-1]</span><span class="p">)</span><br />
<span class="k">print</span><span class="p">(</span><span class="n">x[-7:-1]</span><span class="p">)</span><br />
<span class="k">print</span><span class="p">(</span><span class="n">x[-7:]</span><span class="p">)</span><br />
<b>Output:</b>
!
string
string!
</code></pre>
</figure>
<p>we selected the last character using x[-1]. If we use slice operator x[-7:-1] it selected a substring from index -7 
upto the last character. In order to select tha last character also we left the end_index empty.</p>

<h4>Some Built-in operations on strings!</h4>
<ul>
  <li><b>str.Capitalize()</b> - <br />str.capitalize() is a default function which capitalizes the first character of the string and the 
    rest of the characters will be lower cased.<br /> <b>Ex:</b> 
    <figure class="highlight">
    <pre><code class="language-python" data-lang="python">
    str  = "siVAKrisHna"
    print(str.capitalize())<br />
    <b>Output:</b>
    Sivakrishna
    </code></pre> 
    </figure>
  </li>
  <li><b>str.Count(sub,start,end)</b> - <br />It will count the number of occurences of the substring sub in the string str in range of [start,end].
    Here start and end are optional, if you want to search in whole string don't give start,end.
    <figure class="highlight">
    <pre><code class="language-python" data-lang="python">
    str  = "Hello! welcome to the tutorial on strings!"
    sub1 = "tutorial"
    sub2 = "t"
    print(str.Count(sub1))
    print(str.Count(sub2,19,30))<br />
    <b>Output:</b>
    1
    3
    </code></pre> 
    </figure>
    There are one instance of sub1 and three instances of sub2 in range of [19,30].
  </li>
  <li><b>str.endswith(suffix,start,end)</b> - <br /> It returns True or False, Depending on the string ends with the given suffix or not. 
    If you provide start,end indexes also it will search in that range of substring only.
    <figure class="highlight">
    <pre><code class="language-python" data-lang="python">
    str  = "Hello! welcome to the tutorial on strings!"
    sub1 = "strings!"
    sub2 = "to"
    print(str.endswith(sub1))
    print(str.endswith(sub2,5,27))
    print(str.endswith(sub2,2,26))<br />
    <b>Output:</b>
    True
    True
    False
    </code></pre> 
    </figure>
  </li>
  <li><b>str.find(sub, start, end)</b> - <br /> It returns the starting index of the substring sub if it found in the whole string str 
    or in the substring of str in range [start,end].If nothing found it will return -1.
    <figure class="highlight">
    <pre><code class="language-python" data-lang="python">
    str  = "Hello! welcome to the tutorial on strings!"
    sub1 = "tutorial"
    sub2 = "notdound"
    print(str.find(sub1))
    print(str.find(sub2))<br />
    <b>Output:</b>
    23
    -1
    </code></pre> 
    </figure>
  </li>
  <li><b>str.format(*args)</b> - <br />The string on which this method is called, may include literal text or substitution fields, which
    are delimited by braces. Each replacement field contains either the numerical index of positional logic, or the name of the keyword 
    logic. Returns a copy of the string where each substitution field is replaced with the string value of the same argument.<br />
    <figure class="highlight">
    <pre><code class="language-python" data-lang="python">
    print("The sum of 1 + 2 is {0} and 2+4 is {1}".format(1+2, 2+4))<br />
    <b>Output:</b>
    The sum of 1 + 2 is 3 and 2+4 is 6
    </code></pre> 
    </figure>
    </li>
  <li><b>str.index(sub,start,end)</b> - <br />It is similar to the str.find() function. It returns the starting index of the substring sub if it was found in the string str
    else unlike find() function it will throw a value error saying substring not found.
    <figure class="highlight">
    <pre><code class="language-python" data-lang="python">
    str  = "Hello! welcome to the tutorial on strings!"
    sub1 = "tutorial"
    sub2 = "notfound"
    print(str.index(sub1))
    print(str.index(sub2))<br />
    <b>Output:</b>
    23
    ValueError: substring not found
    </code></pre> 
    </figure>
  </li>
  <li><b>str.islower()</b> - <br /> It returns True if all the characters of the string str are in lower case else it returns False.
    <figure class="highlight">
    <pre><code class="language-python" data-lang="python">
    str1  = "all characters are lower case"
    str2 = "Some characters Uppercase"
    print(str1.islower())
    print(str2.islower())<br />
    <b>Output:</b>
    True
    False
    </code></pre> 
    </figure>
  </li>
  <li><b>str.join(<i>iterable</i>)</b> - <br /> Returns a concatenated string which is a result of the concatenation of the str and <i>iterable</i>. It will throw an error if
    the <i>iterable</i> is not a string.
    <figure class="highlight">
    <pre><code class="language-python" data-lang="python">
    str1  = "all characters are lower case"
    str2 = " Some characters Uppercase"
    print(str1.join(str2))<br />
    <b>Output:</b>
    all characters are lower case Some characters Uppercase
    </code></pre> 
    </figure>
  </li>
  <li><b>str.replace(old, new, count)</b> - <br /> It will return a string by replacing the old substring with the new substring. Count is optional. If count is not given it means replacing the all instances of old substring with new substring. If count is given replace the old instance atmost count number of times.
    <figure class="highlight">
    <pre><code class="language-python" data-lang="python">
    str1  = "This is an exaple of replace function"
    old = "is"
    new = "isn't"
    print(str1.replace(old,new))
    print(str1.replace(old,new,1))<br />
    <b>Output:</b>
    Thisn't isn't an example of replace function
    Thisn't is an example of replace function
    </code></pre> 
    </figure>
  </li>
  <li><b>str.split(sep=None, maxsplit=-1)</b> - <br /> It will return list of words or substrings by splitting at sep as delimiter string. If maxsplit is given it will split atmost maxsplit times and there will be atmost maxsplit+1 words or substrings in the returned list of words.
    If maxsplit is not given it will take default value -1 and makes all possible splits. If Sep is not given it will split using space character as delimiter.
    <figure class="highlight">
    <pre><code class="language-python" data-lang="python">
    str1  = "This is an example of split function"
    print(str1.split())
    print(str1.split(maxsplit=2)<br />
    <b>Output:</b>
    ['This', 'is', 'an', 'example', 'of', 'split', 'function']
    ['This', 'is', 'an example of split function']
    </code></pre> 
    </figure>
  </li>
</ul>

<p></p>

  <ul class="pagination justify-content-center">
  <li class="page-item"><a class="page-link" href="/projects/project1">Previous</a></li>
  <li class="page-item "><a class="page-link" href="/projects/project1">0</a></li>
  <li class="page-item active"><a class="page-link" href="/pages/introduction2/">1</a></li>
  <li class="page-item"><a class="page-link" href="/pages/variables/">2</a></li>
  <li class="page-item"><a class="page-link" href="/pages/numbers/">3</a></li>
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









