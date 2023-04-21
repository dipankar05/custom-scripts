---
permalink: /sentinel-2/agriculture_growth_stage/
nav_exclude: true
---

# Agricultural growth stage

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

 - [Sentinel Playground](https://apps.sentinel-hub.com/sentinel-playground-temporal/?baseWmsUrl=services.sentinel-hub.com&instanceID=7bd7e1c0-4574-45b3-9d73-4f320e1c2e4f&source=S2&lat=45.62484313095204&lng=12.420730590820312&zoom=11&preset=CUSTOM&layers=B01,B02,B03&maxcc=30&gain=1&gamma=1&time=2015-01-01%7C2017-08-31&atmFilter=ATMCOR&showDates=false&evalscript=Ly9WRVJTSU9OPTMgKGF1dG8tY29udmVydGVkIGZyb20gMSkKLyoKU291cmNlOiBASGFyZWxEYW4gLSBodHRwczovL2dpdGh1Yi5jb20vaGFyZWxkdW5uL0dJU19SZXBvL2Jsb2IvbWFzdGVyL011bHRpLVRlbXBvcmFsJTIwTkRWSSUyMGZvciUyMFNlbnRpbmVsJTIwSHViJTIwQ3VzdG9tJTIwU2NyaXB0cwpWaXN1YWxpemluZyBORFZJIG11bHRpLXRlbXBvcmFsIHRyZW5kcyBpbiBTZW50aW5lbC0yIGltYWdlcnkuCkNvcHkgaW50byBTZW50aW5lbC1IdWIgUGxheWdyb3VuZCAKd2lsbCB0YWtlIHRoZSBjdXJyZW50IGltYWdlIGFzIGJhc2VsaW5lIGFuZCBjYWxjdWxhdGUgYXZlcmFnZSBORFZJIGZvciB0aGUgcHJldmlvdXMgMiBtb250aHMKQmFzZWQgb246Cmh0dHBzOi8vdHdpdHRlci5jb20vc2VudGluZWxfaHViL3N0YXR1cy85MjI4MTM0NTcxNDUyMjExMjEKaHR0cHM6Ly90d2l0dGVyLmNvbS9zZW50aW5lbF9odWIvc3RhdHVzLzEwMjA3NTU5OTYzNTkyMjUzNDQKU2NyaXB0IHJlcXVpcmVzIG11bHRpLXRlbXBvcmFsIHByb2Nlc3Npbmcgc28gcGFyYW1ldGVyIFRFTVBPUkFMPXRydWUgc2hvdWxkIGJlIGFkZGVkIHRvIHRoZSByZXF1ZXN0LgoqLwoKZnVuY3Rpb24gc2V0dXAoKSB7CiAgcmV0dXJuIHsKICAgIGlucHV0OiBbewogICAgICBiYW5kczogWwogICAgICAgICAgICAgICAgICAiQjA0IiwKICAgICAgICAgICJCMDgiCiAgICAgIF0KICAgIH1dLAogICAgb3V0cHV0OiB7IGJhbmRzOiAzIH0sCiAgICBtb3NhaWNraW5nOiAiT1JCSVQiCiAgfQp9CgoKZnVuY3Rpb24gY2FsY05EVkkoc2FtcGxlKSB7CiAgdmFyIGRlbm9tID0gc2FtcGxlLkIwNCtzYW1wbGUuQjA4OwogIHJldHVybiAoKGRlbm9tIT0wKSA%2FIChzYW1wbGUuQjA4LXNhbXBsZS5CMDQpIC8gZGVub20gOiAwLjApOwp9CmZ1bmN0aW9uICBzdHJldGNoKHZhbCwgbWluLCBtYXgpICB7CiByZXR1cm4gKHZhbC1taW4pLyhtYXgtbWluKTsKfQoKZnVuY3Rpb24gZXZhbHVhdGVQaXhlbChzYW1wbGVzLHNjZW5lcykgeyAgCiAgdmFyIGF2ZzEgPSAwOwogIHZhciBjb3VudDEgPSAwOwogIHZhciBhdmcyID0gMDsKICB2YXIgY291bnQyID0gMDsKICB2YXIgYXZnMyA9IDA7CiAgdmFyIGNvdW50MyA9IDA7CiAgdmFyIGVuZE1vbnRoID0gc2NlbmVzWzBdLmRhdGUuZ2V0TW9udGgoKTsKICAKICBmb3IgKHZhciBpPTA7aTxzYW1wbGVzLmxlbmd0aDtpKyspIHsKICAgICAgdmFyIG5kdmkgPSBjYWxjTkRWSShzYW1wbGVzW2ldKTsKICAgICAgaWYgKHNjZW5lc1tpXS5kYXRlLmdldE1vbnRoKCk9PWVuZE1vbnRoKQogICAgICB7CgkJYXZnMyA9IGF2ZzMgKyBuZHZpOwogICAgICAgIGNvdW50MysrOwogICAgICB9CiAgICAgIGVsc2UgaWYgKHNjZW5lc1tpXS5kYXRlLmdldE1vbnRoKCk9PShlbmRNb250aC0xKSkKICAgICAgewoJCWF2ZzIgPSBhdmcyICsgbmR2aTsKICAgICAgICBjb3VudDIrKzsKICAgICAgfQogICAgICBlbHNlCiAgICAgIHsgICAgICAKCQlhdmcxPSBhdmcxICsgbmR2aTsKICAgICAgICBjb3VudDErKzsKICAgICAgfQogICAgICAKICB9CiAgYXZnMSA9IGF2ZzEvY291bnQxOwogIGF2ZzIgPSBhdmcyL2NvdW50MjsKICBhdmczID0gYXZnMy9jb3VudDM7CiAgYXZnMSA9IHN0cmV0Y2goYXZnMSwgMC4xLCAwLjcpOwogIGF2ZzIgPSBzdHJldGNoKGF2ZzIsIDAuMSwgMC43KTsKICBhdmczID0gc3RyZXRjaChhdmczLCAwLjEsIDAuNyk7CiAgCiAgcmV0dXJuIFthdmcxLGF2ZzIsYXZnM107CgoKfQpmdW5jdGlvbiBmaWx0ZXJTY2VuZXMgKHNjZW5lcywgaW5wdXRNZXRhZGF0YSkgewogICAgcmV0dXJuIHNjZW5lcy5maWx0ZXIoZnVuY3Rpb24gKHNjZW5lKSB7CgkgIHJldHVybiBzY2VuZS5kYXRlLmdldFRpbWUoKT49KGlucHV0TWV0YWRhdGEudG8uZ2V0VGltZSgpLTMqMzEqMjQqMzYwMCoxMDAwKSA7CiAgICB9KTsKfQo%3D&temporal=true){:target="_blank"}    


## Author of the script
[@HarelDan](https://github.com/hareldunn/GIS_Repo/blob/master/Multi-Temporal%20NDVI%20for%20Sentinel%20Hub%20Custom%20Scripts){:target="_blank"}    

## General description of the script
Agricultural growth stage is a script visualizing the multi-temporal NDVI trends in Sentinel-2 imagery. It takes the current image as baseline and calculates the average NDVI for the previous 2 months.
The script requires multi-temporal processing, so the parameter TEMPORAL=true should be added to the request.

## Description of representative images

The Agricultural growth stage script applied to the agricultural fields of Italy (Veneto). 

![The Agricultural growth stage script applied to agricultural fields of Italy.](fig/fig1.jpg)

## References
Based on: 
[source 1](https://twitter.com/sentinel_hub/status/922813457145221121){:target="_blank"}, 
[source 2](https://twitter.com/sentinel_hub/status/1020755996359225344){:target="_blank"}


