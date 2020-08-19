# Read13

Cookies were invented early in the web’s history, and indeed they can be used for persistent local storage of small amounts of data.
#### three potentially dealbreaking downsides:
- Cookies are included with every HTTP request, thereby slowing down your web application by needlessly transmitting the same data over and over.
- Cookies are included with every HTTP request, thereby sending data unencrypted over the internet (unless your entire web application is served over SSL).
- Cookies are limited to about 4 KB of data — enough to slow down your application (see above), but not enough to be terribly useful.
#### HTML5 Storage
a way for web pages to store named key/value pairs locally, within the client web browser. Like cookies, this data persists even after you navigate away from the web site, close your browser tab, exit your browser, or what have you. Unlike cookies, this data is never transmitted to the remote web server (unless you go out of your way to send it manually).
![NodeTree](Images/13.1.JPG)
