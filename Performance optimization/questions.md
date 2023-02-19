### Profiling and debugging what tools exist and how to use them?

### What should you do before starting code optimization?
* Make sure that existing code works correctly, and it's covered with tests.
* Collect metrics (Devtools profiler, Lighthouse, etc.).
* Understand what exactly slows the system down.
* Set performance goals and start working on them.

### What is obfuscation and minification? 
* Obfuscation is a process of renaming variables and functions with nonsensical names or using techniques such as code flattening, where the code is transformed into a single large function to make it more difficult to understand.
* Minification is removing unnecessary characters from code, such as whitespace, comments, and formatting.

### What to do if a website shows a white screen for several seconds after opening?
* Check network tab in Devtools, make sure that there is no big resources downloading too much time.
* Check async/defer attributes in <script /> tags.
* 

### What are pros/cons of server-side rendering?
Pros:
* Improved SEO: Search engines typically have difficulty crawling and indexing client-side rendered pages, since the content is generated dynamically by JavaScript. 
* Faster initial load time because fully rendered page is sent to the client's browser without requiring additional time for client-side rendering
* Improved performance on low-powered devices since client-side rendering can be resource-intensive, particularly on low-powered devices such as mobile phones.
* Better accessibility because content is delivered to the client as fully rendered HTML, making it more accessible to users who rely on screen readers or other assistive technology.
Cons:
* Increased server load: Server-side rendering puts more strain on the server, as it has to render and serve HTML for each page request.
* Higher development complexity: Server-side rendering requires more complex development processes compared to client-side rendering.
* Slower subsequent page loads: With server-side rendering, subsequent page loads may be slower, as the client has to request the server for every new page load.

### What types of server-side rendering exist?
* Pre-rendering: web pages are generated at build time, and the pre-rendered HTML is served to the client upon request. This approach can provide fast initial load times, and is often used for static sites or sites with a small` number of pages that don't require dynamic content.
* Server-side rendering on-demand: web pages are generated on the server in response to client requests. This allows for dynamic content and interactive experiences, and can improve SEO by providing fully rendered content to search engines.
* Incremental server-side rendering: pre-rendering with on-demand rendering, allowing for fast initial load times and dynamic content. The initial page load is pre-rendered, while subsequent requests are rendered on-demand.
* Hybrid rendering: both client-side rendering (CSR) and server-side rendering (SSR). The initial page load is server-side rendered, while subsequent page loads are rendered on the client using CSR. This approach allows for fast initial load times, dynamic content, and interactivity.

### How to optimize loading of the web page?
* Minimize HTTP requests: Reducing the number of HTTP requests made by your web page can significantly improve loading times. Combine multiple CSS files into one, reduce the number of images used, and remove any unnecessary scripts or plugins.
* Optimize images: Compressing and resizing images can help reduce their file size and loading times. Use image formats such as JPEG or WebP, and reduce the size of images to the exact size needed for your web page.
* Use browser/server/db caching: caching can help reduce the number of HTTP requests made by your web page. By storing static files on the client's device or other caching layers, subsequent page loads can be significantly faster.
* Minify code: Minifying your HTML, CSS, and JavaScript can help reduce the size of files, making them quicker to download and parse. Minification removes unnecessary characters, such as comments, whitespace, and line breaks, without affecting the functionality of the code.
* Use a Content Delivery Network (CDN): A CDN can help distribute your website's content across a network of servers, reducing the distance that content needs to travel to reach the client's browser. This can help improve loading times, especially for users who are far away from your website's server.
* Optimize server-side performance: Ensure that your server is optimized to handle requests efficiently, with adequate resources and configurations such as gzip/brotli compression.
* Lazy loading: Implementing lazy loading allows for images, videos, and other media on the page to load only when they are scrolled into view, reducing the amount of content that needs to be loaded initially. Required resources can also be pre-downloaded using prefetch / preload html attributes.

### How to optimize performance of js code?
* Be aware of memory leaks, always unsubscribe timeouts, event listeners, observers, etc.
* Avoid heavy DOM manipulations, use `createDocumentFragment` method to insert large html structures.
* Use weak versions of map / set.
* Use web workers for computation consuming tasks.
* Memoize heavy calculations.
* Use requestAnimationFrame for long complicated calculations / animations.
* Minify code.

### How to optimize Angular applications?
* Use OnPush strategy.
* Use trackBy attribute to render arrays of data.


### How does event loop work in JavaScript?
JavaScript is single threaded language, to manage execution of asynchronous code such as network requests, timers, events there is a concept of event loop. The event loop consists of two main components: the call stack and the message queue.
The call stack is a stack of functions that need to be executed. When a function is complete, it is removed from the call stack.
When the call stack is empty, the event loop checks the message queue and takes the first task in the queue and adds it to the call stack, where it is executed. This process continues until the message queue is empty.

### What is the critical rendering path and how it works?
CRP is a sequence of steps that the browser takes to render a web page:
1. HTML Parsing: The browser parses the HTML and creates the Document Object Model (DOM) tree, which represents the structure of the web page.
2. CSS Parsing: The browser parses the CSS and creates the CSS Object Model (CSSOM) tree, which represents the styles and layout of the web page.
3. Render Tree Construction: The browser combines the DOM and CSSOM trees to create the render tree, which represents the final visual representation of the web page.
4. Layout: The browser determines the position and size of each element in the render tree, based on the styles and layout properties.
5. Paint: The browser paints the final render tree on the screen, using the appropriate graphics rendering engine.

To optimize the critical rendering path, it's important to minimize the number of blocking resources, such as large images or external scripts, that can slow down the initial loading of the web page. It's also important to use techniques such as minification and compression to reduce the size of the resources, and to prioritize the loading of critical resources, such as the CSS and JavaScript files that are necessary for the initial rendering of the web page.

### What is a difference between SVG and canvas, where to use each of them?
SVG is an XML-based vector image format that defines graphics using paths, shapes, text, and other geometric elements. It is resolution-independent, which means that graphics created using SVG will always look sharp and clear, regardless of the size they are displayed at. Since SVG graphics are based on vector paths, they can be scaled without losing detail and are ideal for creating graphics such as logos, icons, and illustrations. SVG is also easily manipulated using CSS and JavaScript, making it highly customizable.

Canvas, on the other hand, is a bitmap-based drawing technology that allows developers to create 2D and 3D graphics by manipulating pixels on a canvas element. Unlike SVG, which uses vector graphics, canvas uses pixel-based graphics that are created and rendered in real-time. Canvas is best suited for creating graphics that need to be animated or updated frequently, such as games, simulations, or data visualizations. However, canvas graphics are not resolution-independent, and resizing them can cause a loss of quality.

### What is a difference between web and service workers?
Web workers are designed to handle computationally-intensive tasks that would otherwise block the main thread of the web page, causing the page to become unresponsive. Web workers allow developers to run scripts in the background without blocking the main thread, improving the user experience of the web page. Web workers are limited to running code in response to events triggered by the web page, such as user input or timer events.

Service workers, on the other hand, are a type of web worker that run independently of the web page and can intercept network requests made by the web page. This allows them to perform tasks such as caching resources, managing offline data, and handling push notifications. Service workers can be used to create web applications that work offline, have faster load times, and can provide a more seamless user experience. Service workers are not limited to running code in response to events triggered by the web page and can be registered to respond to events that happen outside the context of the web page, such as network events.