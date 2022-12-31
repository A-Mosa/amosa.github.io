---
layout: post
title:  JavaScript Type System
date:   2022-12-24 20:05:00
description: Explaining the concept of type systems in programming languages. You will understand the difference between static and dyanmic typing as well as strong and weak typing. You will also learn that JavaScript is dynamically and weakly typed language.
tags: JavaScript, Type-System, dynamic-typing, static-typing, weak-typing, strong-typing
categories: JavaScript
giscus_comments: true
---
<blockquote>
    JavaScript is known to be dynamically and weakly or loosely typed.
</blockquote>
In any programming language, the <b>type system </b> is usually built into the compiler or interpreter to assign a <b>type to a value </b> or any programming construct (such as variables and functions) and specify the <b>allowed operations</b> on each data type. The type system is useful in several aspects, such as reducing type errors and enabling certain compiler optimizations. Programming languages can check for the type during <b>compile time (static)</b>, <b>run time (dynamic)</b>, or at <b>both</b>. Programming languages are classified based on the type checking (**static vs dynamic**) and the type safety (**strong vs weak**). So, let's try to understand the difference between them.

{% mermaid %}

graph TD
    A[Type System] --> B(When?)
    A[Type System] --> C(How Strict?)
    B --> D(Compile time)
    B --> E(Run time)
    D --> F(Static)
    E --> G(Dynamic)
    C --> H(Strict)
    C --> I(Flexible)
    H --> J(Strong)
    I --> K(Weak)

{% endmermaid %}
<br>

#### Type Checking (When?): Static versus Dynamic 
Type checking determines <b>when</b> types are checked and verified. For example, a <b>dynamically-typed</b> programming language checks for the types during <b> run time</b>. However, a <b> statically-typed</b> language checks the types and any syntactic errors during the <b>compile time</b> (before the actual running or execution of the code). JavaScript, PHP, Python and Ruby are examples of dynamically-typed languages. For example, in JavaScript, you can write:

{% highlight python %}
let age = 20;
{% endhighlight %}

So, in the above statement, we have declared a variable without explicitly specifying the data type. The JavaScript interpreter assigns the proper type based on the given value (which will be a number in the above example) and checks for type errors during the run-time. On the other hand, Java, C, C++, Go and Scala are examples of statically-typed languages. Using a statically-typed langauage means that you must explicitly declare the type of the variable. For example, Java would throw a compile-time error if you forgot to specify the type in the following statement.
{% highlight java %}
int age = 20;
{% endhighlight %}

<blockquote>
    Compile time type checking is static, while run time checking is dynamic. Static typing can help catch errors at compile time, and can also improve the performance of a program. Howver, a dynamically typed language is usually flexible and easier to use, but can result in more run time errors.
</blockquote>

#### Type Safety (How Strict/Serious?): Weak versus Strong  
<b>Strongly typed</b> programming languages ​​have <b>stricter typing rules</b>, such as preventing the use of a variable in a way that is incompatible with its type. However, <b>weakly typed</b> languages ​​have more <b>flexible and relaxed typing rules</b>. For example, in a strongly typed language, an explicit data type conversion may be required even if the implicit data type conversion does not cause any problems. Strong and weak typing is a somewhat relative spectrum and not fixed classes, so the typing system of a language may be stronger or weaker than the other. For example, PHP can be classified as a weakly typed language; however, it is more strongly typed than JavaScript. Moreover, strong and weak typing are not related to static and dynamic typing. For example, a dynamically typed language could be either strongly or weakly typed and vice versa. For example, Python is both dynamically- and strongly-typed, as shown in the following type system quadrant: 
<div class="row mt-3">
    <div class="col-sm mt-3 mt-md-0">
        {% include figure.html path="assets/img/TypeSystemQuadrant.PNG" class="img-fluid rounded " zoomable=true %}
    </div>
    <div class="col-sm mt-3 mt-md-0">
        {% include figure.html path="assets/img/10.jpg" class="img-fluid rounded z-depth-1" zoomable=true %}
    </div>
</div>


<blockquote>
    Strict? Strong, else weak.
</blockquote>

<hr>
Try the following code in JavaScript to understand how a weekly-typed language could behave:

{% highlight javascript linenos %}
    console.log("7" + 3);
    console.log("7" * 3);
    console.log("7" / 3);
    console.log(true / 3);
    console.log(true + 3);
    console.log(false + 3);
{% endhighlight %}

<hr>

#### Test your Understanding

1. Which of the following describes `static typing`?
    - A. Type checking is performed at run time
    - B. Type checking is performed at compile time 
    - C. Type checking is performed at run and compile times
2. Which of the following describes `dynamic typing`?
    - A. Type checking is performed at run time
    - B. Type checking is performed at compile time 
    - C. Type checking is performed at run and compile times
3. Which of the following describes `strong typing`?
    - A. Type checking is strict and will not allow operations between incompatible types without type conversion
    - B. Type checking is lenient and will allow operations between incompatible types  
    - C. Type checking is always static in strong typing
    - C. Type checking is always dynamic in weak typing
4. Which of the following describes `weak typing`?
    - A. Type checking is strict and will not allow operations between incompatible types without conversion
    - B. Type checking is lenient and will allow operations between incompatible types  
    - C. Type checking is always static in strong typing
    - D. Type checking is always dynamic in weak typing
4. Which of the following languages is `dynamically typed`?
    - A. Java
    - B. JavaScript 
    - C. C++
    - D. Go
