# HTTPS-check
Show/hide HTML elements depending on whether or not the connection uses HTTPS.

The code contained in this repo is in the public domain.

--------

Occasionally, some functionality you want to include on a webpage requires HTTPS (for example, a "copy to clipboad" button that uses Javascript clipboad API). 

If the user isn't using HTTPS, sometimes I just want to hide these elements to make the page cleaner. There's where HTTPS-check comes in.

See `https-check.html` for the code.

* If the user is using HTTPS, then any elements with the class `https-no` are hidden.  
* If the user is _not_ using HTTPS, then any elements with the class `https-yes` are hidden.


----

 `v1`: `2020-10-18`


