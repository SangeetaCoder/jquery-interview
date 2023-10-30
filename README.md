# jquery-interview
practice
1. Define Jquery with its core features?
=> Jquery is a fast and lightweigth javascript libarary. It simplifies a lot of  tasks that consume a lot of  time and effort with standard javascript. It simplifies rapid web development Ajax interactions, event handlling, animatios, and HTLM document traversing, and manipulation.
The main core features of jquery are:
Take Down notes.
DOM manipulation - DOM elements can be easily traversed, modified.
Animations - Lots of built-in Animations.
Ajax- Assist a lot in developing responsive and feature- rich site using AJAX.
Ligthweight - About 19kb in size.
Event handling - Several events can be captured with ease with event handlers.
Cross-browser support - Works well with IE 6.0+, safari, crme and opers, firefox.

2. What are the selectors in jquery and how many types are there?
=> Selectors are used to finding the Html elements. A jquery selector is a function that makes the use of the expression to find out matching
elements from a DOM-based on any given criteria. Once we select an element , we can perform certain operations on them. Basic selectrs are :
1. Name : Selects all elements which match with the given element Name.
2. .Class : Selects all elements which match with the given class
3. #id : Selects a single element that matchs the given id.
4. Universal (*): Selecte all elements available in a DOM.
5. Attribute Selector : Select element based on its attribute value.

3. What is the basic difference between the body? onload() and document.ready function?
=> Both function differ with each other .
1. There can be more than one document.ready() function on a single page where as only one body. onload() function is allowed.
2. document.ready() function is called as soon as DOM is loaded for a page , whereas body.onload() function is called when everything gets loaded on a page including DOM , images, and resources associated with the page .    

4. What is the difference between $(this) and 'this' in jquery?
=> this is used in a traditional way but when this is used with $() then it becomes a JQuery object on which we can use the fuctions of jquery.
example : $(document).ready(function()
{
    $('#clickme').click(fucntion()
    {
        alert($(this).text());
        alert(this.innerText);
    });
});
when only this keyword is used then we can use the jquery text() function to get the text of the element, becouse it is not a jquery object. Once the this keyword is wrapped in $() then we can use the jquery function text() to get the text of the element.

5. what are the various AJAX functions in jquery ?
=> Ajax call allows the user t exchange data with a server and upadte parts of a page without reloading the ebtire page . Some of the functions of AJAX are as follow :
1. $.ajax() : It is considered to be the lowest level and basic functions. It is used to send requests. This function can be performed without a selector . 
2. $.ajaxSetup() : This function is used to define and set the options for various ajax calls . 
For example : 
$.ajaxSetup(
    {"type": "POST","url":"ajax.php","success":
    fuction(data)
    {
        $("#bar").css("background","yellow").html(data);
    }
    });   
3. Shorthand ajax methods: they comprise of simply the wrapper function that call $.ajax() with certain parameter of simply the wrapper function that call $.ajax() with certain parameters already set.
4. $getJSON() : This is a special type of shorthand function which is used to accept the url to which the requests arev sent . also, optional data and option callback functions are possible in such functions.
6. What is jquery.onConflict?
=> Jquery no.conflict is an option given by jquery to overcome the conflicts between the different js frameworks or libaries. when we use jquery no-conflict mode , we are replacing the S to a new variable and assigning to jquery some other javascript libraries. Also use the S as a function or variable name that jquery has. And in our development life, we are not at all strict to the only jquery.
example: 
jQuery.noConflict();
jQuery(document).ready(function()
{jQery("div").hide();
});
we can also use your own specific character in the place of doller($) sign in jQery.
var $j = jQery.noConflict();
$j(document).ready(function(){
    $j("div").hide();
});

7. What is the use of jquery .each() function?
=> It is a general a collection . If there are Array-like objects with a length property, they can be iterated with thier index position and value. Other objects can be iterated with key-value properties. This function , however, works differenttly from the $(selector).each() function that works on the DOM element using the selector. But both iterate over a jquery object..
example: 
$("button).click(function(){
    $("li").each(function()
    {
        alert($(this).text())
    });
});

8. what are the methods used to provide effects in jquery?
=> jQuery provides many wnderful effects, we can apply these effects, with a simple configuration. The effect may be hiding, showing, toggling, fadeout, fade in, fade to and so on toggle(), show() and hide() methods. Similarly, we can use other methods as in the fllowing:
example:
animation(params, [duration,easing,callback])
This function makes custom animations for your HTML elements.
fadeIn(speed,[callback])
This function fades in all the matched elements by adjusting their opacity and firing an optional csllback after completion.
fadeOut(speed,[callback])
This function is used to fade out all the matched elements by adjusting their opacity to 0, then setting the display to "none" and firing an optional callback after completion.
fadeTo(speed, opacity, callback)
This function fades the opacity of all the matched elements to a specified opacity and firing an optional collback after completion.
stop(clearQueue, goto end)
This function stops all the currently running animations.

9. which one is faster, document.getElementByID('txtname') ar $('#txtName).?
=> In general, using `$('#txtName')` with jQuery is likely to be faster than `document.getElementById('txtname')` in pure JavaScript. This is because jQuery is a JavaScript library that's optimized for DOM manipulation and provides various performance enhancements.

Here are a few reasons why `$('#txtName')` is usually faster:

1. **Optimized Selector Engine:** jQuery has a highly optimized selector engine that can quickly find elements by their ID or other selectors.

2. **Cross-browser Compatibility:** jQuery takes care of cross-browser inconsistencies, ensuring consistent and efficient behavior across different browsers.

3. **Caching:** When you use `$('#txtName')`, jQuery caches the result, which means it doesn't need to search the DOM again if you reuse the selection. In contrast, `document.getElementById('txtname')` would require a new search each time.

4. **Chaining:** jQuery allows you to chain multiple operations together, which can be more efficient than separate lines of code in plain JavaScript.

However, it's important to note that the performance difference between the two methods is usually negligible in most cases, especially when dealing with a small number of elements. The choice between the two should also consider factors like code readability, maintainability, and the overall use of jQuery in your project.

In modern web development, you might also consider using vanilla JavaScript (e.g., `document.querySelector('#txtName')` or `document.getElementById('txtName')`) because modern browsers have significantly improved their native DOM selection and manipulation capabilities, reducing the need for external libraries like jQuery.



10. what is the difference between $('div') and $('<div>') in jquery?
In jQuery, `$('div')` and `$('<div>')` serve different purposes and have distinct meanings:

1. `$('div')`:
   - This is a selector that searches for existing `<div>` elements in the DOM.
   - It returns a jQuery object containing all the `<div>` elements that match the selector.
   - It's used to select and manipulate existing elements in your web page.

   Example:
   ```javascript
   $('div').css('color', 'red'); // Selects all existing <div> elements and changes their text color to red.
   ```

2. `$('<div>')`:
   - This is used to create a new `<div>` element as a jQuery object.
   - It creates an HTML element that you can then manipulate or append to the DOM.
   - It's used for creating new elements dynamically.

   Example:
   ```javascript
   var newDiv = $('<div>'); // Creates a new <div> element in memory as a jQuery object.
   newDiv.text('This is a new div').appendTo('body'); // Adds the new div to the body of the document.
   ```

So, in summary, `$('div')` selects existing `<div>` elements in the DOM, while `$('<div>')` is used to create a new `<div>` element in memory, which can be manipulated and inserted into the DOM later. They have different purposes and are not interchangeable.
