
Q: 
I am building a website through VScode on html and css, I am using a video tutorial to guide me. This is the video: 
https://www.youtube.com/watch?v=lBfshkPlMW8&t=245s
I am on 16:30 on the video and I have been using it step by step. We are now making a side navigation bar and it should look like this: (the first photo attached) 
However, mine looks like this: (second photo attached) 
This is my code on html: 
```
<div id="sideNav">
            <nav>
                <ul>
                    <li><a href="#">HOME</a></li>
                    <li><a href="#">FEATURES</a></li>
                    <li><a href="#">SERVICES</a></li>
                    <li><a href="#">TESTIMONIALS</a></li>
                    <li><a href="#">MEET US</a></li>
                </ul>
            </nav>

        </div>
```
And this is my css:
```
#sideNav{
    width: 120px;
    height: 100px;
    position: fixed;
    right: 0;
    top: 0;
    background: #009688;
    z-index: 2;

}
```
Can you explain to me why my side Navigation bar does not look the same as in the videos, and can you provide me with a code that will create my wishes side Navigation bar for me to copy and paste . 

A-G4-1:
From your description and the code you've provided, there could be several reasons why your side navigation bar does not look the same as in the tutorial video:

1. **CSS for `ul` and `li` elements**: The tutorial might have included specific styles for the `ul` and `li` elements inside the `nav` that you might have missed. These styles would control the list formatting, such as removing bullet points, setting the padding and margin to 0, or changing the list items to display as block elements.

2. **CSS for `a` elements**: The anchor (`a`) elements within the list might have specific styles applied to them in the tutorial, such as text color, text-decoration (to remove underlines), and padding for clickable area expansion.

3. **Width and Height**: The width and height you have set for `#sideNav` might be different from what's used in the tutorial. `height: 100vh;` would make the sidebar extend the full height of the viewport, which is a common style for side navigation bars.

4. **Additional Styles**: There might be additional styles such as `font-family`, `font-size`, `text-align`, and `line-height` that have been applied to the text or to the navigation bar itself to make it look a certain way.

To assist you further, here is a sample code that might help you get the desired look based on standard practices for side navigation bars. You may need to adjust some values to match exactly what's shown in the video.

```css
#sideNav {
    width: 200px; /* Adjust the width as necessary */
    height: 100vh; /* Full height of the viewport */
    position: fixed;
    left: 0; /* For a sidebar on the left side */
    top: 0;
    background: #009688;
    z-index: 2;
    padding-top: 20px; /* Space from the top */
}

#sideNav nav ul {
    list-style-type: none; /* Remove bullet points */
    padding: 0;
    margin: 0;
}

#sideNav nav ul li {
    padding: 10px; /* Space around the text */
}

#sideNav nav ul li a {
    text-decoration: none; /* Remove underlines from links */
    color: white; /* Text color */
    display: block; /* Make the links fill the li */
    transition: 0.3s; /* Smooth transition for hover effects */
}

#sideNav nav ul li a:hover {
    background-color: #00aba9; /* Hover background color */
}
```

Please check the tutorial video again to ensure that you've included all the necessary CSS. If you still face issues, you might want to cross-reference with the exact timestamp in the video to see if there are additional styles that you may have missed.