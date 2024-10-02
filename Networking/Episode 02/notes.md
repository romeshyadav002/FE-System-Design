* `How the web works`

* `Server` :- Server is something that that can process some request and after some processing it can respond you with some data
it should be
 - reliable
 - 24 * 7 available
 - memory etc

- two device which needs to be connected through internet should have IP address ( IP is similar to PIN code in real life)

* `DNS (Domain name server)`
 - so whenever you search any website eg:- google.com than in DNS we will found the IP address of that server we want to hit
 - so first we get the IP from DNS server and now our request will go to this IP 
 - we will get our HTML, CSS, JS

* so this is how internet is connected
 - whole Internet --> ISP(Internet service Provider) eg:- BSNL --> telephone line --> Modem --> Router --> LAN/wifi --> computer/mobile

* DNS structure is governed by several companies for eg:- ICANN
 1. Root domain 
   - `.`
 2. Top level domains
   - `edu` , `org`, `gov`, `com`, `au`
 3. Second-level domains
   - `openOffice`.org , `expedia`.gov , `microsoft`.com
 4. Third-level domains 
   - `wwww`.expedia.gov , `download`.microsoft.com 

* whenever we try to search something than it will try to search in these things cache
 1. Browser(cache, Service worker)
 2. Operating system
 3. Router
 4. ISP

* `Peering` - Google developed this method in which you decrease the no. of hops(levels), that the request have to cross to get the response

* Steps occur in Network call
 1. DNS Lookup
 2. TCP Handshake - means in which it will check whether the client is ready to get the response or not
 3. SSL handshake - certificate will get exchanged in this step, basically server will send a clientKey than this key will send with each request so that i can verify that you are authorized to get the response
 4. HTTP GET Request
   - data will come in these sizes
     - 14kb than
     - 28kb than
     - 56kb so on...

* `How the web page renders`
   Rendering Flowchart
1. Request sent
2. DNS Resolution
3. Server Response (HTML)
4. Parse HTML → Build DOM
5. Request Resources (CSS, JS, Images)
6. Parse CSS → Build CSSOM
7. Parse JS → Execute
8. Create Render Tree
9. Layout (Reflow)
10. Painting
11. Compositing
12. Webpage Displayed

Web page rendering involves multiple steps, starting from a user's request to view a webpage to the final display in the browser. Here’s an overview of how this process works:

1. `URL Request`
The user enters a URL in the browser or clicks a link.
The browser sends an HTTP request to the server for the page's content.

2. `DNS Resolution`
The browser checks the URL and sends a request to a DNS (Domain Name System) server to resolve the domain name (e.g., example.com) into an IP address.

3. `Server Response`
Once the DNS resolution is complete, the browser contacts the server using the resolved IP address.
The server processes the request (e.g., for index.html) and returns the content (typically HTML, CSS, and JavaScript files).

4. `Parsing HTML and Building the DOM`
The browser starts reading the HTML document line by line.
The HTML is parsed and converted into a DOM (Document Object Model) tree.
DOM is a structured representation of the HTML elements on the page.
For example, <div>, <h1>, and <p> tags are nodes in this tree.

5.` Downloading Resources (CSS, JS, Images)`
As the browser parses the HTML, it encounters references to external resources such as CSS, JavaScript, fonts, and images.
It sends additional HTTP requests to fetch these resources.
For example:
<link rel="stylesheet" href="styles.css"> for CSS files.
<script src="script.js"></script> for JavaScript files.
These resources are requested asynchronously, meaning they are fetched in parallel to avoid blocking page rendering.

6. `Building the CSSOM`
The browser downloads and parses the CSS files to create a CSSOM (CSS Object Model).
CSSOM defines the styles for each element in the DOM.

7. `JavaScript Execution`
JavaScript files are downloaded and executed by the browser's JavaScript engine.
JavaScript can manipulate the DOM and CSSOM dynamically (e.g., for animations, form submissions, or data fetching).

8. `Rendering Tree Construction`
The browser combines the DOM and CSSOM into a render tree.
The render tree only includes the nodes that are visible on the page (e.g., nodes with display: none are excluded).
This tree determines the structure and styles of the elements that will be displayed on the screen.

9. `Layout (Reflow)`
The browser calculates the layout of each element, determining its size, position, and dimensions based on the render tree and CSS rules.
This is called reflow or layout, and it ensures all elements are positioned correctly on the page.

10. `Painting`
After layout, the browser starts painting the pixels on the screen.
It draws out the visual elements (e.g., backgrounds, text, borders) according to the calculated styles and layout.

11. `Compositing`
In the final step, the browser may split the page into multiple layers, which are drawn separately and then combined.
This is especially useful for complex animations or elements with special effects like z-index, transformations, or transparency.
The layers are composited together to form the final image that the user sees.

12. `Rendering Complete`
Once all resources have been fetched and rendered, the web page is displayed to the user.

* Key Concepts:

  - Blocking resources: CSS blocks the rendering of the page until it's fully loaded and parsed because the layout depends on CSS. JavaScript can also block if scripts are not deferred or asynchronously loaded.
    CSS - blocks rendering
    JS - blocks parser

  - Reflow: Layout recalculations triggered by DOM or CSS changes (e.g., resizing windows or modifying elements).

  - Repaint: Changes in appearance without affecting layout (e.g., color change).

  By optimizing the loading of resources (e.g., minifying files, deferring JavaScript), developers can speed up page rendering and improve user experience.