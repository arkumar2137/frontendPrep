# Theoritical Questions

### 1. What is the Geolocation API in HTML5?

Geolocation API is used to share the physical location of the client with websites. This helps in serving locale-based content and a unique experience to the user,
based on their location. This works with a new property of the global navigator object and most of the modern browsers support this.


```html5
<!DOCTYPE html>
<html>
  <body>
     <p>Click "try it" button to get your coordinates.</p>
     <button onclick="getLocation()">Try It</button>
     <p id="demo"></p>
     <script>
        var x = document.getElementById("demo");
        
        function getLocation() {
          if (navigator.geolocation) {
            navigator.geolocation.getCurrentPosition(showPosition);
          } else { 
            x.innerHTML = "Geolocation functionality is not supported by this browser.";
          }
        }
        
        function showPosition(position) {
          x.innerHTML = "Latitude: " + position.coords.latitude + 
          "<br>Longitude: " + position.coords.longitude;
        }
     </script>
  </body>
</html>
```

### 2. What is a manifest file in HTML5?
lists down resources that can be cached to make the web page load faster
There are 3 sections in the manifest file

    CACHE Manifest - Files needs to be cached.
    Network - File never to be cached, always need a network connection.
    Fallback - Fallback files in case a page is inaccessible

    CACHE MANIFEST
    2012-06-16 v1.0.0
    /style.css
    /logo.gif
    /main.js
    
    NETWORK:
    login.php
    
    FALLBACK:
    /html/ /offline.html

```html
<!DOCTYPE HTML>
<html manifest="tutorial.appcache">
...
...
</html>

```