---
permalink: /skysat/true_color/
nav_exclude: true
---

# True color product, SkySat

{% assign paths = page.dir | remove_first: "/" | split: "/" | join: "-"%}
<button class="btn btn-primary" id="toggle-script" onclick="toggleScript()">Show Script</button>
[Download Script](script.js){: .btn target="_blank" download="{{paths | append: ".js"}}"}
{: .mt-lg-4 }

<div id="script" style="display:none;"> 
{% highlight javascript %}
{% include_relative script.js %}
{% endhighlight %}
</div>

## Evaluate and visualize

As SkySat is commercial data, brought into Sentinel Hub as Bring Your Own Data, direct EO Browser and Sentinel Playground links are not possible due to the personalized data credentials.   

## General description

The true color product combines Skysat band values Red, Blue, and Green to create a true color image.

## Description of representative images

True color visualisation over Rome, Italy, acquired on 2018/08/28.

![Small true color image, on 8.10.2017.](fig/skysat_true_color.jpeg)


## References
 - Wikipedia, [True color](https://en.wikipedia.org/wiki/False_color#True_color). Accessed October 10th 2017.