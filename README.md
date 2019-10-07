so far you have been coding and displaying in a window on your computer or console on your computer.... 

While that is great and all for learning coding concepts, it is now how we really use computers in the real world.

Real world you usually have code running on a server out on the internet and you use a web browser to access and display information.

The browser is your console/wpf display.  

Traditionally it looks somethign like this:

server

server and user with laptop

http GET request

c# code runs on back end server to get data (calling pokemon api to get data) then makes the html page and sends the response.

http HTML response

browser displays HTML

This is how One.ou.edu works

Another way to do the same thing, some may say is better is an SPA.  

you load initial HTML into a browser and use javascript in the browser to update the html or go and get data via json.

it looks somethign like this

http GET request

server sends HTML file response with javascript code

browser displays initial html and the javascript code then goes and handles routing and getting data (more data up front)

browser then makes GET requests to APIs to get data

server sends JSON response back with data.

This is how the new one.ou.edu will work

show browser network info on both


We will be making a standalone HTML file that we can load into the browser that fetches JSON data from a server and updates the page.


Lets talk about the browser and how it works.

When a request is made and the response is HTML, the browser starts parsing the HTMl from line 1 to end of file.  It begins building an internal data structure of the page we call the Document Object Model or DOM.  

The DOM is what we will be manipulating with javascript to change things the page displays on the fly.

Since the browser starts loading and executing the file from line 1 down, the order or placement of javascript can affect the way the page is displayed.  If you place your code at the top of the file before the HTML it will start executing that before it starts showing the HTML which could make the page seem to load slowly.  As you see with us, we have a spinner loaded initially just to show something, then after the page is loaded and API returns we display the entire page at once.  Something to keep in know/keep in mind.

Remember your console apps?   You put your code in the MAIN() which is called once the server starts running your code.  javascript will run immediately when parsed and you usually do not want that.  Instead you want to respond to events.

Just like your WPF projects where you (instead of putting code in a MAIN() to run) have code running when a button pushed it is an event.  We respond to events.  load the page and wait.  

Show code loading and cannot find element

First event is "DOMContentLoaded"  ->  This could execute like a main() and auto raised when DOM is fully parsed, built and ready to access.

other events could be mouse movement, scrolling, clicking etc.  Lots of events:  show ww3 event list (google javascripot events) and show w3schools.com DOM Events

write functions to handle the events and they are called

So, think of what you want done, then google your way through it!

Show network tab


document.getElementById("myButton").onclick = changeColor;
let x = "1";
function changeColor() {
	
  
  if (x === 1) {
	document.getElementsByClassName("myDiv")[0].style.backgroundColor = "red";
  x++;
  } else {
  	document.getElementsByClassName("myDiv")[0].style.backgroundColor = "pink";
  }
}
