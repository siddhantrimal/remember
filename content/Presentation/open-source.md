+++
title= "Open Source"
date= 2017-11-13T07:26:34+05:45
description = "A presentation on open source, made possible by open source"
draft= false
type="slide"

theme = "serif"
[revealOptions]
transition= 'convex'
controls= true
progress= true
history= true
center= true
+++

# Awesome Source

a.k.a

### Open Source

<small>&dash; a presentation by Siddhant Rimal</small>

--- <!-- .element: data-background-image="/img/presentation-open-source/data-centre.jpg" data-transition="zoom" -->

## Open Source Software in Data Centres <!-- .element: style="color:#fff !important;" -->

<blockquote cite="https://www.computerworld.com/article/2538737/network-software/open-source-software-in-the-data-center.html"><small>__&ldquo;In general, enterprises are using open source in the following three primary areas: Web presence and portals, the small to medium-size database tier and the application tier&rdquo;__<sup style="font-size: 0.8em;">[[1]<!-- .element: style="color:#fff !important;" -->]</sup><br/>
&dash; James Staten, Analyst, Forrester Research Inc.</small></blockquote><!-- .element: style="color:#fff !important;" -->

[1]: https://www.computerworld.com/article/2538737/network-software/open-source-software-in-the-data-center.html

___

### Why?

1. Speeds delivery of software and hardware solutions
1. Saves money
1. Provides flexibility
1. Helps companies stay on the leading edge of technology development<sup style="font-size: 0.5em;">[[2]]</sup>

[2]: https://www.linuxfoundation.org/blog/using-open-source-software-to-speed-development-and-gain-business-advantage/
___ <!-- .element: data-background="/img/presentation-open-source/linux-speed-of-development.gif" data-transition="none" -->

### <!-- .element: style="color:#fff;" --> <span style="background-color:rgba(255,255,255,.3); color:#000; padding-left:.1em; padding-right:.1em;" >but,</span>  __How?__ <!-- .element: style="background-color:rgba(0,0,0,.3); margin-left:-.2em; padding-left:.1em; padding-right:.1em;" -->

Note: [1]Faster, easier aquisition process [2]Quicker Deployments [3]Rapid evolution and innovation [4]Higher quality [5]Ease of customization [6]Evolutionary delivery

--- <!-- .element: data-background-image="/img/presentation-open-source/cloud-computing.jpg" data-transition="fade" data-image-transition="fade"  -->

## Open Source Software in Cloud Computing

--- <!-- .element: data-transition="slide" data-background="#4D7E65" data-background-transition="slide"  -->

## Web Presence <!-- .element: style="color:#fff;" -->

___

### Apache <!-- .element: style="color:rgba(77,126,101,.8);" -->

* Most widely used Webserver software <!-- .element: class="fragment fade-up" data-fragment-index="1" -->
* Runs 67% of all webservers in the world <!-- .element: class="fragment fade-up" data-fragment-index="1" -->
* Fast, Reliable, Secure and highly customizable <!-- .element: class="fragment fade-up" data-fragment-index="1" -->

___

### Jetty <!-- .element: style="color:rgba(77,126,101,.8);" -->

* Eclipse Jetty is a Java HTTP server and Java Servlet container <!-- .element: class="fragment fade-up" data-fragment-index="1" -->
* Used particularly in machine-to-machine communications in large sotware frameworks <!-- .element: class="fragment fade-up" data-fragment-index="1" -->

___

### Zend Framework <!-- .element: style="color:rgba(77,126,101,.8);" -->

* Collection of professional PHP packages with more than 184 million installations <!-- .element: class="fragment fade-up" data-fragment-index="1" -->
* It can be used to develop web applications and services using PHP 5.6+, and provides 100% object-oriented code using a broad spectrum of language features <!-- .element: class="fragment fade-up" data-fragment-index="1" -->
* Focused on Simplicity, Reusability and Performance <!-- .element: class="fragment fade-up" data-fragment-index="1" -->

--- <!-- .element:  data-transition="slide" data-background="#B5533C" data-background-transition="slide" -->

## Database Tier <!-- .element: style="color:#fff;" --> 

___

## MySQL <!-- .element: style="color:rgba(181,83,60,.8);" -->

* MySQL is a database management system <!-- .element: class="fragment fade-up" data-fragment-index="1" -->
* Popularly paired with PHP <!-- .element: class="fragment fade-up" data-fragment-index="1" -->

___

## PostgreSQL <!-- .element: style="color:rgba(181,83,60,.8);" -->

* PostgreSQL is a powerful, open source object-relational database system <!-- .element: class="fragment fade-up" data-fragment-index="1" -->

___ <!-- .element: data-transition="fade" -->

### A quick diff <!-- .element: style="color:rgba(181,83,60,.8);" -->

|MySQL|PostgreSQL|
|---|---|
|The Governance model is not open source|PostgreSQL Global Development Group fully licensed open-source|
|FreeBSD OS support|HP-UX support|

___ <!-- .element: data-transition="slide" -->

### A quick diff <!-- .element: style="color:rgba(181,83,60,.8);" -->

|MySQL|PostgreSQL|
|---|---|
|Replication is master-master, but can also support master-slave|Replication properties are same as MySQL along with added modes of replications possible with 3rd party extensions|

___ <!-- .element: data-transition="slide" -->

### A quick diff <!-- .element: style="color:rgba(181,83,60,.8);" -->

|MySQL|PostgreSQL|
|---|---|
|MySQL Cluster to perform horizontal clustering|Doesn't implement true partitionings|
||More access methods such as the platform's native C library|

--- <!-- .element: data-transition="slide" data-background="#361134" data-background-transition="slide"  -->

## Application Tier <!-- .element: style="color:#fff;" -->

___

## Zope <!-- .element: style="color:rgba(122,59,105,.8);" -->

* Z Object Publishing Environment <!-- .element: class="fragment fade-up" data-fragment-index="1" -->
* Open source web application server written in Python <!-- .element: class="fragment fade-up" data-fragment-index="1" -->

___

## Plone <!-- .element: style="color:rgba(122,59,105,.8);" -->

* Can be classified as Enterprise CMS <!-- .element: class="fragment fade-up" data-fragment-index="1" -->
* Plone is a free and open source content management system built on top of the Zope application server <!-- .element: class="fragment fade-up" data-fragment-index="1" -->

___ <!-- .element: data-transition="slide" -->

## AJAX <!-- .element: style="color:rgba(122,59,105,.8);" -->

* Asynchronous JavaScript and XML <!-- .element: class="fragment fade-up" data-fragment-index="1" -->
* Is a Rich Internet Application technology. <!-- .element: class="fragment fade-up" data-fragment-index="1" -->
* Ajax uses XHTML for content, CSS for presentation, along with Document Object Model and JavaScript for dynamic content display. <!-- .element: class="fragment fade-up" data-fragment-index="1" -->

___ <!-- .element: data-transition="concave" -->

## AJAX <!-- .element: style="color:rgba(122,59,105,.8);" -->
#### <small>an example: _on the html side_</small>

```
<!DOCTYPE html>
	<html>
	<body>

	<div id="demo">
	  <h2>Let AJAX change this text</h2>
	  <button type="button" onclick="loadDoc()">Change Content</button>
	</div>

	</body>
</html>
```
___ <!-- .element: data-transition="concave" -->

## AJAX <!-- .element: style="color:rgba(122,59,105,.8);" -->
#### <small>an example: _AJAX snippet_</small>

```
function loadDoc() {
  var xhttp = new XMLHttpRequest();
  xhttp.onreadystatechange = function() {
    if (this.readyState == 4 && this.status == 200) {
     document.getElementById("demo").innerHTML = this.responseText;
    }
  };
  xhttp.open("GET", "ajax_info.txt", true);
  xhttp.send();
}
```
___ <!-- .element: data-transition="concave" -->

## AJAX <!-- .element: style="color:rgba(122,59,105,.8);" -->
<h4><small>a
<button style="font-size: 1em; line-height:1em; margin-top:.0em;" onclick="swal.queue([{
title: 'Your public IP',
confirmButtonText: 'Show my public IP',
text: 'Your public IP will be received via AJAX request',
showLoaderOnConfirm: true,
preConfirm: function () {
return new Promise(function (resolve) {
  $.get('https://api.ipify.org?format=json')
    .done(function (data) {
      swal.insertQueueStep(data.ip)
      resolve()
    })
})
},
type:'info'
}])">DEMO</button><!-- Wondering about the inline JS? Don't worry, its a design decision to save overhead in this particular use case. If you'll be using this feature a lot, it makes sense to just inject this into the corresponding Revealjs partial -->

_courtesy of [Sweet Alert 2](limonte.github.io/sweetalert2/)_<sup style="font-size: .4em">[MIT](https://opensource.org/licenses/MIT "MIT License")</sup></small></h4>

___

## Apache Struts <!-- .element: style="color:rgba(122,59,105,.8);" -->

* Made for JVM <!-- .element: class="fragment fade-up" data-fragment-index="1" -->
* free, open-source, MVC framework for creating elegant, modern Java web applications <!-- .element: class="fragment fade-up" data-fragment-index="1" -->
* favors convention over configuration, is extensible using a plugin architecture, and ships with plugins to support REST, AJAX and JSON <!-- .element: class="fragment fade-up" data-fragment-index="1" -->

--- <!-- .element: data-transition="slide" data-background="#1446A0" data-background-transition="slide" -->

### System and Network Management Tier <!-- .element: style="color:#fff;" -->

___

## Nagios <!-- .element: style="color:rgba(20,70,160,.8);" -->

* comprehensive monitoring tool <!-- .element: class="fragment fade-up" data-fragment-index="1" -->
* centralized visibility and, escalation awareness capabilities <!-- .element: class="fragment fade-up" data-fragment-index="1" -->
* Time-tested, reliable, stable, extendable and, proven architecture <!-- .element: class="fragment fade-up" data-fragment-index="1" -->

___

## NetXMS <!-- .element: style="color:rgba(20,70,160,.8);" -->

* Unified platform for management and monitoring of the entire IT infrastructure <!-- .element: class="fragment fade-up" data-fragment-index="1" -->
* Designed for maximum performance and scalability <!-- .element: class="fragment fade-up" data-fragment-index="1" -->
* Distributed network monitoring and automated network discovery <!-- .element: class="fragment fade-up" data-fragment-index="1" -->
* Flexible and easy to use event processing <!-- .element: class="fragment fade-up" data-fragment-index="1" -->

___

## Pandora FMS <!-- .element: style="color:rgba(20,70,160,.8);" -->

* On premise monitoring system <!-- .element: class="fragment fade-up" data-fragment-index="1" -->
* Monitors: Network, Server, UX, APM, Inventory, SLA, IOT, Logs collection, Business activity, Remote control and, more &middot;&middot;&middot; <!-- .element: class="fragment fade-up" data-fragment-index="1" -->
* Community development. But, has a payment model for enhanced features <!-- .element: class="fragment fade-up" data-fragment-index="1" -->

___

## Cacti <!-- .element: style="color:rgba(20,70,160,.8);" -->

* complete RRDtool-based graphing solution <!-- .element: class="fragment fade-up" data-fragment-index="1" -->
* web-based monitoring <!-- .element: class="fragment fade-up" data-fragment-index="1" -->
* fast poller, advanced graph templating, multiple data acquisition methods, and user management features out of the box <!-- .element: class="fragment fade-up" data-fragment-index="1" -->

___

## Hyperic <!-- .element: style="color:rgba(20,70,160,.8);" -->

* application monitoring and, performance and availabilty management of a broad range of OS, middleware and, applications running on physical, virtual and, cloud environments <!-- .element: class="fragment fade-up" data-fragment-index="1" -->
* developed by VMware <!-- .element: class="fragment fade-up" data-fragment-index="1" -->

---

## presentation.EOF(1);

<small>_In the spirit of Open Source, this presentation is brought to you with [Reveal.js](https://github.com/hakimel/reveal.js/)_<sup style="font-size: .4em">[MIT](https://opensource.org/licenses/MIT "MIT License")</sup></small><br/>
<small>&hearts; _continuously deployed from [Github](https://github.com/siddhantrimal/remember) with free stock photos from [Plexels.com](https://www.pexels.com)_<sup style="font-size: .4em">[CC0](https://creativecommons.org/share-your-work/public-domain/cc0/ "Creative Commons 0")</sup></small>
