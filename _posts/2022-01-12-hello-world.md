---
layout: post
title:  "Hello world!"
date:   2022-01-12 14:21:34 -0800
categories: jekyll update
---
I'm forging ahead with Jekyll as my documentation builder for now, because it's straightforward and directly
links with `gh-pages`, despite it not being an official "documentation" generator *a la* readthedocs, etc.

The intention here is not to be documentation in the official sense, which will ideally come later, but instead
a place for me to document my actual process in building the resource (working title: Compendia). To this end,
a blog platform is maybe the more suitable tool. 

In any case, I've only put an hour or so into getting the repository, `gh-pages` branch, and Jekyll 
implementation set up, with no time spent actually building Compendia itself. We'll see if anything
actually develops from here...

(I'll leave this Jekyll content below because it's currently showing me some syntax that I want to
remember without googling it 19 times when I actually need it)

Jekyll also offers powerful support for code snippets:

{% highlight ruby %}
def print_hi(name)
  puts "Hi, #{name}"
end
print_hi('Tom')
#=> prints 'Hi, Tom' to STDOUT.
{% endhighlight %}

Check out the [Jekyll docs][jekyll-docs] for more info on how to get the most out of Jekyll. File all bugs/feature requests at [Jekyll’s GitHub repo][jekyll-gh]. If you have questions, you can ask them on [Jekyll Talk][jekyll-talk].

[jekyll-docs]: http://jekyllrb.com/docs/home
[jekyll-gh]:   https://github.com/jekyll/jekyll
[jekyll-talk]: https://talk.jekyllrb.com/
