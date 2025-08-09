---
# Documentation: https://sourcethemes.com/academic/docs/managing-content/

title: "Regular Expressions"
subtitle: ""
summary: "Regular expressions are algebraic notations used to search in text particularly useful when we have patterns to search for in the text."
authors: []
tags: []
categories: []
date: 2019-11-03T09:44:03-05:00
lastmod: 2019-11-03T09:44:03-05:00
featured: false
draft: false

# Featured image
# To use, add an image named `featured.jpg/png` to your page's folder.
# Focal points: Smart, Center, TopLeft, Top, TopRight, Left, Right, BottomLeft, Bottom, BottomRight.
image:
  caption: ""
  focal_point: ""
  preview_only: false

# Projects (optional).
#   Associate this post with one or more of your projects.
#   Simply enter your project's folder or file name without extension.
#   E.g. `projects = ["internal-project"]` references `content/project/deep-learning/index.md`.
#   Otherwise, set `projects = []`.
projects: []
---

<h2>What is Regular Expressions</h2>
Regular expressions are the detectives when it comes to searching for patterns in texts. They have been used in my favourite command line tool <b>grep</b> as well. We give short description of culprit, in this case the pattern, we are looking for in the text and lo-and-behold it will return all the candidates. <a href="https://web.stanford.edu/~jurafsky/slp3/2.pdf">Chapter 2</a> of Dan Jurafsky's book has well defined regular expressions as "algebraic notation" that are best at finding patterns in text as we will learn next. A thing to remember while using regular expressions is that it is <b>case-sensitive</b> and will return the texts exactly match the pattern. It would be like if you gave description of the thief that stole your bag then the regular expression would just bring back the thief not the bag.

<h2>Basic Regular Expression Patterns</h2>
Do we have to learn a new language to do this? Now, that would be tedious and is therefore not required. The patterns of regular expression, the way to describe the pattern we need if you may, is easy once you get to know them. Let's look at some of them.

<h3>Simple Search</h3>
Simple search in regular expressions is , as you might have guessed, when we want to search for specific word or set of characters in a text. Regular expressions are <b>case-sensitive</b> so it will return the matched text if an only if the pattern exists down to the case.

<h3>Disjunction</h3>
To solve for the case-sensitiveness or single search, we give set of options within large braces (<b>[</b> and <b>]</b>). For example, to avoid case sensitiveness we can search for <b>[fF]</b>ox which will match for both "Fox" and "fox". 

We can even use a dash (<b>-</b>) to define the range of characters inside the braces. [0-9], [a-z], and [A-Z] will match a single digit, a lowercase letter and an uppercase letter respectively.

<h3>Caret (^)</h3>
We use caret with disjunction to let the regular expression detective know patterns we don't want to match. For example, [~A-Z] will not match for an uppercase letter. 

An important note here is that this expression works if we use it at the beginning of disjunction otherwise it is just another character to be matched. For example, [A-Z^] will match any upper case character or caret character in the text.

<h3>Question mark (?)</h3>
We use this operator if we want to match none or one instance of character prior to "?" in simple search. For example, if we use regular expression /colou?r/ this would return both "color" and "colour", should it match, as the regular expression (?) makes "u" matching optional.

<h3>Kleene</h3>
From the expressions till now if we have to match multiple of same characters (e.g. z, zz, zzz, zzzz...) we have to mention it somehow in the regular expression which seems tedious. We instead use Kleene (+) or (*) expression in disjunction which would allow us to make "one or more" or "none or more" of characters preceeding the expression. 

If we use [ab*] and [0-9][0-9]*, it would match zero or more a's or b's and a single digit or single digit followed by arbitary length of numbers respectively. If we use [0-9][0-9]+, it would match one digit followed by one or more digits.

<h3>Wildcard (.)</h3>
If we want to match any one character but not sure which one we can use wildcard. For example if we use /ha.ry/, we will get haary to hazry and so on based on what match it finds.

<h3> Grouping and precedence</h3>
If we want to match multiple patterns we can use <b>|</b> character. For example, [dog|cat] would match either dog or cat. Similarly if we want to match certain options within a same word we can group them within small paranthesis. For example, [pupp(y|ies)] will match puppy and puppies.

While using the regular expressions there is certain order that it follows: parenthesis, counters, sequences and anchors, and |

<br />
<b>References:</b><br>
https://web.stanford.edu/~jurafsky/slp3/2.pdf