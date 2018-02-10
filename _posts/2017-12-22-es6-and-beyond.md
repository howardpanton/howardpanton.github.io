---
layout: post
title: "ES6 and beyond"
description: "Look at the new ES6 features, builtins, fat arrow functions."
youtubeId: znkyiX50Ehk
tags: [web, javascript, ES6, udacity]
---

I've just completed the [Udacity Google Developer Challenge Scholarship](https://classroom.udacity.com/courses/ud899-emea), which
covered Mobile Web development, [Service Workers](https://developer.mozilla.org/en-US/docs/Web/API/Service_Worker_API),
[IndexedDB](https://developer.mozilla.org/en-US/docs/Web/API/IndexedDB_API)
and ES6.

I will go through some of the ES6 syntax and functions I learned on the course,
will cover Service Workers and IndexedDb in a separate post.

ES6, Harmony, ES2015 are all different names for all the same thing Javascript.
This major update has changed the way we write Javascript and it has also introduced
some new builtins.

## Var and Hoisting

There are now two ways to write variables, previously when you we writing Javascript
you would declare a variable using the keyword `var.`

So why the change from `var`,

Variables declared with the `var` keyword were [hoisted](https://developer.mozilla.org/en-US/docs/Glossary/Hoisting)
at runtime, which means they were raised to the top of the function scope.

Javascript is basically putting function declarations in memory before it runs the code. This allows you to use a function in Javascript before you decalre it in your
code.

You can still declare variables using the `var' keyword when you want a variable to
be global, however this is now seen as bad practice.

{% include youtubePlayer.html id=page.youtubeId %}

## Let and Const

Variables declared with let can be reassigned

{% highlight javascript %}
let instructor = 'James';
instructor = 'Richard';
{% endhighlight %}

However they can't be redeclared in the same scope.

{% highlight javascript %}
{
let instructor = 'James';
instructor = 'Richard';

let instructor = 'Dave';
}
{% endhighlight %}
this would fail.

With const the rules are different, a variable declared with const must be
assigned an initial value, but can’t be redeclared in the same scope, and can’t
be reassigned.

{% highlight javascript %}
const INSTRUCTOR = 'James';
{% endhighlight %}
