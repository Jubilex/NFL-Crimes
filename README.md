# NFL-Crimes
For CS
so far you have been coding and displaying in a window on your computer or console on your computer.... 

While that is great and all for learning coding concepts, it is now how we really use computers in the real world.

Real world you usually have code running on a server out on the internet and you use a web browser to access and display information.

The browser is your console/wpf display.  

Traditionally it looks somethign like this:

server

server and user with laptop

http GET request

http HTML response

c# code runs on back end server to get data (calling pokemon api to get data) then makes the html page and sends the response.

browser displays HTML

This is how One.ou.edu works

Another way to do the same thing, some may say is better is an SPA.  

you load initial HTML into a browser and use javascript in the browser to update the html or go and get data via json.

it looks somethign like this

http GET request

server sends HTML file response with javascript code

browser displays initial html and the javascript code then goes and handles routing and getting data

This is how the new one.ou.edu will work

show browser network info on both





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
