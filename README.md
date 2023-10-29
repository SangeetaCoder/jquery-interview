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
