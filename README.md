# Slick-SliderVertical version BACC responsive

[1]: <https://github.com/Baccara123/Slick-SliderVertical>

#### Demo

[http://kenwheeler.github.io/slick](http://kenwheeler.github.io/slick/)

#### CDN

To start working with Slick right away, there's a couple of CDN choices availabile
to serve the files as close, and fast as possible to your users:

- https://cdnjs.com/libraries/slick-carousel
- https://www.jsdelivr.com/projects/jquery.slick


Version vertical BACC
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
