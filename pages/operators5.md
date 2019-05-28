---
layout: default
title: Operators
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
  <h3>Operators</h3>
  <p>Operators in python are special symbols that carryout operations between variables or values. For example 1+2=3 here 1,2 are operands and + is the operator symbol for addition. Python hass divided operators into different groups.</p>
	<ul>
		<li>Arithmetic operators</li>
		<li>Assignment operators</li>
		<li>Comparison operators</li>
		<li>Logical operators</li>
		<li>Identity operators</li>
		<li>Membership operators</li>
		<li>Bitwise operators</li>
	</ul>
  <h4>Arithmetic operators</h4>
	<ul>
		<li><b>Addition (+)</b> - Adds two operands on both sides of the operator.<br /> 	
<!--Code block -->
<figure class="highlight">
<pre><code class="language-python" data-lang="python">
a = 5
b = 2
print(a+b)<br />
<b>Ouput:</b>
7
</code></pre>
</figure>
		</li>
		<li><b>Subtraction (-)</b>subtract two operands on both sides of the operator. <br />
<!--Code block -->
<figure class="highlight">
<pre><code class="language-python" data-lang="python">
a = 5
b = 2
print(a-b)<br />
<b>Ouput:</b>
3
</code></pre>
</figure>
		</li>
		<li><b>Multiplication (*)</b> - multiplies two operands on both sides of the operator.
<!--Code block -->
<figure class="highlight">
<pre><code class="language-python" data-lang="python">
a = 5
b = 2
print(a*b)<br />
<b>Ouput:</b>
10
</code></pre>
</figure>
		</li>
		<li><b>Division (/)</b> - Divides the left hand variable with right hand variable of the operator.
<!--Code block -->
<figure class="highlight">
<pre><code class="language-python" data-lang="python">
a = 6
b = 2
print(a/b)<br />
<b>Ouput:</b>
3
</code></pre>
</figure>
<!--Code block -->
<figure class="highlight">
<pre><code class="language-python" data-lang="python">
a = 5
b = 2
print(a/b) <span clas="c">#It will return the integer values only. Example we get 2.5 but it return only 2.</span><br />
<b>Ouput:</b>
2
</code></pre>
</figure>
		</li>
		<li><b>Moudlus (%)</b> - It returns the remainder by dividing the left side operand with right side operand of the 			operator. The quotient should be an integer value and not a float.
<!--Code block -->
<figure class="highlight">
<pre><code class="language-python" data-lang="python">
a = 5
b = 2
print(a/b)<br />
<b>Ouput:</b>
1
</code></pre>
</figure>
		</li>
		<li><b>Exponent (**)</b> - It will return a value that is left hand variable to the power of right hand variable.
<!--Code block -->
<figure class="highlight">
<pre><code class="language-python" data-lang="python">
a = 5
b = 2
print(a**b)<br />
<b>Ouput:</b>
25
</code></pre>
</figure>
		</li>
		<li><b>Floor division (//)</b> - it first do the division of operands and if the quotient is positive the decimal point 		will be removed. If quotient is negative the result will rounded to the negative infinity.
<!--Code block -->
<figure class="highlight">
<pre><code class="language-python" data-lang="python">
a = 5
b = 2
print(5//2)
print(5.0//2.0)
print(-5 // 2)<br />
<b>Ouput:</b>
2
2.0
-3
</code></pre>
</figure>
		</li>
	</ul>
<h4> Assignment operators</h4>
	<ul>
		<li><b> = </b>  <br> It assigns the right hand side value to the left hand variable. <b>Ex:</b> a = 2+3, b = 1+2.</li>
		<li><b> += </b>  <br> It will assign a value to the left hand side variable by adding left hand variable to the right 
			hand value. <b>Ex:</b> a += 5 is similar to a = a+5.</li>
		<li><b> -= </b> <br> It will assign a value to the left hand side variable by subtracting right hand value  from left 
			hand value or variable. <b>Ex:</b> a -= 5 is similar to a = a-5.</li>
		<li><b> *= </b> <br> Similar to above operator by replacing subtraction with multiplication. <b>Ex:</b> a *= 5 similar 
			to a = a*5.</li>
		<li><b> /= </b> <br> Similar to above operator by replacing the multiplication with division. <b>Ex:</b> a /= 5 => a = 
			a/5.</li>
		<li><b> %= </b> <br> Similar to above operator by replacing division with modulus operation.<b>Ex:</b> a %= 5 similar to a = 
			a%5.</li>
		<li><b> **= </b> <br> Similar to above operator by replacing modulus with Exponential operation.<b>Ex:</b> a **= 5 similar to 
			a = a**5.</li>
		<li><b> //= </b> <br> Similar to above operator by replacing Exponential with floor division operation.<b>Ex:</b> a //= 5 
			similar to a = a//5.</li>
</ul>
<p>Examples of assignment operators</p>
<!--Code block -->
<figure class="highlight">
<pre><code class="language-python" data-lang="python">
a,b = 5,2
a += b
print(a)

a,b = 5,2
a -= b
print(a)

a,b = 5,2
a *= b
print(a)

a,b = 5,2
a /= b
print(a)

a,b = 5,2
a %= b
print(a)

a,b = 5,2
a **= b
print(a)

a,b = 5,2
a //= b
print(a)
<br />
<b>Ouput:</b>
7
3
10
2
1
25
2
</code></pre>
</figure>

<h4>Comparison Operators</h4>
	<ul>
		<li><b> == </b> <br> If the two values of operands are equal it will return true else return false.</li>
		<li><b> != </b> <br> If the two values of operands are not equal it returns true else returns false.</li>
		<li><b> <> </b> <br> It is similar to not equal operator.</li>
		<li><b> > </b> <br> If the value of left operand is greater than right operand it will return true else it will return 
			false.</li>
		<li><b> < </b> <br> If the value of left operand is less than right operand it will return true else it will return 
			false.</li>
		<li><b> <= </b> <br> If the value of left hand operand is less than or equal to the right hand operand value it will 
			return true else it will return false.</li>
		<li><b> >= </b> <br> If the value of left hand operand is greater than or equal to the value of right hand operand it 
			will return true else it will return false.</li>
	</ul>
<p>Examples of Comparison operators</p>
<!--Code block -->
<figure class="highlight">
<pre><code class="language-python" data-lang="python">
a,b = 5,2
print(a == b)

print(a != b)

print(a <> b)

print(a < b)

print(a > b)

print(a <= b)

print(a >= b)
<br />
<b>Ouput:</b>
False
True
True
False
True
False
True
</code></pre>
</figure>

<h4>Logical Operators</h4>
<ul>
	<li><b> and </b> <br> Logical AND - if both operands are true then the condition will return true. If one of the operand is 
		false it will return false.</li>
	<li><b> or </b> <br> Logical OR - If one of the operand is true it will return true. If both operands are false then only it 
		will return false.</li>
	<li><b> not </b> <br> Logical NOT - If the operand is true it will return false. If operand is false it will return true.</li>
</ul>
<p>Examples of Logical operators</p>
<!--Code block -->
<figure class="highlight">
<pre><code class="language-python" data-lang="python">
a,b = 5,2

print(a and b)

print(a or b)

print(not(a))<br />
<b>Ouput:</b>
True
True
False
</code></pre>
</figure>

<h4>Identity operators</h4>
<ul>
	<li><b>is</b> <br>If the two operands on both side of the operator point to the same object or same memory location it 
		will return true else will return false.</li>
	<li><b>is not</b> <br> If the two operands on both sides of the operator point to the same memory location or same 
		object then it will return fasle, Else it will return true.</li>
</ul>
<p>Examples of Identity operators</p>
<!--Code block -->
<figure class="highlight">
<pre><code class="language-python" data-lang="python">
a = 5
b = a
# If we assign values like above two statements both will point to same memory location.

print(a is b)

print(a is not b)

print(not(a))<br />
<b>Ouput:</b>
True
False
</code></pre>
</figure>

<h4>Membership operators</h4>
<ul>
	<li><b>in</b> <br>If the value of leftt operand is present in right operand sequence a member of the sequence of thr right 
		operand it will return true else it will return false.</li>
	<li><b>not in</b> <br> If the value of leftt operand is present in right operand sequence a member of the sequence of thr right 
		operand it will return false else it will return true.</li>
</ul>
<p>Examples of Membership operators</p>
<!--Code block -->
<figure class="highlight">
<pre><code class="language-python" data-lang="python">
a = [1, 2, 3, 4, 5]
b = 6
# If we assign values like above two statements both will point to same memory location.
print(b in a)

print(b not in a)

print(not(a))<br />
<b>Ouput:</b>
True
False
</code></pre>
</figure>

<h4>Bitwise Operators</h4>
<p>Bitwise operators works on bits. As the name suggests they work on each bit by bit. Foe example a=41 it wll be represented in binary bits form as 0100 0001. Take one example with Binary AND operator.<br/>
a = 41 (0010 1001), b = 25 (0001 1001)
	<pre>
	a & b (a AND b) => 0010 1001
	                   0001 1001
			   ---------
		      (9)  0000 1001
	</pre>
</p>
<ul>
	<li><b> & (Binary AND)</b> <br> if both operands have bit 1 reurns 1 else returns 0.</li>
	<li><b> | (Binary OR)</b> <br> IF either one of the operand bit is 1 it will return 1 else it will return 0.</li>
	<li><b> ^ (Binary XOR)</b> <br> If both bits of the two operands are same it will return 0. If both are different it will return 
		1. </li>
	<li><b> ~ (Binary Ones Compliment)</b> <br> It returns the bit which is the compliment of the original bit. It means if the 
		original bit is 1 it will return 0 and vice versa.</li>
	<li><b> << (Binary LEFT SHIFT)</b> <br> The operand on left will be shifted left by the number of bits specified by the number 
		value on right side of the operator.</li>
	<li><b> >> (Binary RIGHT SHIFT)</b> <br> The operand on left will be shifted right by the number of bits specified by the number 
		value on right side of the operator.</li>
</ul>
<p>Examples of Bitwise operators</p>
<!--Code block -->
<figure class="highlight">
<pre><code class="language-python" data-lang="python">
a = 41
b = 25
# If we assign values like above two statements both will point to same memory location.
print(a & b)

print(a | b)

print(a ^ b)

print(~(a))

print(a << 2)

print(a >> 2)<br />
<b>Ouput:</b>
9
57
48
-42
164
10
</code></pre>
</figure>
<h4>Precedence(which works first when all mixed) Order of the operators from high to low</h4>
<ol>
	<li>**</li>
	<li>~, +, -</li>
	<li>*, /, %, //</li>
	<li>>>, <<</li>
	<li>&</li>
	<li>^, |</li>
	<li><=, <, >, >=</li>
	<li><>, ==, !=</li>
	<li>=, %=, /=, //=, -=, +=, *=, **=</li>
	<li>is, is not</li>
	<li>in, not in</li>
	<li>not, or, and</li>
</ol>
<p>That's it for this lesson. I hope you all liked it. If you want to give any suggestion please feel free to let us know them thriugh the comment section. Have a great day!</p>

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









