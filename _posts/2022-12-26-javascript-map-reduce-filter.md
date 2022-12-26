---
layout: post
title: Map, Reduce and Filter in JavaScript
date: 2022-12-26 07:12:00-0400
description: Understanding map, reduce and filter in JavaScript
tags: map, reduce, filter, declarative, high-order
categories: JavaScript external-services
giscus_comments: true
---
**Map**, **Reduce** and **Filter** are three declarative and higher-order array methods that are particularly important in JavaScript applications and even the majority of all modern programming languages. Each of these three methods iterates over a given array and performs specific actions. Steven Luscher humorously described them in a single tweet, as shown below. 

{% twitter https://twitter.com/steveluscher/status/741089564329054208 %}

### The map Method

The map(callback) method returns a new array by applying the given callback function to every element of the given array. Let's initially declare an array of books, where each book is an object, as follows:
<div class="row mt-3">
    <div class="col-sm mt-3 mt-md-0">
        {% include figure.html path="assets/img/booksArray.png" class="img-fluid rounded " zoomable=true %}
    </div>
</div>

Now, let's see how to use the map() method to map the details of each book into a sentence.

<div class="row mt-3">
    <div class="col-sm mt-3 mt-md-0">
        {% include figure.html path="assets/img/map.png" class="img-fluid rounded z-depth-1" zoomable=true %}
    </div>
</div>

Remember that the map method returns a new array, so it is an anti-pattern not to use the returned array. Therefore, it would be better to use the forEach or for...of loops if you are not going to use the returned array or if the used callback does not return a value.

### The filter Method

The filter(callback) method creates a new array with all elements that pass the condition made by the given callback function. The filter() method would return an empty array if all elements did not pass the condition. The following code snippet uses the filter() method to return books that have been published after 2018.
<div class="row mt-3">
    <div class="col-sm mt-3 mt-md-0">
        {% include figure.html path="assets/img/filter.png" class="img-fluid rounded z-depth-1" zoomable=true %}
    </div>
</div>
In addition, the following code snippet shows how to apply the map() method to the filtered data so that we can return textual descriptions of the recent JavaScript books.
<div class="row mt-3">
    <div class="col-sm mt-3 mt-md-0">
        {% include figure.html path="assets/img/mapFiltered.png" class="img-fluid rounded z-depth-1" zoomable=true %}
    </div>
</div>

### The reduce Method

As in map and filter, the reduce(callback) executes the given callback function (known as a reducer) on each element of the array, in order, while passing in the previously calculated value from the previous array element to the next element and returning a single value by the end. The following code snippet shows how to use the reduce method to calculate the sum of all elements in the array.
<div class="row mt-3">
    <div class="col-sm mt-3 mt-md-0">
        {% include figure.html path="assets/img/reduce.png" class="img-fluid rounded z-depth-1" zoomable=true %}
    </div>
</div>
If you did not specify an initial value, the reduce method will use the element at index 0 as the initial value, and the calculation starts from the second element (element at index 1). 