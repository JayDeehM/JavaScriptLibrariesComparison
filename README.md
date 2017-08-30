# JavaScript

History
- JavaScript is a programming language developed in May 1995 and was formerly known as Mocha, and Live script on September 1995. JavaScript's name was permanently changed on the month of December of the same year. 

Function
- JavaScript functions as a controller for the programmer to manipulate web page elements and for it to be dynamic.


### Javascript Libraries
JavaScript Library is a collection of pre-written JavaScript whis gives the programmer an easier way of using Javascript.

### 3 commonly used libraries

#### 1. JQUERY 

![alt text](https://upload.wikimedia.org/wikipedia/en/thumb/9/9e/JQuery_logo.svg/1280px-JQuery_logo.svg.png)

Example code for fade-in:
```javascript
$(el).fadeIn();
```


##### 2. ANGULAR

![alt text](https://upload.wikimedia.org/wikipedia/commons/thumb/c/ca/AngularJS_logo.svg/800px-AngularJS_logo.svg.png)

Example code for fade-in:
```html
<div ng-controller="animationsCtrl">
            <button ng-click="fadeAnimation = !fadeAnimation">Toggle fade</button>
            fadeAnimation value: {{fadeAnimation}}
            <div class="firstSampleAnimation" ng-show="fadeAnimation">
                This element appears when the fadeAnimation model is true
            </div>
        </div>
```

#### 3. REACT
![alt text](https://cdn.worldvectorlogo.com/logos/react.svg)

Example code for fade-in:
```html
<FadeIn>
  <div>Element 1</div>
  <div>Element 2</div>
  <div>Element 3</div>
  <div>Element 4</div>
  <div>Element 5</div>
  <div>Element 6</div>
</FadeIn>
```

## Native JavaScript for fade-in:
```javascript
function fadeIn(el) {
  el.style.opacity = 0;

  var last = +new Date();
  var tick = function() {
    el.style.opacity = +el.style.opacity + (new Date() - last) / 400;
    last = +new Date();

    if (+el.style.opacity < 1) {
      (window.requestAnimationFrame && requestAnimationFrame(tick)) || setTimeout(tick, 16);
    }
  };

  tick();
}

fadeIn(el);
```

### Comparison:

(Comparison will be from my own opinion alone.)

-  As a comparison of the 3 libraries, it does make the production faster and more efficient. The three would require LESS lines of code compared to the native way of using JavaScript. However for the last two libraries, the user won't have to enclose the code in a script tag (<script></script>) for it to work but instead, they just have to link the library and add it straight to the html file.

- As a conclusion, we all have our own preferences. I  believe that all three libraries are very efficient and user friendly.







