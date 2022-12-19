# Web Developer Road Map Part 1

Hello everyone! In today's blog I want to share a practical road map I would follow if I was to start learning web development from scratch today.
Please note: I have seen a lot of materials online saying that one can learn web development within a *few weeks* and start applying for the jobs. Unfortunately or fortunately web development is a marathon and not a sprint as many articles having been say. To be a proficient web developer it takes a lot of time with determination and dedication. In this road map I will try to be very brief and direct to the point with actionable steps from A to Z. I will as well share relevant learning materials where possible. Let's begin the journey:

## How does the internet work?


![image.png](https://cdn.hashnode.com/res/hashnode/image/upload/v1669467295333/4jjZdI4P7.png align="left")

Internet is the large system of connected computers around the world that allows people to share information and communicate with each other.
The internet is a worldwide computer network that transmits a variety of data and media across interconnected devices. It works by using a packet routing network that follows **Internet Protocol (IP)** and **Transport Control Protocol (TCP)** .

TCP and IP work together to ensure that data transmission across the internet is consistent and reliable, no matter which device you’re using or where you’re using it.
When data is transferred over the internet, it’s delivered in messages and packets. Data sent over the internet is called a message, but before messages get sent, they’re broken up into tinier parts called **packets**.
These messages and packets travel from one source to the next using Internet Protocol (IP) and Transport Control Protocol (TCP). IP is a system of rules that govern how information is sent from one computer to another computer over an internet connection.
Using a numerical address (IP Address) the IP system receives further instructions on how the data should be transferred.
The Transport Control Protocol (TCP) works with IP to ensure transfer of data is dependable and reliable. This helps to make sure that no packets are lost, packets are reassembled in proper sequence, and there’s no delay negatively affecting the data quality.
Wondering how the internet works from browser launch to search results? Let’s go over the process step-by-step.
**WHEN YOU TYPE IN A WEB ADDRESS INTO YOUR BROWSER...**

**Step 1:** 

Your PC or device is connected to the web through a modem or router. Together, these devices allow you to connect to other networks around the globe. Your router enables multiple computers to join the same network while a modem connects to your ISP (Internet Service Provider) which provides you with either cable or DSL internet.

**Step 2:** 

Type in a web address, known as a URL (Uniform Resource Locator). Each website has its own unique URL that signals to your ISP where you want to go.

**Step 3:** 

Your query is pushed to your ISP which connects to several servers which store and send data like a NAP Server (Network Access Protection) and a DNS (Domain Name Server). Next, your browser looks up the IP address for the domain name you typed into your search engine through DNS. DNS then translates the text-based domain name you type into the browser into the number-based IP address.
Example: Google.com becomes 64.233.191.255

**Step 4: **

Your browser sends a Hypertext Transfer Protocol (HTTP) request to the target server to send a copy of the website to the client using TCP/IP.

  **Step 5: **

The server then approves request and sends a “200 OK” message to your computer. Then, the server sends website files to the browser in the form of data packets.

**Step 6:** 

As your browser reassembles the data packets, the website loads allowing you to learn, shop, browse, and engage.

**Step 7:** 

Enjoy your search results!

For more information you can have a look at this [Link from the hp website](https://www.hp.com/us-en/shop/tech-takes/how-does-the-internet-work#:~:text=It%20works%20by%20using%20a,where%20you're%20using%20it.)

I have also included a video tutorial that is more visual and engaging.  [youtube](https://youtu.be/x3c1ih2NJEg)

## HTML

![image.png](https://cdn.hashnode.com/res/hashnode/image/upload/v1669464810156/ICbtH0dGN.png align="left")
HTML stands for Hypertext Markup Language it is used for creating web pages. HTML creates the basic web page content link paragraphs, headings, lists, images etc.
The basic html document contains an opening and a closing **html **tags, opening and closing **head** tags, opening and closing **title** tags and opening and closing **body** tags as shown below.


![code.png](https://cdn.hashnode.com/res/hashnode/image/upload/v1669231246835/qpOdVRZOz.png align="left")

For learning HTML the following materials comes in very hardy.
> [freeCodeCamp New Responsive Web Design](https://www.freecodecamp.org/learn/2022/responsive-web-design/)

> [HTML Tutorial](https://www.w3schools.com/html/default.asp)

> [HTML & CSS Full Course - Beginner to Pro (2022)](https://youtu.be/G3e-cpL7ofc)

## CSS

![image.png](https://cdn.hashnode.com/res/hashnode/image/upload/v1669464908896/B7YoTnqwQ.png align="left")
CSS (Cascading Style Sheets) is used to style and layout web pages — for example, to alter the font, color, size, and spacing of your content, split it into multiple columns, or add animations and other decorative features.

### CSS syntax

![image.png](https://cdn.hashnode.com/res/hashnode/image/upload/v1669465304953/842IqIuvh.png align="left")
The selector points to the HTML element you want to style.

The declaration block contains one or more declarations separated by semicolons.

Each declaration includes a CSS property name and a value, separated by a colon.

Multiple CSS declarations are separated with semicolons, and declaration blocks are surrounded by curly braces.
#### Difference between HTML and CSS in a picture
HTML dictates the structure and the content of a web page while CSS modifies the design and display of HTML elements.

![image.png](https://cdn.hashnode.com/res/hashnode/image/upload/v1669465695952/MkfLKjkJr.png align="left")
The following materials can be used when learning CSS:
> [w3school](https://www.w3schools.com/css/default.asp)

> [web.dev from google](https://web.dev/learn/css/)

> [Learn to style HTML using CSS](https://developer.mozilla.org/en-US/docs/Learn/CSS)

> [CSS Full Course for Beginners | Complete All-in-One Tutorial | 11 Hours](https://youtu.be/n4R2E7O-Ngo)

> [CSS Tutorial - Zero to Hero (Complete Course)](https://youtu.be/1Rs2ND1ryYc)

> [CSS Masterclass - Tutorial & Course for Beginners](https://youtu.be/FqmB-Zj2-PA)

That's all for the first part until next time continue hacking!

*Quote of the week:* **"In some ways, programming is like painting. You start with a blank canvas and certain basic raw materials. You use a combination of science, art, and craft to determine what to do with them."** - Andrew Hunt



