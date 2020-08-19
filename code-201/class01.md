# Read01
## Introduction 
#### How you can access the web
###### Browsers
Pepole access websites using software called __web browser__.
Popular examples : firefox, internet explorer, safari, chrome and opera.
To view a web page the user might enter a web address into their browser.
###### Web servers
When you ask your browser for a web page, the request is sent across the Internet to a special computer known as a __web server__ which hosts the website.
Web servers are special computers that are constantly connected to the Internet, and are optimized to send web pages out to people who request them.
###### Devices
There many way to accessing website as desktop computers, laptops, tablets and mobile phones. and as you know every device of this have different screen size and some of them have faster connections than others.

#### How the web works
When you visit a website, the web server hosting that site could be anywhere in the world. In order for you to find the location of the web server, your browser will first connect to a Domain Name System (DNS) server, The DNS server then tells the browser the location of the web server hosting the site.
- When you connect to the web, you do so via an Internet Service Provider (ISP). You type a domain name or web address into your browser to visit a site.
- Your computer contacts a network of servers called Domain Name System (DNS) servers. These act like phone books; they tell your computer the IP address associated with the requested domain name. An IP address is a number of up to 12 digits separated by periods / full stops. Every device connected to the web has a unique IP address; it is like the phone number for that computer.
- The unique number that the DNS server returns to your computer allows your browser to contact the web server that hosts the website you requested. A web server is a computer that is constantly connected to the web, and is set up especially to send web pages to users.
- The web server then sends the page you requested back to your web browser.
## Structure
Structure is very important in helping readers to understand the messages you are trying to convey and to navigate around the document.
#### Tags
HTML structure creates using tags is made up of characters that live inside angled brackets, each element has an opening tag and a closing tag.
Tags act like containers. They tell you something about the information that lies between their opening and closing tags.
###### A closer look at tags
Example of tage <p> is the paragraph tage:
here this is a opening tag and the closing tag like this </p> will set at the last of the paragraph.
< left angle brackets, > right-angle brackets, inside them there is a p character, in case its a closing tag we add before the character a forward slash  /.
Attributes provide additional information about the contents of an element. They appear on the opening tag of the element and are made up of two parts: a name and a value, separated by an equals sign.
Code sample : <p lang="fr">Paragraphe en Français</p> which the lang is the name of the attribute and the "fr" is the value of the attribute.

## Extra markup
###### Comments IN HTML
Comment tage <!-- --> If you want to add a comment to your code that will not be visible in the user's browser, you can add the text between these characters.
comments to your code because, no matter how familiar you are with the page at the time of writing it, when you come back to it later or if someone else needs to look at the code comments will make it much easier to understand.

###### ID Attribute
Every HTML element can carry the id attribute. It is used to uniquely identify that element from other elements on the page.
It is important that no two elements on the same page have the same value for their id attributes otherwise the value is no longer unique.
###### CLASS Attribute
Every HTML element can also carry a class attribute Sometimes, rather than uniquely identifying one element within a document, you will want a way to identify several elements as being different from the other elements on the page. 
 
###### Block elements
Some elements will always appear to start on a new line in the browser window. These are known as block elements.
Example of block elements <h1>, <p> and <li>.
###### Inline elements
Some elements will always appear to continue on the same line as their neighbouring elements. These are known as inline elements.
Examples of inline elements are \<a>, <b>, <em> and <img>.\

###### Grouping text & elements in a block
__<div>__ This element allows you to group a set of elements together in one block-level box.
###### Grouping text & elements in a inline
__<span>__ element acts like an inline equivalent of the <div> element. It is used to either:
- Contain a section of text
-  Contain a number of inline elements
###### Iframe
Is a littel window that has been cut into your page, and that window can see another page from it, an ifram created using the <ifram> element.
There are a few attributes that you will need to know to use it.
- src : this attribute specifes the URL of the page to show it in the frame.
- height : this attribute specifes the height of the iframe.
- width : this attribute specifes the width of the iframe.
###### Meta
The <meta> element lives inside the <head> element and contains information about that web page.
purposes of it such as telling search engines about your page.
The <meta> element is an empty element so it does not have a closing tag. 
###### Escape characters
Therefore, if you want these characters to appear on your page you need to use what are termed "escape" characters.
For example:
- < = &lt
- \ > \ = &gt
- & = &amp
- " = &quot
## HTML5 Layout
HTML5 introduces a new set of elements that allow you to divide up the parts of a page. The names of these elements indicate the kind of content you will find in them. 
using HTML5 layout makes the code easier to follow, search engines might place more weight on the content.
###### Header & footer
The __<header>__ and __<footer>__ elements can be used for:
- The main header or footer that appears at the top or bottom of every page on the site. ( <header> element used to contain the site name and the main navigation)
- A header or footer for an individual <article> or <section> within the page. ( <footer> element contains copyright information, along with links to the privacy policy and terms and conditions.)
###### Nav
The <nav> element is used to contain the major navigational blocks on the site such as the primary site navigation.
###### Article
The <article> element acts as a container for any section of a page that could stand alone.
The <article> elements can even be nested inside each other.
###### Aside
When the <aside> element is used inside an <article> element, it should contain information that is related to the article but not essential to its overall meaning. 
When the <aside> element is used outside of an <article> element, it acts as a container for content that is related to the entire page. 
###### Section
The <section> element groups related content together, and typically each section would have its own heading.
If you have a page with a long article, the <section> element can be used to split the article up into separate sections.
The <section> element should not be used as a wrapper for the entire page unless the page only contains one distinct piece of content.
## Process & design
Every website should be designed for the
target audience, you must ask your self some question befor start your design your web, such as :
- what the gender customer or visitor ?
- there age ?
- culture came from ?
- Frequency visits ?
- time set on it ?

And if it was B to B there is different questions, such as:
- what the purpous from the visit ?
- siz of it ?
- the budget they have ?
###### WIREFRAMES
it's not logical to start coding you site and you dont have a simple sketch shows the final interface, so start by creating a wireframe to inform and hierarchy design.

![WIREFRAME](https://www.edrawsoft.com/images/chart/wireframe.png)
###### Design navigation
Site navigation not only helps people find where they want to go, but also helps them understand what your site is about and how it is organized. 
Three principles to get good navigation.
- Concise: the navigation should be quick and easy to read. It is a good idea to try to limit the number of options in a menu to no more than eight links. 
- Clear: choose single descriptive words for each link rather than phrases,be able to predict the kind of information that they will find on the page before clicking on the link.
- Selective :The primary navigation should only reflect the sections or content of the site.
- Context :ets the user know where they are in the website at that moment.
- Interactive :Each link should be big enough to click on and the appearance of the link should change when the user hovers over each item or clicks on it. It should also be visually distinct from other content on the page.

A large site may have primary, secondary and even tertiary navigation. Primary navigation often appears across the top of the site from left to right, or down the left hand side of the page. Secondary navigation could be under the primary navigation or down the side of the page.


## The ABC of programing
Javascript allows you to make web pages more interactive by accessing and modifying the content and markup used in a web page while it being viewed in the browser.

- ACCESS CONTENT : You can use JavaScript to select any element, attribute, or text from an HTML page. 
- MODIFY CONTENT : You can use JavaScript to add elements, attributes, and text to the page, or remove them.

PROGRAM RULES  : You can specify a set of steps for the browser to follow which allows it to access or change the content of a page.

REACT TO EVENTS : You can specify that a script should run when a specific event has occurred.

###### HTML and CSS quick review
- __HTML__ elements its to describe the structure of the page, its consists of opening and closing tag, in the opening tag there is a attribute name and attribute value.
- __CSS__ elements consists from selector and seclaration which include property name and property value.

###### What is a script and how do i create one
A script is a series of instructions that a computer can follow to achieve a goal. 
A browser may use different parts of the script depending on how the user inteacts with web page.
Scripts can run different section of the code in response to the situation around them.
To write a script  you need to first state your goal and then list the tasks that need to be completed in order to achieve it. 
Start with the big picture of what you want to achieve, and break that down into smaller steps. 
- define the goal
- Design the script
- code each step

__learning any new language, you need to get to grips with the:__
- __Vocabulary: The words that computers understand__
- __Syntax: How you put those words together to create instructions computers can follow__
