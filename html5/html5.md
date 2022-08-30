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

### 3. Elements of HTML Meta tag
    <head>...</head>
    <link>...</link>
    <meta>
    <style>...</style>
    <title>...</title>

```
<!DOCTYPE html>
  <html lang="en">
    <head>
      <meta charset="UTF-8">
      <title> HTML Cheatsheet </title>
      <link rel="stylesheet" href="styles.css">
      <style>
        h1 {colour:green;}
        p {colour:yellow;}
      </style>
    </head>
</html>
```

### 4. HTML Elements: Sectioning the Content

    * <address>..</address>: The HTML address> element denotes that the enclosing HTML 
                            contains contact information for a person or group of people, or for a company.
    
                <address>
                Written by <a href="mailto:interviewbit@example.com">Kit Harrington</a>.<br>
                Find us at:<br>
                interviewbit.com<br>
                Mumbai<br>
                India
                </address>

    * <article>...</article>
    * <aside>...</aside>
    * 

### 5. What are some advantages of HTML5 over its previous versions?
* Multimedia Support
* JS runs in the background.
* Stores offline data using application caches and SQL DBs.
* Users can draw various shapes like squares, circles, triangles etc.
* Includes new semantic tags and form controls.

### 6. How can we include audio or video in a webpage?
    We can use <audio> and <video> tags using which we can add the audio or video directly in the webpage.

### 7. Examples of Inline and Block elements?
    Inline elements are:

    <span>      <abbr>      <input>
    <a>         <label>     <output>
    <strong>    <sub>       <q>
    <img>       <cite>      <i> 
    <button>    <script>    <select>
    <em>        <label>

    Block elements are:
    
    <header>    <footer>    <section>
    <article>   <h1><h6>    <canvas>
    <figure>    <table>     <figcaption>
    <div>       <form>      <p>
    <ul>        <ol>        <hr>
    <pre>       <video>     <blockquote>


### 8. What is the difference between 'figure' tag and 'img' tag?
The figure tag specifies the self-contained content, like diagrams, images, code snippets, etc. 

### 9. What are Semantic Elements?
Semantic elements are those which describe the particular meaning to the browser and the developer. Elements like form, table, article, figure, etc., are semantic elements.

### 10. What is the difference between meter tag and progress tag?
progress tag should be used when we want to show the completion progress of a task, whereas if we just want a scalar measurement within a known range or fraction value. Also, we can specify multiple extra attributes for meter tags like ‘form’, ‘low’, ‘high’, ‘min’, etc.

### 11. Difference between SVG and Canvas HTML5 element?
* SVG
  * vector based
  * works better with a larger surface
  * modified using CSS and scripts
  * prints at high quality with high resolution as it is highly scalable

* Canvas
  * raster based
  * works better with smaller surface
  * modified only using scripts
  * less scalable

### 12. What type of audio files can be played using HTML5?
  Supports 3 types : Mp3, WAV, Ogg

### 13. What are the significant goals of the HTML5 specification?
* Introduction of new semantic tags to better structure the web page
* Backward compatibility with older versions
* Support for different devices and platforms and forming a standard in cross browser behaviour
* Basic interactive elements without the dependency of plugins such as video tags instead of flash

### 14. Explain the concept of web storage in HTML5.
* Helps in storing some static data in the local storage
* Size limit based on different browsers
* Decreases load time and smooth UX
* Two types:
  * Local Storage: stored for each webapp on different browsers
  * Session storage: used for one session only and deletes after closing the browsers

### 15. What is Microdata in HTML5 ?
* Used for extracting data for site crawlers and search engines.
* basically a group of name-value pairs
* The groups are called items, and each name-value pair is a property.

### 16. What is new about the relationship between the header tag and h1 tags in HTML5?
* header tag specifies the header section of the webpage.
* Unlike in previous version there was one h1 element for the entire webpage, now this is the header for one section such as article or section.
* According to the HTML5 specification, each <header> element must at least have one h1 tag.

### 17. Explain new input types provided by HTML5 for forms?
New data types offered by HTML5 are:
* Date - Only select date by using type = "date"
* Week - Pick a week by using type = "week"
* Time - Only select time by using type = "time"
* Datetime - Combination of date and time by using type = "datetime"
* Color - Accepts multiple colors using type = "color"
* Email - Accepts one or more email addresses using type = "email"
* Number - Accepts a numerical value with additional checks like min and max using type = "number"
* Search - Allows searching queries by inputting text using type = "search"
* Tel - Allows different phone numbers by using type = "tel"
* Placeholder - To display a short hint in the input fields before entering a value using type = "placeholder"
* Range - Accepts a numerical value within a specific range using type = "range"
* Url - Accepts a web address using type = "url”

```html
<form>  
        <div>
            <label>Date:</label>
            <input type="date" id="date" />
            <br>
            <label>Week:</label>
            <input type="week" id="week" />
            <br>
            <label>Month:</label>
            <input type="month" id="month" />
            <br>
            <label>Time:</label>
            <input type="time" id="time" />
            <br>
            <label>Datetime:</label>
            <input type="datetime" id="datetime" />
            <br>
            <label>Datetime Local:</label>
            <input type="datetime-local" id="datetime-local" />
            <br>
            <label>Color:</label>
            <input type="color" id="color"/>
            <br>
            <label>Email:</label>
            <input type="email" id="email" placeholder="email address" />
            <br>
            <label>Number:</label>
            <input type="number" id="number" />
            <br>
            <label>Search:</label>
            <input type="search" id="search" />
            <br>
            <label>Phone:</label>
            <input type="tel" id="phone" placeholder="Phone Number" pattern="\d{10}$" />
            <br>
            <label>Range:</label>
            <input type="range" id="range" />
            <br>
            <label>URL:</label>
            <input type="url" id="url"/>
        </div>  
    </form>
```

### 18. What are the New tags in Media Elements in HTML5?
* audio - Used for sounds, audio streams, or music, embed audio content without any additional plug-in.
* video - Used for video streams, embed video content etc.
* source - Used for multiple media resources in media elements, such as audio, video, etc.
* embed -  Used for an external application or embedded content
* track - Used for subtitles in the media elements such as video or audio

```html
<label>
       Video:
   </label>
    <video width="320" height="240" controls>
        <source src="video.mp4" type="video/mp4">
        <track src="subtitles.vtt" kind="subtitles" srclang="en" label="English">
    </video>
    <br>
    <label>
        Embed:
    </label>
    <embed type="video/webm" src="https://www.youtube.com/embed/MpoE6s2psCw" width="400" height="300">
    <br>
    <label>
        Audio:
    </label>
    <audio controls>
        <source src="audio.mp3" type="audio/mpeg">
    </audio>
```

### 19. Why do you think the addition of drag-and-drop functionality in HTML5 is important? How will you make an image draggable in HTML5?
* The drag and drop functionality is a very intuitive way to select local files
* Before the native drag and drop API, this was achievable by writing complex Javascript programming or external frameworks like jQuery.
* To enable this functionality there is a draggable attribute in the <img> tag and need to set ondrop and ondragover attribute to an eventhandler available in scripts.

```html
<body>
   ...
   <div id="div1" ondrop="drop(event)" ondragover="allowDrop(event)" style="border: 1px solid #aaaaaa; width:350px; height: 70px;"></div>
   <br>
   <img id="drag1" src="img_logo.gif" draggable="true" width="336" height="69">
    ...
 </body>
```

### 20. Why do we need the MathML element in HTML5?
MathML stands for Mathematical Markup Language. It is used for displaying mathematical expressions on web pages. For this 'math' tag is used.
```html
<math>
  <mrow>
    <mrow>
      <msup>
        <mi> a </mi>
        <mn> 2 </mn>
      </msup>
      <mo> + </mo>
      <msup>
        <mi> b </mi>
        <mn> 2 </mn>
      </msup>
      <mo> + </mo>
      <mn> 2 </mn>
      <mn> a </mn>
      <mn> b </mn>
    </mrow>
    <mo> = </mo>
    <mn> 0 </mn>
  </mrow>
</math>
```

### 21. What are the server-sent events in HTML5?
* The events pushed from the webserver to the browsers are called server-sent events.
* DOM elements can be continuously updated using these events. This has a major advantage over straight-up polling.
* In polling, there is a lot of overhead since every time it is establishing an HTTP connection and tearing it down whereas, in server-sent events, there is one long-lived HTTP connection. 
* To use a server-sent event, 'eventsource' element is used. The src attribute of this element specifies the URL from which sends a data stream having the events.

```html
<eventsource src = "/cgi-bin/myfile.cgi" />
```

### 22. What are Web Workers?
* Brings parallelism and async capability. 
* runs in the background to do the computationally expensive tasks without yielding to make the page responsive.
* achieved by starting a separate thread for such tasks. These are not meant to perform UI operations. 
* Three types:
  * Dedicated Workers - These are workers that are utilized by a single script
  * Shared Workers -These are workers that are utilized by multiple scripts running in different windows, IFrames, etc
  * Service Workers - These act as proxy servers between web applications, the browser, and the network. Mostly used for push notifications and sync APIs.

```html
<p>Count numbers: <output id="result"></output></p>
<button onclick="startWorker()">Start Worker</button>
<button onclick="stopWorker()">Stop Worker</button>
<script>
var w;
function startWorker() {
if(typeof(Worker) !== "undefined") {
    if(typeof(w) == "undefined") {
        w = new Worker("demo_workers.js");
}
w.onmessage = function(event) {
        document.getElementById("result").innerHTML = event.data;
    };
  }
}

function stopWorker() {
 w.terminate();
 w = undefined;
}
</script>
```

### 23. What are raster images and vector images?
* Raster Images - The raster image is defined by the arrangement of pixels in a grid with exactly what color the pixel should be. Few raster file formats include PNG(.png), JPEG(.jpg), etc.
* Vector Images - The vector image is defined using algorithms with shape and path definitions that can be used to render the image on-screen written in a similar markup fashion. The file extension is .svg

### 24. What are different approaches to make an image responsive?
* Art direction
  * Using 'picture' element the landscape image fully shown in desktop layout can be zoomed in with the main subject in focus for a portrait layout.
```html
<picture>
 <source media="(min-width: 650px)" srcset="img_cup.jpg">
 <img src="img_marsh.jpg" style="width:auto;">
</picture>
```

* Resolution switching
  Instead of zoom and crop the images can be scaled accordingly using vector graphics. Also, this can be further optimized to serve different pixel density screens as well. 