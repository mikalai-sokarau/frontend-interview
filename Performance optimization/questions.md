### What is performance in scope of web applications?
Performance refers to how efficiently and effectively the application is able to deliver its intended functionality to its users.

### What metrics to measure web performance do you know?
1. Core Web Vitals are a set of metrics introduced by Google to measure and improve user experience on the web. The Core Web Vitals consist of three specific page speed and user interaction measurements that are critical to delivering a quality user experience:
    * Largest Contentful Paint (LCP): This metric measures loading performance, specifically the time it takes for the largest content element (such as an image or video) to load and become visible within the user's viewport. To provide a good user experience, LCP should occur within 2.5 seconds of when the page first starts loading.
    * First Input Delay (FID): This metric measures interactivity and responsiveness, specifically the time between a user's first interaction (such as clicking a button) and the time it takes for the application to respond. To provide a good user experience, pages should have a FID of 100 milliseconds or less.
    * Cumulative Layout Shift (CLS): This metric measures visual stability, specifically the amount of unexpected layout shift that occurs during page loading. To provide a good user experience, pages should maintain a CLS of 0.1 or less.
2. RAIL is a performance model, RAIL stands for Response, Animation, Idle, and Load, representing different aspects of user interaction with a web page. Currently, Core Web Vitals is preferred over RAIL.
    * Response: This refers to the ability of a web page to respond quickly to user input, 100ms is a good response time.
    * Animation: This refers to the ability of a web page to render animations smoothly, 60fps is a good animation rate, 10ms is a good frame budget.
    * Idle: This refers to the ability of a web page to maintain a consistent frame rate during idle time, 50ms or less is good time.
    * Load: This refers to the ability of a web page to load quickly and efficiently, under 2 seconds is a good load time.
3. First Contentful Paint (FCP): the time it takes for the first content element of a web page to be rendered on the user's screen, 0–2 seconds is good.
4. Time to First Byte (TTFB): The amount of time it takes for a user's browser to receive the first byte of data from a web server.
5. Time to Interactive (TTI): The time it takes for a web page to become fully interactive for a user. Good result is 4 seconds or less.
6. Page Size: The size of the web page, including all images, scripts, and other resources.
7. Number of HTTP Requests: The number of requests made to a server to load a page.\
...and many others.

### How can we understand that performance of the application is low?
* Collect metrics and compare current values with previous to understand if the application is starting behave worse.
* To stick to the performance NFR requirements.
* To track response times, page load, resource usage, throughput, errors and users complains, all of it can be a signal of low performance.
* Users feedback.

### What should you do before starting code optimization?
* Make sure that existing code works correctly, and it's covered with tests.
* Collect metrics (Devtools profiler, Lighthouse, etc.).
* Understand what exactly slows the system down.
* Set performance goals and start working on them.
* Document results.

### What is obfuscation and minification? 
* Obfuscation is a process of renaming variables and functions with nonsensical names or using techniques such as code flattening, where the code is transformed into a single large function to make it more difficult to understand.
* Minification is removing unnecessary characters from code, such as whitespace, comments, and formatting.

### What to do if a website shows a white screen for several seconds after opening?
0. Check for errors: Inspect the browser console for any error messages or warnings that could provide insights into the problem. Look for JavaScript errors, failed network requests, or any other relevant information that could help identify the cause.

1. Analyze the website's performance: Use performance analysis tools, such as browser developer tools or performance profiling tools, to identify potential bottlenecks and areas of improvement in terms of loading and rendering speed.

2. Optimize the code and assets: Review the website's codebase, including HTML, CSS, and JavaScript, to ensure it is clean, efficient, and properly optimized. Minify and compress your code, optimize images and other assets, and consider using techniques like lazy loading, caching or asynchronous loading for improved performance.

3. Review network requests: Examine the network requests made by the website during the initial loading phase. Identify any unnecessary requests or slow-loading resources, and optimize or eliminate them if possible. Consider using techniques like caching or content delivery networks (CDNs) to improve loading speed.

4. Prioritize critical content: Ensure that the essential content of the website is loaded and displayed quickly. Load critical CSS and JavaScript inline or asynchronously to speed up the initial rendering. This can prevent the white screen from appearing while the page fully loads.

5. Implement loading indicators: Show a loading indicator or progress bar during the initial loading process to give users a visual cue that the website is still loading. This can help manage their expectations and reduce frustration.

6. Test across different devices and networks: Verify that the slow loading issue is not specific to a particular device or network. Test the website on different browsers, devices, and network conditions to identify any platform-specific issues or performance discrepancies.

### How to optimize performance of js code?
* Be aware of memory leaks, always unsubscribe timeouts, event listeners, observers, etc.
* Avoid heavy DOM manipulations, use `createDocumentFragment` method to insert large html structures.
* Use weak versions of map / set.
* Use web workers for computation consuming tasks.
* Memoize heavy calculations.
* Use requestAnimationFrame for long complicated calculations / animations.
* Minify code.

### What are the pros and cons of using server side rendering?
Pros:
1. Better SEO: Server-side rendering enables search engines to easily crawl and index the website, leading to better SEO performance.
2. Faster Initial Load Time: Server-side rendering can send pre-rendered HTML to the browser, resulting in a faster initial load time.
3. Better Accessibility: Server-side rendering can improve accessibility since it allows the browser to display content before JavaScript is fully loaded.
4. Better Performance on Low-Powered Devices: Server-side rendering can improve performance on low-powered devices since it reduces the amount of client-side processing required.
5. Improved Security: Server-side rendering can reduce the risk of XSS attacks by rendering content on the server before sending it to the client.

Cons:
1. Higher Server Load: Server-side rendering can put a higher load on the server since the server has to render each page before sending it to the client.
2. More Complex Development: Server-side rendering requires more complex development, including setting up a server and dealing with issues related to server-side rendering.
3. Slower Subsequent Page Loads: While server-side rendering can improve initial load times, subsequent page loads can be slower since the server has to render each page before sending it to the client.

### What types of server-side rendering exist?
* Static SSR: the server generates the HTML content for each page during the build process or on-demand, and the resulting HTML is then sent to the client.
* Dynamic SSR: the server generates the HTML content on the server in response to each client request. 
* Hybrid SSR: both static and dynamic SSR used to some extent.

### How to optimize loading of the web page?
* Minimize HTTP requests: Reducing the number of HTTP requests made by your web page can significantly improve loading times. Combine multiple CSS files into one, reduce the number of images used, and remove any unnecessary scripts or plugins.
* Optimize images: Compressing and resizing images can help reduce their file size and loading times. Use image formats such as JPEG or WebP, and reduce the size of images to the exact size needed for your web page.
* Use browser/server/db caching: caching can help reduce the number of HTTP requests made by your web page. By storing static files on the client's device or other caching layers, subsequent page loads can be significantly faster.
* Minify code: Minifying your HTML, CSS, and JavaScript can help reduce the size of files, making them quicker to download and parse. Minification removes unnecessary characters, such as comments, whitespace, and line breaks, without affecting the functionality of the code.
* Use a Content Delivery Network (CDN): A CDN can help distribute your website's content across a network of servers, reducing the distance that content needs to travel to reach the client's browser. This can help improve loading times, especially for users who are far away from your website's server.
* Optimize server-side performance: Ensure that your server is optimized to handle requests efficiently, with adequate resources and configurations such as gzip/brotli compression.
* Lazy loading: Implementing lazy loading allows for images, videos, and other media on the page to load only when they are scrolled into view, reducing the amount of content that needs to be loaded initially. Required resources can also be pre-downloaded using prefetch / preload html attributes.

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

### Is there a difference between repaint and reflow process?
Reflow (or layout) refers to the process of calculating the size and position of elements on a web page, based on the content, styles, and layout rules defined in the HTML and CSS. Reflow is triggered whenever a change is made to the layout of the page, such as adding or removing an element, changing the width or height of an element, or changing the font size. Reflow is a more expensive process than repaint because it requires the browser to recalculate the position and size of all affected elements, and may cause the entire page to be redrawn.

Repaint, on the other hand, refers to the process of updating the pixels on the screen to reflect changes in the appearance of the elements on the web page. Repaint is triggered whenever a change is made to the visual style of an element, such as changing its background color or border style. Repaint is less expensive than reflow because it does not require the browser to recalculate the layout of the page, but may still require a significant amount of processing power if the affected area is large.

### What process is more expensive repaint or reflow?
Reflow is generally considered to be a more expensive process than repaint. This is because reflow involves recalculating the layout of the entire page, which can be a time-consuming task, especially if the page contains a large number of elements or complex layout rules. In contrast, repaint involves updating the pixels on the screen to reflect changes in the appearance of elements, which is a relatively lightweight process.

Reflow can be triggered by many actions that change the layout of the page, such as changing the size or position of an element, changing the font size, or modifying the content of the page. Repaint is triggered by changes in the appearance of elements, such as changes to color, borders, or background images.

### What is a difference between web and service workers?
Web workers are designed to handle computationally-intensive tasks that would otherwise block the main thread of the web page, causing the page to become unresponsive. Web workers allow developers to run scripts in the background without blocking the main thread, improving the user experience of the web page. Web workers are limited to running code in response to events triggered by the web page, such as user input or timer events.

Service workers, on the other hand, are a type of web worker that run independently of the web page and can intercept network requests made by the web page. This allows them to perform tasks such as caching resources, managing offline data, and handling push notifications. Service workers can be used to create web applications that work offline, have faster load times, and can provide a more seamless user experience. Service workers are not limited to running code in response to events triggered by the web page and can be registered to respond to events that happen outside the context of the web page, such as network events.

### How to improve performance of React applications?
1. Use React.memo or PureComponent to avoid unnecessary re-renders of components.
2. Avoid using the index as the key for list items. Instead, use a unique identifier that is consistent across renders.
3. Use the useCallback hook to memoize functions and prevent unnecessary re-renders of child components.
4. Use the useMemo hook to memoize expensive computations and prevent them from being recalculated unnecessarily.
5. Use lazy loading and code splitting to reduce the initial bundle size and improve performance.
6. Use a production build of React to reduce the size of the application.
7. Use the Chrome DevTools to analyze and optimize the performance of your application.
8. Use the React Profiler to identify performance bottlenecks in your application.
9. Optimize images and other media to reduce their size and improve the overall performance of the application.

### How to improve performance of Angular applications?
1. Use OnPush Change Detection Strategy: By default, Angular's change detection mechanism can be slow for large applications. Using the OnPush change detection strategy can significantly improve performance by reducing the number of checks performed by Angular.
2. Use AOT (Ahead-of-Time) Compilation: AOT compilation generates compiled code during build time, resulting in faster load times and better performance.
3. Lazy Loading: Lazy loading modules only load modules when they are needed, reducing the initial load time and improving performance.
4. Tree Shaking: Tree shaking removes unused code from the application, resulting in a smaller bundle size and better performance.
5. Minimize the number of HTTP requests: Combining HTTP requests, caching data, and using CDNs can reduce the number of HTTP requests and improve application performance.
6. Use trackBy with ngFor: When iterating over a list with ngFor, using the trackBy function can help Angular to identify changes in the list and avoid unnecessary re-rendering of components.
7. Use Pure Pipes: Pure pipes are more efficient and performant than impure pipes since they are only executed when the input data changes.
8. Use the Angular CLI: The Angular CLI provides many performance optimization tools such as generating production builds, measuring bundle sizes, and providing performance reports.
9. Use the Production Mode: Enabling production mode provides additional performance optimizations such as disabling Angular's debugging features and changing the change detection strategy.
10. Profile and analyze application performance using tools such as Chrome DevTools or Angular's built-in performance profiling tools to identify performance bottlenecks and areas for improvement.
11. Angular Universal: If your application requires SEO or better performance on slow networks, consider using Angular Universal for Server-Side Rendering (SSR). This enables your application to render on the server before sending it to the client, improving initial load times and search engine discoverability.

### What are techniques to optimize and reduce bundle size on the project?
* Code Splitting: Code splitting is a technique where you split your code into smaller chunks, which are loaded on demand only when needed. This can significantly reduce the initial bundle size and improve load times. You can use tools like Webpack or Rollup to implement code splitting in your project.
* Lazy Loading: Lazy loading is a technique where you load components or modules only when they are actually needed, instead of loading them all upfront. This can be achieved using dynamic imports or lazy loading APIs provided by modern frameworks like React, Angular, or Vue.
* Tree Shaking: Tree shaking is a process of eliminating unused code from the final bundle. This is done by static analysis of the code to determine which parts are actually used and which are not. This can be achieved by using tools like Webpack along with ES6 modules, which allow for dead code elimination.
* Minification: Minification is the process of reducing the size of your code by removing unnecessary characters like whitespace, comments, and renaming variables and functions to shorter names. This can be achieved using minification plugins or tools like Terser or UglifyJS.
* Compression: Compression is the process of reducing the size of your assets by compressing them before sending them over the network. Common compression techniques include gzip, brotli, or other compression algorithms supported by web servers.
* Image Optimization: Optimizing images can greatly reduce the overall bundle size, as images are usually one of the largest assets in a web project. Techniques such as image compression, lazy loading of images, and using responsive images can help reduce the image size and improve performance.
* Externalize Dependencies: Externalizing dependencies means loading external libraries or dependencies from a CDN or other external source, instead of bundling them with your application code. This can help reduce the size of your bundle and improve caching and loading times.
* Runtime Environment: Consider the runtime environment of your application and optimize accordingly. For example, in a production environment, you can use production builds, enable server-side caching, and leverage Content Delivery Networks (CDNs) to serve static assets efficiently.
* Code Review and Refactoring: Regular code review and refactoring can help identify and eliminate unnecessary or redundant code, reduce duplication, and optimize performance.
