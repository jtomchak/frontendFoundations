autoscale: true
## jQuery
* fast, small, and feature-rich JavaScript library
* makes things like HTML document traversal and manipulation, event handling, animation, and Ajax much simpler
* provides a paradigm for event handling that goes beyond basic DOM element selection and manipulation.

---

## ok, but why?
```js
function changeBachground(color) {
Document.body.style.background = color;
}

Onload=changeBackground (‘red’);
```
**OR**

```js
$ (‘body’) .css (‘background’, ‘#ccc’);
```

---

## or another
```js
var d = getElementsByClassName("yo");
for(var i=0;i<d.length;i++){
  d[i].className = d[i].className + " selected";
}
```
**OR**

```js
$(".yo").addClass("selected");
```

---
## ajax calls
* AJAX = Asynchronous JavaScript and XML.
* Loading data in the background and display it on the webpage, without reloading the whole page.
* Send data to a server - in the background, you know, like a form!

---
## ajax example
# Peasants
```js
function loadDoc() {
  var xhttp = new XMLHttpRequest();
  xhttp.onreadystatechange = function() {
    if (this.readyState == 4 && this.status == 200) {
      document.getElementById("demo").innerHTML =
      this.responseText;
    }
  };
  xhttp.open("GET", "ajax_info.txt", true);
  xhttp.send();
```

---
## ajax example
# Gong farmer
```js
$("button").click(function(){
    $.ajax({url: "demo_test.txt", success: function(result){
        $("#div1").html(result);
    }});
});
```

