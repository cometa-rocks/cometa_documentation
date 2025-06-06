# Security Feature Guide

<picture>
  <source media="(prefers-color-scheme: dark)" srcset="https://raw.githubusercontent.com/cometa-rocks/cometa_documentation/main/img/logos/COMETAROCKS_LogoEslog_Y_W.png">
  <source media="(prefers-color-scheme: light)" srcset="https://raw.githubusercontent.com/cometa-rocks/cometa_documentation/main/img/logos/COMETAROCKS_LogoEslog_Y_B.png">
  <img alt="Shows a black logo in light color mode and a white one in dark color mode." src="https://raw.githubusercontent.com/cometa-rocks/cometa_documentation/main/img/logos/COMETAROCKS_LogoEslog_Y_B.png">
</picture>

## Detailed Information

Exposing detailed information about the server, backend technologies, or other components running on the web server can pose a security risk. This information is often referred to as "server headers" or "HTTP response headers". It includes details such as the web server software, server version, programming language, and other technologies in use.

If information about the server's application reveals the presence of vulnerabilities such as XSS, CSRF, DDoS, or others, it increases the risk of malicious activities. Attackers armed with this knowledge could exploit the identified vulnerabilities, potentially leading to harmful consequences.

For a better understanding of HTTP response headers vulnerabilities, please refer [X-Powered-By](https://www.zaproxy.org/docs/alerts/10037/), [Server](https://www.zaproxy.org/docs/alerts/10036-2) and [HTTP response headers cheet sheets](https://cheatsheetseries.owasp.org/cheatsheets/HTTP_Headers_Cheat_Sheet.html#server). 

### The Cometa has introduced the feature
During feature execution, Cometa records and validates network response headers filters the ones exposing sensitive information, and displays the count in real time. After execution, users can check the step report for details on vulnerable headers and network responses, aiding in understanding.

The network Response list item contains 2 sections:

1. [Vulnerable Headers List](#vulnerable-headers-list)
2. [Network Response](#network-response)

#### Vulnerable Headers List
The list presents vulnerable headers and their values in a JSON key-value pair format.

#### Network Response
The network response refers to the data returned by a server in response to an HTTP request made by a client. It includes various pieces of information, which can be analyzed by referring to network responses.

* **URL** Indicates the endpoint that was requested, providing information about the resource accessed.
* **Status Code** Indicates the success, failure, or other conditions of the request (e.g., 200 for success, 404 for not found, 500 for server error).
* **Headers** Metadata associated with the response, including content type, content length, caching directives, and more.
* **Cookies** Information set by the server in cookies, which can be used for tracking, session management, or other purposes.
* **Redirects** If the response is a redirection, you can get the URL to which it redirects and the type of redirection (e.g., 301 for permanent, 302 for temporary).
* **Timing Information** Details about how long it took for the server to respond (e.g., latency, time to first byte).

### Activate Security Feature in Cometa
When creating a feature in Cometa, the Information section includes an option to enable the Network Logging feature, allowing users to enable or disable this security functionality.

> **Note:** Enabling this checkbox will record all your network response headers and store them in the database, potentially increasing the data load. Therefore, if the feature is not in use, please kindly consider disabling the checkbox.   

<img src="https://raw.githubusercontent.com/cometa-rocks/cometa_documentation/main/img/feature_screens/information_section.jpg" alt="Information Section" style="display: block; max-width: 800px;">

### Refer To Report
Cometa will display a list of network responses within the step report. This list will show which network responses were received during each step. Specifically, if a step takes 2 seconds to execute, any network responses received during those 2 seconds will be stored alongside the step.

In the OPTIONS section of the Step Report, you should find the following icon.

> **Note:** In case of vulnerabilities, a red indicator will be shown; otherwise, the color will be gray.

1. This indicates that the network header has been recorded and does have vulnerabilities.

    <img width="300px" src="https://raw.githubusercontent.com/cometa-rocks/cometa_documentation/main/img/feature_screens/vulnerability_Indicator.jpg">
    <br><br>
1. This indicates that the network header has been recorded and does not have vulnerabilities.

    <img width="300px" src="https://raw.githubusercontent.com/cometa-rocks/cometa_documentation/main/img/feature_screens/logging_Indicator.jpg">
    <br><br>
1. Click on the icon shown above to view the list of responses.

     <img width="800px" src="https://raw.githubusercontent.com/cometa-rocks/cometa_documentation/main/img/feature_screens/JQ_Screen.jpg">

4. The JSON data can be analyzed using JQ patterns. Please refer [JQ Documentation](https://jqlang.github.io/jq/manual/) to learn about patterns.

## Need Help?

### Where can I get help?
- Join our [Discord community](https://discord.gg/PUxt5bsRej)
- Contact us at [tec_dev@cometa.rocks](mailto:tec_dev@cometa.rocks)

Happy testing! 🚀 