---
permalink: /sentinel-2/evi2/
nav_exclude: true
---

# EVI2 (Enhanced Vegetation Index 2)

<a href="#" id='togglescript'>Show</a> script or [download](script.js){:target="_blank"} it.
<div id='script_view' style="display:none">
{% highlight javascript %}
{% include_relative script.js %}
{% endhighlight %}
</div>

## Evaluate and visualize
 - [Sentinel Playground](https://apps.sentinel-hub.com/sentinel-playground/?source=S2&lat=42.10051506871418&lng=12.23602294921875&zoom=11&preset=CUSTOM&layers=B01,B02,B03&maxcc=20&gain=1.0&gamma=1.0&time=2019-05-01%7C2019-11-21&atmFilter=&showDates=false&evalscript=Ly8gRW5oYW5jZWQgVmVnZXRhdGlvbiBJbmRleCAyICAoYWJicnYuIEVWSTIpCi8vIEdlbmVyYWwgZm9ybXVsYTogMi41ICogKE5JUiAtIFJFRCkgLyAoKE5JUiArIFJFRCArIDEpCi8vIFVSTCBodHRwczovL3d3dy5pbmRleGRhdGFiYXNlLmRlL2RiL3NpLXNpbmdsZS5waHA%2Fc2Vuc29yX2lkPTk2JnJzaW5kZXhfaWQ9MTYKCmxldCBFVkkyID0gMi40ICogKEIwOCAtIEIwNCkgLyAoQjA4ICsgQjA0ICsgMS4wKTsKCmlmIChFVkkyPC0xLjEpIHJldHVybiBbMCwwLDBdOwplbHNlIGlmIChFVkkyPC0wLjIpIHJldHVybiBbMC43NSwwLjc1LDFdOwplbHNlIGlmIChFVkkyPC0wLjEpIHJldHVybiBbMC44NiwwLjg2LDAuODZdOwplbHNlIGlmIChFVkkyPDApIHJldHVybiBbMSwxLDAuODhdOwplbHNlIGlmIChFVkkyPDAuMDI1KSByZXR1cm4gWzEsMC45OCwwLjhdOwplbHNlIGlmIChFVkkyPDAuMDUpIHJldHVybiBbMC45MywwLjkxLDAuNzFdOwplbHNlIGlmIChFVkkyPDAuMDc1KSByZXR1cm4gWzAuODcsMC44NSwwLjYxXTsKZWxzZSBpZiAoRVZJMjwwLjEpIHJldHVybiBbMC44LDAuNzgsMC41MV07CmVsc2UgaWYgKEVWSTI8MC4xMjUpIHJldHVybiBbMC43NCwwLjcyLDAuNDJdOwplbHNlIGlmIChFVkkyPDAuMTUpIHJldHVybiBbMC42OSwwLjc2LDAuMzhdOwplbHNlIGlmIChFVkkyPDAuMTc1KSByZXR1cm4gWzAuNjQsMC44LDAuMzVdOwplbHNlIGlmIChFVkkyPDAuMikgcmV0dXJuIFswLjU3LDAuNzUsMC4zMl07CmVsc2UgaWYgKEVWSTI8MC4yNSkgcmV0dXJuIFswLjUsMC43LDAuMjhdOwplbHNlIGlmIChFVkkyPDAuMykgcmV0dXJuIFswLjQ0LDAuNjQsMC4yNV07CmVsc2UgaWYgKEVWSTI8MC4zNSkgcmV0dXJuIFswLjM4LDAuNTksMC4yMV07CmVsc2UgaWYgKEVWSTI8MC40KSByZXR1cm4gWzAuMzEsMC41NCwwLjE4XTsKZWxzZSBpZiAoRVZJMjwwLjQ1KSByZXR1cm4gWzAuMjUsMC40OSwwLjE0XTsKZWxzZSBpZiAoRVZJMjwwLjUpIHJldHVybiBbMC4xOSwwLjQzLDAuMTFdOwplbHNlIGlmIChFVkkyPDAuNTUpIHJldHVybiBbMC4xMywwLjM4LDAuMDddOwplbHNlIGlmIChFVkkyPDAuNikgcmV0dXJuIFswLjA2LDAuMzMsMC4wNF07CmVsc2UgcmV0dXJuIFswLDAuMjcsMF07){:target="_blank"}
 - [EO Browser](https://apps.sentinel-hub.com/eo-browser/?lat=42.3388&lng=11.9971&zoom=10&time=2017-10-08&preset=CUSTOM&datasource=Sentinel-2%20L1C&layers=B01,B02,B03&evalscript=Ly8gRW5oYW5jZWQgVmVnZXRhdGlvbiBJbmRleCAgKGFiYnJ2LiBFVkkpCi8vIEdlbmVyYWwgZm9ybXVsYTogMi41ICogKE5JUiAtIFJFRCkgLyAoKE5JUiArIDYqUkVEIC0gNy41KkJMVUUpICsgMSkKLy8gVVJMIGh0dHBzOi8vd3d3LmluZGV4ZGF0YWJhc2UuZGUvZGIvc2ktc2luZ2xlLnBocD9zZW5zb3JfaWQ9OTYmcnNpbmRleF9pZD0xNgoKbGV0IEVWSTIgPSAyLjQgKiAoQjA4IC0gQjA0KSAvIChCMDggKyBCMDQgKyAxLjApOwoKaWYgKEVWSTI8LTEuMSkgcmV0dXJuIFswLDAsMF07CmVsc2UgaWYgKEVWSTI8LTAuMikgcmV0dXJuIFswLjc1LDAuNzUsMV07CmVsc2UgaWYgKEVWSTI8LTAuMSkgcmV0dXJuIFswLjg2LDAuODYsMC44Nl07CmVsc2UgaWYgKEVWSTI8MCkgcmV0dXJuIFsxLDEsMC44OF07CmVsc2UgaWYgKEVWSTI8MC4wMjUpIHJldHVybiBbMSwwLjk4LDAuOF07CmVsc2UgaWYgKEVWSTI8MC4wNSkgcmV0dXJuIFswLjkzLDAuOTEsMC43MV07CmVsc2UgaWYgKEVWSTI8MC4wNzUpIHJldHVybiBbMC44NywwLjg1LDAuNjFdOwplbHNlIGlmIChFVkkyPDAuMSkgcmV0dXJuIFswLjgsMC43OCwwLjUxXTsKZWxzZSBpZiAoRVZJMjwwLjEyNSkgcmV0dXJuIFswLjc0LDAuNzIsMC40Ml07CmVsc2UgaWYgKEVWSTI8MC4xNSkgcmV0dXJuIFswLjY5LDAuNzYsMC4zOF07CmVsc2UgaWYgKEVWSTI8MC4xNzUpIHJldHVybiBbMC42NCwwLjgsMC4zNV07CmVsc2UgaWYgKEVWSTI8MC4yKSByZXR1cm4gWzAuNTcsMC43NSwwLjMyXTsKZWxzZSBpZiAoRVZJMjwwLjI1KSByZXR1cm4gWzAuNSwwLjcsMC4yOF07CmVsc2UgaWYgKEVWSTI8MC4zKSByZXR1cm4gWzAuNDQsMC42NCwwLjI1XTsKZWxzZSBpZiAoRVZJMjwwLjM1KSByZXR1cm4gWzAuMzgsMC41OSwwLjIxXTsKZWxzZSBpZiAoRVZJMjwwLjQpIHJldHVybiBbMC4zMSwwLjU0LDAuMThdOwplbHNlIGlmIChFVkkyPDAuNDUpIHJldHVybiBbMC4yNSwwLjQ5LDAuMTRdOwplbHNlIGlmIChFVkkyPDAuNSkgcmV0dXJuIFswLjE5LDAuNDMsMC4xMV07CmVsc2UgaWYgKEVWSTI8MC41NSkgcmV0dXJuIFswLjEzLDAuMzgsMC4wN107CmVsc2UgaWYgKEVWSTI8MC42KSByZXR1cm4gWzAuMDYsMC4zMywwLjA0XTsKZWxzZSByZXR1cm4gWzAsMC4yNywwXTs%3D){:target="_blank"}

## General description of the script

In areas of dense canopy where the leaf area index (LAI) is high, the NDVI values can be improved by leveraging information in the blue wavelength. Information in this portion of the spectrum can help correct for soil background signals and atmospheric influences.

## Description of representative images

EVI2, Italy. Acquired on 08.10.2017, processed by Sentinel Hub. 

![EVI2](fig/fig1.png)
