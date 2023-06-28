CVE-2023-XXXXXX

Author: Charles Heidbreder
Software: TWProxy Trialworks
Version: Trialworks v11.4
Patch Level: n/a
Vulnerability: DOM-based XSS

Description: The TWProxy Trialworks Software is vulnerable to a DOM-based XSS attack. A DOM-based XSS attack when a user sneds an executed payload to the host and a result, it modifies the DOM environment in the victim's browsers from the original client-side script This attack was found manually searhcing burp requests, running tested parameters through a XSS finder tool called Dalfox, then verifying the DOM of the affected host to view the bheaivor of the application.

Impact: An attacker can insert malciious code within the application DOM. This code can be excuted causing the application to run client code unexpectedly. For testing purposes, the impact showed a payload consisting of a basic alert being called within the DOM inspection from the "src" JavaScript functions. Then after sending the payload, the tester couls see within the DOM itself that break of the "value" html value and then. theJavaScript function itself. Additionally, an attaker could upload a reflected XSS payload into the search parameter and pull information from the website via the reflected payload.

Recommendation: To prevent XSS, you must sanatize all untrusted data, even if. itis only used in client-side scripts. If you must use user input on your page, always use it to test context, never as HTML tags or any other potential code. If you can, entirely avoid using user input, especially if it affects DOM elements. 

Reproduction steps:

![DOM-XSS](https://github.com/HeidiSecurities/CVEs/assets/105435056/60ce1781-1ee6-4767-b3f4-c70f5613429f)

![Request](https://github.com/HeidiSecurities/CVEs/assets/105435056/b3efc211-a95c-47b5-adde-6068debb2d90)

![Response](https://github.com/HeidiSecurities/CVEs/assets/105435056/9fb695f6-baff-4ca5-8532-02fc64b63a77)

![DOM_Collaborator](https://github.com/HeidiSecurities/CVEs/assets/105435056/39b0b8bf-aa5e-44c1-bf80-2367efd4da97)
