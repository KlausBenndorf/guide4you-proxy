# Guide4You AJAX proxy

In short *Guide4You AJAX Proxy* is an AJAX proxy modified to fit the needs of
the *Guide4You* web application and requires PHP 5.3 or later.

You want or need more details? Here you go: 

*Guide4You* is a web application to display map data from several sources.
As such, it sometimes runs into difficulties with the same-origin policy (SOP).
The SOP is an important concept in the web application security model.
 
SOP stops scripts contained in a web page from accessing data that has a
different origin where an origin is defined as a combination of URI scheme
(e.g. *https*), hostname (e.g. *example.com*), and port number (e.g. *80*).

While in most cases this behavior is what you want, it can be a hindrance when
you need to compile map data from different sources and in principle a web
server can use response headers to allow scripts from other sites to access
data that under the SOP would be inaccessible. If however the server for some
reason does not provide such a header the only feasible way to access the data
needed is to re-route it through the server that hosts the script. This is what
an AJAX proxy is good for.

This AJAX proxy in particular is not a standalone application insofar that it
relies on Guide4You to set its configuration. However you can always use the
source and modify it to your needs. However, you better simply use the
original stand alone proxy that *Guide4You AJAX proxy* is based on:

* AJAX Cross Domain (PHP) Proxy by Iacovos Constantinou, available at
https://github.com/softius/php-cross-domain-proxy