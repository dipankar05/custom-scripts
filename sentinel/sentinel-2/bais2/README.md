---
permalink: /sentinel-2/bais2/
nav_exclude: true
---

# BAIS2 (Burned Area Index for Sentinel 2)

<a href="#" id='togglescript'>Show</a> script or [download](script.js){:target="_blank"} it.
<div id='script_view' style="display:none">
{% highlight javascript %}
{% include_relative script.js %}
{% endhighlight %}
</div>

## Evaluate and visualize
 - [Sentinel Playground](https://apps.sentinel-hub.com/sentinel-playground/?source=S2&lat=28.034258491403897&lng=-15.69671630859375&zoom=12&preset=CUSTOM&layers=B01,B02,B03&maxcc=61&gain=1.0&gamma=1.0&time=2019-02-01%7C2019-08-19&atmFilter=&showDates=false&evalscript=Ly8KLy8gQnVybmVkIEFyZWEgSW5kZXggZm9yIFNlbnRpbmVsLTIgICAoYWJicnYuIEJBSVMyKQovLyBCYXNlZCBvbiBET0k6IDEwLjMzOTAvZWNycy0yLTA1MTc3IAovLyAybmQgSW50ZXJuYXRpb25hbCBFbGVjdHJvbmljIENvbmZlcmVuY2Ugb24gUmVtb3RlIFNlbnNpbmcsIFZvbHVtZTogUHJvY2VlZGluZ3MsIDIoNyksIDM2NAovLyBCeSBGZWRlcmljbyBGaWxpcHBvbmkgb2YgSVNQUkEKLy8gVVJMIGh0dHBzOi8vd3d3LnJlc2VhcmNoZ2F0ZS5uZXQvcHVibGljYXRpb24vMzIzOTY0MTI0X0JBSVMyX0J1cm5lZF9BcmVhX0luZGV4X2Zvcl9TZW50aW5lbC0yCi8vIEFkYXB0ZWQgYnkgSGFyZWwgRGFuLiBASGFyZWxEYW4sIGhhcmVsLmR1bm5AZ21haWwuY29tCi8vCgpsZXQgaW5kZXggPSAoMS0oKEIwNipCMDcqQjhBKS9CMDQpKiowLjUpKigoQjEyLUI4QSkvKChCMTIrQjhBKSoqMC41KSsxKTsKbGV0IG1pbiA9IDA7CmxldCBtYXggPSAwLjk5OwpsZXQgemVybyA9IDAuNTsKCi8vIGNvbG9yQmxlbmQgd2lsbCByZXR1cm4gYSBjb2xvciB3aGVuIHRoZSBpbmRleCBpcyBiZXR3ZWVuIG1pbiBhbmQgbWF4IGFuZCB3aGl0ZSB3aGVuIGl0IGlzIGxlc3MgdGhhbiBtaW4uCi8vIFRvIHNlZSBibGFjayB3aGVuIGl0IGlzIG1vcmUgdGhhbiBtYXgsIHVuY29tbWVudCB0aGUgbGFzdCBsaW5lIG9mIGNvbG9yQmxlbmQuCi8vIFRoZSBtaW4vbWF4IHZhbHVlcyB3ZXJlIGNvbXB1dGVkIGF1dG9tYXRpY2FsbHkgYW5kIG1heSBiZSBwb29ybHkgc3BlY2lmaWVkLCBmZWVsIGZyZWUgdG8gY2hhbmdlIHRoZW0gdG8gdHdlYWsgdGhlIGRpc3BsYXllZCByYW5nZS4KLy8gVGhpcyBpbmRleCBjcm9zc2VzIHplcm8sIHNvIGEgZGl2ZXJnaW5nIGNvbG9yIG1hcCBpcyB1c2VkLiBUbyB0d2VhayB0aGUgdmFsdWUgb2YgdGhlIGJyZWFrIGluIHRoZSBjb2xvciBtYXAsIGNoYW5nZSB0aGUgdmFyaWFibGUgJ3plcm8nLgoKbGV0IHVuZGVyZmxvd19jb2xvciA9IFsxLCAxLCAxXTsKbGV0IGxvd19jb2xvciA9IFswLzI1NSwgMC8yNTUsIDI1NS8yNTVdOwpsZXQgaGlnaF9jb2xvciA9IFsyNTUvMjU1LCAyMC8yNTUsIDIwLzI1NV07CmxldCB6ZXJvX2NvbG9yID0gWzI1MC8yNTUsIDI1NS8yNTUsIDEwLzI1NV07CmxldCBvdmVyZmxvd19jb2xvciA9IFsyNTUvMjU1LCAwLzI1NSwgMjU1LzI1NV07CgpyZXR1cm4gY29sb3JCbGVuZChpbmRleCwgW21pbiwgbWluLCB6ZXJvLCBtYXhdLApbCgl1bmRlcmZsb3dfY29sb3IsCglsb3dfY29sb3IsCgl6ZXJvX2NvbG9yLCAvLyBkaXZlcmdlbnQgc3RlcCBhdCB6ZXJvCgloaWdoX2NvbG9yLAoJb3ZlcmZsb3dfY29sb3IgLy8gdW5jb21tZW50IHRvIHNlZSBvdmVyZmxvd3MKXSk7){:target="_blank"}    
 - [EO Browser](https://apps.sentinel-hub.com/eo-browser/?lat=27.9401&lng=-15.6967&zoom=11&time=2019-08-19&preset=CUSTOM&datasource=Sentinel-2%20L1C&layers=B01,B02,B03&evalscript=Ly8gQnVybmVkIEFyZWEgSW5kZXggZm9yIFNlbnRpbmVsLTIgICAoYWJicnYuIEJBSVMyKQovLyBCYXNlZCBvbiBET0k6IDEwLjMzOTAvZWNycy0yLTA1MTc3IAovLyAybmQgSW50ZXJuYXRpb25hbCBFbGVjdHJvbmljIENvbmZlcmVuY2Ugb24gUmVtb3RlIFNlbnNpbmcsIFZvbHVtZTogUHJvY2VlZGluZ3MsIDIoNyksIDM2NAovLyBCeSBGZWRlcmljbyBGaWxpcHBvbmkgb2YgSVNQUkEKLy8gVVJMIGh0dHBzOi8vd3d3LnJlc2VhcmNoZ2F0ZS5uZXQvcHVibGljYXRpb24vMzIzOTY0MTI0X0JBSVMyX0J1cm5lZF9BcmVhX0luZGV4X2Zvcl9TZW50aW5lbC0yCi8vIEFkYXB0ZWQgYnkgSGFyZWwgRGFuLiBASGFyZWxEYW4sIGhhcmVsLmR1bm5AZ21haWwuY29tCi8vCgpsZXQgaW5kZXggPSAoMS0oKEIwNipCMDcqQjhBKS9CMDQpKiowLjUpKigoQjEyLUI4QSkvKChCMTIrQjhBKSoqMC41KSsxKTsKbGV0IG1pbiA9IDA7CmxldCBtYXggPSAwLjk5OwpsZXQgemVybyA9IDAuNTsKCi8vIGNvbG9yQmxlbmQgd2lsbCByZXR1cm4gYSBjb2xvciB3aGVuIHRoZSBpbmRleCBpcyBiZXR3ZWVuIG1pbiBhbmQgbWF4IGFuZCB3aGl0ZSB3aGVuIGl0IGlzIGxlc3MgdGhhbiBtaW4uCi8vIFRvIHNlZSBibGFjayB3aGVuIGl0IGlzIG1vcmUgdGhhbiBtYXgsIHVuY29tbWVudCB0aGUgbGFzdCBsaW5lIG9mIGNvbG9yQmxlbmQuCi8vIFRoZSBtaW4vbWF4IHZhbHVlcyB3ZXJlIGNvbXB1dGVkIGF1dG9tYXRpY2FsbHkgYW5kIG1heSBiZSBwb29ybHkgc3BlY2lmaWVkLCBmZWVsIGZyZWUgdG8gY2hhbmdlIHRoZW0gdG8gdHdlYWsgdGhlIGRpc3BsYXllZCByYW5nZS4KLy8gVGhpcyBpbmRleCBjcm9zc2VzIHplcm8sIHNvIGEgZGl2ZXJnaW5nIGNvbG9yIG1hcCBpcyB1c2VkLiBUbyB0d2VhayB0aGUgdmFsdWUgb2YgdGhlIGJyZWFrIGluIHRoZSBjb2xvciBtYXAsIGNoYW5nZSB0aGUgdmFyaWFibGUgJ3plcm8nLgoKbGV0IHVuZGVyZmxvd19jb2xvciA9IFsxLCAxLCAxXTsKbGV0IGxvd19jb2xvciA9IFswLzI1NSwgMC8yNTUsIDI1NS8yNTVdOwpsZXQgaGlnaF9jb2xvciA9IFsyNTUvMjU1LCAyMC8yNTUsIDIwLzI1NV07CmxldCB6ZXJvX2NvbG9yID0gWzI1MC8yNTUsIDI1NS8yNTUsIDEwLzI1NV07CmxldCBvdmVyZmxvd19jb2xvciA9IFsyNTUvMjU1LCAwLzI1NSwgMjU1LzI1NV07CgpyZXR1cm4gY29sb3JCbGVuZChpbmRleCwgW21pbiwgbWluLCB6ZXJvLCBtYXhdLApbCgl1bmRlcmZsb3dfY29sb3IsCglsb3dfY29sb3IsCgl6ZXJvX2NvbG9yLCAvLyBkaXZlcmdlbnQgc3RlcCBhdCB6ZXJvCgloaWdoX2NvbG9yLAoJb3ZlcmZsb3dfY29sb3IgLy8gdW5jb21tZW50IHRvIHNlZSBvdmVyZmxvd3MKXSk7Cg%3D%3D){:target="_blank"}   


## General description of the script

BAIS2 adapts the traditional BAI for Sentinel-2 bands, taking advantage of the wider spectrum of Visible, Red-Edge, NIR and SWIR bands.

Values description: The range of values for the BAIS2 is -1 to 1 for burn scars, and 1 - 6 for active fires. Different fire intensities
may result in different thresholds, the current values were calibrates, as per original author, on mostly Mediterranen regions.

## Description of representative images

Burned area index, Las Palmas de Grand Canaria. Acquired on 19.08.2019.

![snow classifier](fig/fig1.png)