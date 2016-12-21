# Slick-SliderVertical version Baccara responsive

[1]: <https://github.com/Baccara123/Slick-SliderVertical>

#### Demo

[http://kenwheeler.github.io/slick](http://kenwheeler.github.io/slick/)

#### CDN

To start working with Slick right away, there's a couple of CDN choices availabile
to serve the files as close, and fast as possible to your users:

- https://cdnjs.com/libraries/slick-carousel
- https://www.jsdelivr.com/projects/jquery.slick

#####Example using jsDelivr

Just add a link to the css file in your `<head>`:
```html
<link rel="stylesheet" type="text/css" href="//cdn.jsdelivr.net/jquery.slick/1.6.0/slick.css"/>
<!-- Add the slick-theme.css if you want default styling -->
<link rel="stylesheet" type="text/css" href="//cdn.jsdelivr.net/jquery.slick/1.6.0/slick-theme.css"/>
```

Then, before your closing ```<body>``` tag add:

```html
<script type="text/javascript" src="//cdn.jsdelivr.net/jquery.slick/1.6.0/slick.min.js"></script>
```

#### Package Managers

```sh
# Bower
bower install --save slick-carousel

# NPM
npm install slick-carousel
```

#### Contributing

PLEASE review CONTRIBUTING.markdown prior to requesting a feature, filing a pull request or filing an issue.

### Data Attribute Settings

In slick 1.5 you can now add settings using the data-slick attribute. You still need to call $(element).slick() to initialize slick on the element.

Example:

```html
<div data-slick='{"slidesToShow": 4, "slidesToScroll": 4}'>
  <div><h3>1</h3></div>
  <div><h3>2</h3></div>
  <div><h3>3</h3></div>
  <div><h3>4</h3></div>
  <div><h3>5</h3></div>
  <div><h3>6</h3></div>
</div>
```

### Settings

Option | Type | Default | Description
------ | ---- | ------- | -----------
accessibility | boolean | true | Enables tabbing and arrow key navigation
adaptiveHeight | boolean | false | Adapts slider height to the current slide
autoplay | boolean | false | Enables auto play of slides
autoplaySpeed | int  | 3000 | Auto play change interval
centerMode | boolean | false | Enables centered view with partial prev/next slides. Use with odd numbered slidesToShow counts.
centerPadding | string | '50px' | Side padding when in center mode. (px or %)
cssEase | string |  'ease' | CSS3 easing
customPaging | function | n/a | Custom paging templates. See source for use example.
dots | boolean | false | Current slide indicator dots
dotsClass | string | 'slick-dots' | Class for slide indicator dots container
draggable | boolean | true | Enables desktop dragging
easing | string |  'linear' | animate() fallback easing
edgeFriction | integer | 0.15 | Resistance when swiping edges of non-infinite carousels
fade | boolean | false | Enables fade
arrows | boolean | true | Enable Next/Prev arrows
appendArrows | string | $(element) | Change where the navigation arrows are attached (Selector, htmlString, Array, Element, jQuery object)
appendDots | string | $(element) | Change where the navigation dots are attached (Selector, htmlString, Array, Element, jQuery object)
mobileFirst | boolean | false | Responsive settings use mobile first calculation
prevArrow | string (html \| jQuery selector) \| object (DOM node \| jQuery object) | `<button type="button" class="slick-prev">Previous</button>` | Allows you to select a node or customize the HTML for the "Previous" arrow.
nextArrow | string (html \| jQuery selector) \| object (DOM node \| jQuery object) | `<button type="button" class="slick-next">Next</button>` | Allows you to select a node or customize the HTML for the "Next" arrow.
infinite | boolean | true | Infinite looping
initialSlide | integer | 0 | Slide to start on
lazyLoad | string | 'ondemand' | Accepts 'ondemand' or 'progressive' for lazy load technique. 'ondemand' will load the image as soon as you slide to it, 'progressive' loads one image after the other when the page loads.
pauseOnFocus | boolean | true | Pauses autoplay when slider is focussed
pauseOnHover | boolean | true | Pauses autoplay on hover
pauseOnDotsHover | boolean | false | Pauses autoplay when a dot is hovered
respondTo | string | 'window' | Width that responsive object responds to. Can be 'window', 'slider' or 'min' (the smaller of the two).
responsive | array | null | Array of objects [containing breakpoints and settings objects (see example)](#responsive-option-example). Enables settings at given `breakpoint`. Set `settings` to "unslick" instead of an object to disable slick at a given breakpoint.
rows | int | 1 | Setting this to more than 1 initializes grid mode. Use slidesPerRow to set how many slides should be in each row.
slide | string | '' | Slide element query
slidesPerRow | int | 1 | With grid mode initialized via the rows option, this sets how many slides are in each grid row.
slidesToShow | int | 1 | # of slides to show at a time
slidesToScroll | int | 1 | # of slides to scroll at a time
speed | int | 300 | Transition speed

version vertical BACCARA
```javascript
var $s = $(".slider");
$s.slick({
    autoplay: false,
    autoplaySpeed: 600,
    slidesToShow: 3,
    responsive: [{ 
        breakpoint: 1000,
        settings: {
            slidesToShow: 4
        } 
    }]
});
// =============================================
//  Now lets add a bunch of unique breakpoints.
// =============================================
$s.slick("setOption", "responsive", [{
    breakpoint: 900, 
    settings: { slidesToShow: 3 }
}], true);
// =============================================
//  we shouldnt see this next one, as we overwrite it later.
// =============================================
$s.slick("setOption", "responsive", [{
    breakpoint: 500, 
    settings: { slidesToShow: 2 }
}], true);
// =============================================
//  test for adding an array of breakpoints.
// =============================================
$s.slick("setOption", "responsive", [{
    breakpoint: 800, 
    settings: { slidesToShow: 2, centerMode: true }
},{
    breakpoint: 700, 
    settings: { slidesToShow: 3, vertical: true, verticalSwiping: true }
}], true);
// =============================================
//  Below here we test adding a few duplicates.
// =============================================
$s.slick("setOption", "responsive", [{
    breakpoint: 500, 
    settings: { slidesToShow: 5 }
},{
    breakpoint: 500, 
    settings: { slidesToShow: 3, fade: true }
}], true);
```
