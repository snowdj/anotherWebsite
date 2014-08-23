---
layout: post    
title:  "I am alive!"
description: ""
date:   3013-06-12 21:00:39
categories: programming
math: true
comments: true
image:
    feature: night_sunset.jpg
---

I am finally online!  


This is a text with a
footnote[^1].

I found that it is beautiful footnotes[^2]

Some Ruby:

{% highlight ruby %}
def print_hi(name)
  puts "Hi, #{name}"
end
print_hi('Allan')
#> 'Hi, Allan'
{% endhighlight %}

Some Python:

{% highlight python %}
def print_hi(name):
  print "Hi, %s" % name

print_hi('Allan')
#> 'Hi, Allan'
{% endhighlight %}

Some C:

{% highlight c %}
void function print_hi(char* name){
  printf("Hi, %s", name);
}

name = "Allan";
print_hi(name);
#> 'Hi, Allan'
{% endhighlight %}

Some math:
$$x^2$$


Now that was easy! Inline: \\( x_1 + x_2 = 5 \\).

\\[ x^3 - x^2 = 10 \\]


<blockquote cite="http://www.worldwildlife.org/who/index.html">
For 50 years, WWF has been protecting the future of nature. The world's leading conservation organization, WWF works in 100 countries and is supported by 1.2 million members in the United States and close to 5 million globally.
</blockquote>

What about a table?

<table summary="Employee Pay Sheet">
    <thead>
        <tr>
            <th scope="col">Employee</th>
            <th scope="col">Salary</th>
            <th scope="col">Bonus</th>
            <th scope="col">Supervisor</th>
        </tr>
    </thead>
    <tbody>
        <tr>
            <td>Stephen C. Cox</td>
            <td>$300</td>
            <td>$50</td>
            <td>Bob</td>
        </tr>
        <tr>
            <td>Josephin Tan</td>
            <td>$150</td>
            <td>-</td>
            <td>Annie</td>
        </tr>
        <tr>
            <td>Joyce Ming</td>
            <td>$200</td>
            <td>$35</td>
            <td>Andy</td>
        </tr>
        <tr>
            <td>James A. Pentel</td>
            <td>$175</td>
            <td>$25</td>
            <td>Annie</td>
        </tr>
    </tbody>
</table>


| Header | Header | Right  |
| ------ | ------ | -----: |
|  Cell  |  Cell  |   $10  |
|  Cell  |  Cell  |   $20  |

Notes:

[^1]: And here is the definition.
[^2]: Indeed it is.