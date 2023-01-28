# CSS-Basics

CSS stands for Cascading Style Sheets, and it's a way to describe style rules that we'd like to set for our HTML elements. Using CSS we can alter things like colors, fonts, margins, text alignment, and much more

There are three ways to include CSS in our web pages:
1. Inline styling. This is done by adding a style attribute to an HTML tag. We will see shortly that this can have some unintended consequences.
2. <style></style>. This is done by using a style tag and placing CSS inside of it.
3. External stylesheets. need to know how to link the CSS to the HTML with a link tag! If we have a file called style.css in the same folder as our HTML file, we can link them with the following tag, which you should place inside of the head element
<!-- <link rel="stylesheet" href="style.css"> -->

One important thing to know about CSS is the C, or cascading nature of CSS. This means that your code is read top to bottom, so if you have the same level of specificity, the rule closest to the bottom wins.

## Syntax and Selectors

Each CSS rule consists of a selector (how we find the element/elements) to target and a pair of curly braces, a.k.a. {}. Inside of {} we specify properties and values; we separate the two with a :, and after the value we add a ;. To add multiple selectors we separate each one by a ,. 

we can use attributes like class and id to target our elements
- ids must be unique
- you can have multiple elements share the same class

### Other Useful Selectors

#### Descendant Selector
matches all elements that are descendants of a specified element. The selector below will find all of the p tags inside of a footer tag (read the selectors from right to left).

<img width="280" alt="image" src="https://user-images.githubusercontent.com/101606295/215228312-2da8cdbf-fb4a-4e16-b2e4-4d538a39b87a.png">

#### Adjacent Selector
finds all elements that are directly adjacent to some other specified element. The selector below will find all the h4 tags that are directly adjacent to an h1 tag.

<img width="280" alt="image" src="https://user-images.githubusercontent.com/101606295/215228638-15b3958a-ea5e-46b8-af0a-0ab699f8a64e.png">

#### Direct child selector
The direct child selector matches all elements that are direct children - not just ancestors - of a specified element. The selector below will find all lis which are children of a ul.

<img width="280" alt="image" src="https://user-images.githubusercontent.com/101606295/215230084-5c0d4809-bbec-448a-bbf5-2d091a6ea0ce.png">

#### Attribute Selector
The attribute selector finds elements based on the value of some attribute. The selector below will find all a tags whose href attribute is set to "#".

<img width="270" alt="image" src="https://user-images.githubusercontent.com/101606295/215230242-5c4b74a5-0dea-4449-b216-ceb250c5bfe5.png">

#### First / Last Child Selector
The first-child and last-child selectors find all elements which are the first (or last, respectively) children of their parents. The selector below will find all the li's which are the first children of their parents.

<img width="280" alt="image" src="https://user-images.githubusercontent.com/101606295/215230282-aa3192fc-1c57-4ff0-8263-40fbad30abed.png">

#### n-th child selector
will find all elements which are the nth children of their parents, for some specified value of n. The selector below will find all the li's which are the second children of their parents.

<img width="280" alt="image" src="https://user-images.githubusercontent.com/101606295/215230368-59d93a0a-8ad7-4fa0-a487-3b969cc284c7.png">

## Specificity

One of the most important ideas around CSS is that of specificity, or how specific we are with our selectors
These weightings are not exact (10 element selectors does not equal a class selector), it is more an idea of showing you the magnitude of each kind of selector.

<img width="306" alt="Screenshot 2023-01-27 at 8 23 41 PM" src="https://user-images.githubusercontent.com/101606295/215234023-ad6fe43c-562f-46fe-9743-87d9e6947003.png">

What this means is that a style rule on an id is weighed much more heavily than a style rule on a class. Similarly, a style rule on a class is weighed more heavily than a rule on an element. Put another way, id rules are more specific than class rules, and class rules are more specific than element rules.












