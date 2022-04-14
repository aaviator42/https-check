# HTTPS-check
Show/hide HTML elements depending on whether or not the connection uses HTTPS.

The code contained in this repo is in the public domain.

--------

Occasionally, some functionality you want to include on a webpage requires HTTPS (for example, a "copy to clipboard" button that uses the Javascript clipboard API). 

If the user isn't using HTTPS, sometimes I just want to hide these elements to make the page cleaner. That's where HTTPS-check comes in.

See `https-check.html` for the code.

* If the user is using HTTPS, then any elements with the class `https-no` are hidden.  
* If the user is _not_ using HTTPS, then any elements with the class `https-yes` are hidden.

-----

Usage:

```html
<!-- include this in all your files where you want to use HTTPS-check! -->
<script>
window.onload = HTTPScheck();

function HTTPScheck(){
  if (location.protocol === 'https:') {
    var divsToHide = document.getElementsByClassName("https-no");
  } else {
    var divsToHide = document.getElementsByClassName("https-yes");	
  }
  for(var i = 0; i < divsToHide.length; i++){
    divsToHide[i].style.display = "none";
  }
}
</script>

<!-- the following will only show if connected through HTTP -->
<span class="https-no">
  Not connected through HTTPS.
</span>

<!-- the following will only show if connected through HTTPS -->
<span class="https-yes">
  Connected through HTTPS.
</span>
 ```

----

 `v1`: `2021-10-18`


