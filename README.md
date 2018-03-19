# js-dom-filter
allows filtering of DOM elements based on URI anchor name

The following script will hide elements in the selector following the first '#' in the URL (after 'url-decoding' the anchor name):

Samples can be seen here: https://khs-projects.github.io/js-dom-filter/sample.html

```
jQuery(function(){
  var anchorOfUrl =
        (window.location.href.split('#').length<2)
        ? "" :
        decodeURIComponent(
          window.location.href.split('#')[window.location.href.split('#').length-1]
        );
  jQuery(''+anchorOfUrl).slideUp();
});

```
