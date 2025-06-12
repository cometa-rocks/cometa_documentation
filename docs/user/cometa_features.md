# Co.meta Features Documentation

<picture>
  <source media="(prefers-color-scheme: dark)" srcset="https://raw.githubusercontent.com/cometa-rocks/cometa_documentation/main/img/logos/COMETAROCKS_LogoEslog_Y_W.png">
  <source media="(prefers-color-scheme: light)" srcset="https://raw.githubusercontent.com/cometa-rocks/cometa_documentation/main/img/logos/COMETAROCKS_LogoEslog_Y_B.png">
  <img alt="Shows a black logo in light color mode and a white one in dark color mode." src="https://raw.githubusercontent.com/cometa-rocks/cometa_documentation/main/img/logos/COMETAROCKS_LogoEslog_Y_B.png" style="display: block; max-width: 800px;">
</picture>

> [!TIP]
> - Use your browser's search (Ctrl+F or Cmd+F) to find specific features

## Feature List
1. [End to End Monitoring](#end-to-end-monitoring)
2. [Security Feature](#security-feature)
3. [AI Feature](#ai-feature)
4. [API Testing](#api-testing)
5. [Load Testing](#load-testing)
6. [Historical Analysis Feature](#historical-analysis-feature)
7. [Data Driven Testing](#data-driven-testing)
8. [Database Testing](#database-testing)
9. [Mobile Testing](#mobile-testing)
10. [Accessibility Testing](#accessibility-testing)
11. [Multi-Factor Authentication](#multi-factor-authentication)
12. [Email Feature](#email-feature)
13. [Telegram Notifications](#telegram-notifications)

## End to  End Monitoring

### Key Capabilities
- Real-time test execution monitoring
- WebSocket-based live updates
- Test progress visualization
- Results analysis and reporting
- Screenshot comparison
- Video recording of test execution
- PDF report generation
- Performance metrics tracking

<details>
<summary>Learn more about End-to-End Monitoring</summary>

## What is the End-to-End Monitoring Feature?
The End-to-End Monitoring Feature provides comprehensive real-time monitoring and visualization of test execution, allowing users to track test progress, analyze results, and identify issues across the entire testing pipeline.

## Key Capabilities
- Real-time test execution monitoring
- WebSocket-based live updates
- Test progress visualization
- Results analysis and reporting
- Screenshot comparison
- Video recording of test execution
- PDF report generation
- Performance metrics tracking

## Monitoring Components

### Frontend Monitoring
- Angular-based monitoring interface
- Real-time test execution status
- Step-by-step execution details
- Visual regression testing results
- Mobile emulator interface
- Test scheduling dashboard

### Backend Monitoring
- Django REST API endpoints
- WebSocket server for live updates
- Container service monitoring
- Test execution orchestration
- Data storage and retrieval
- Authentication and authorization

## Test Execution Flow

### Real-time Updates
- WebSocket-based communication
- Live test progress tracking
- Immediate result notifications
- Screenshot capture and comparison
- Video recording of test sessions

### Results Analysis
- Step-by-step execution details
- Visual regression comparisons
- Performance metrics
- Error tracking and reporting
- PDF report generation
- Test execution videos

## Monitoring Features

### Test Execution Monitoring
- Live test progress tracking
- Step-by-step execution details
- Screenshot capture and comparison
- Video recording of test sessions
- Performance metrics collection

### Results Visualization
- Interactive test result charts
- Visual regression comparisons
- Execution timing metrics
- Error tracking and reporting
- PDF report generation

### Container Monitoring
- Browser container status
- Mobile emulator status
- Resource utilization tracking
- Container health checks
- Selenoid configuration monitoring

## Integration Capabilities

### API Integration
- REST API endpoints
- WebSocket connections
- Authentication support
- Data synchronization
- Real-time updates

### Reporting Integration
- PDF report generation
- Test result exports
- Performance metrics
- Error logs
- Screenshot archives
</details>

[Back to top](#feature-list)

## Security Feature

### What is the Security Feature?
The Security Feature helps identify and validate network response headers that might expose sensitive information. It helps prevent security vulnerabilities like XSS, CSRF, and DDoS attacks.

### Key Capabilities
- Records and validates network response headers
- Filters sensitive information
- Displays vulnerability counts in real-time
- Provides detailed step reports for vulnerable headers
- Shows network responses with:
  - URL information
  - Status codes
  - Headers
  - Cookies
  - Redirects
  - Timing information

<details>
<summary>Learn more about Security Feature</summary>

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
</details>

[Back to top](#feature-list)

## AI Feature

### What is the AI Feature?
The AI Feature provides intelligent validation and object recognition capabilities for testing.

### Key Capabilities
- Automated autonomous browsing
- Screen content validation
- Object recognition
- Visible object listing
- Custom validation options
- AI-powered test automation

<details>
<summary>Learn more about AI Feature</summary>

## What is the AI Testing Feature?
The AI Testing Feature enables intelligent test automation through computer vision, natural language processing, and machine learning capabilities. This feature allows for robust visual testing, content validation, and dynamic interaction with web and mobile applications. And of course autonomous browsing.

## Key Capabilities
- Automated autonomous browsing
- Visual object detection and recognition
- Screen content analysis and validation
- Natural language processing for test instructions
- Dynamic element identification
- Intelligent test step generation
- Visual regression testing
- Automated test maintenance
- Real-time analysis and reporting

## Core Components

### Visual Analysis
- Object detection and classification
- Text extraction (OCR)
- Layout analysis
- Color and style detection
- Visual comparison
- Element positioning

### Natural Language Processing
- Test step interpretation
- Content validation
- Semantic analysis
- Multi-language support
- Context-aware processing

### Machine Learning Features
- Dynamic element locator adaptation
- Pattern recognition
- Anomaly detection
- Self-healing test scripts
- Performance optimization
</details>

[Back to top](#feature-list)

## API Testing

### What is the API Testing Feature?
Cometa provides robust API testing capabilities for validating backend services and APIs alongside UI tests.

### Key Capabilities
- RESTful API support (GET, POST, PUT, DELETE, PATCH)
- Request configuration (headers, body, authentication)
- Response validation
- JSON schema validation
- Data extraction from responses
- Request chaining
- API call editor with visual interface

<details>
<summary>Learn more about API Testing</summary>

## What is API Testing?
API Testing is a type of software testing that involves testing application programming interfaces (APIs) directly and as part of integration testing to determine if they meet expectations for functionality, reliability, performance, and security.

## Key Capabilities
- RESTful API support (GET, POST, PUT, DELETE, PATCH)
- Request configuration (headers, body, authentication)
- Response validation
- JSON schema validation
- Data extraction from responses
- Request chaining
- API call editor with visual interface

## Testing Features

### Request Types
- GET requests
- POST requests
- PUT requests
- DELETE requests
- PATCH requests
- Custom HTTP methods

### Authentication Methods
- Basic Authentication
- OAuth 2.0
- API Keys
- JWT Tokens
- Custom authentication

### Response Validation
- Status code verification
- Response body validation
- Header validation
- Schema validation
- Custom assertions

### Data Handling
- JSON parsing
- XML parsing
- Form data
- File uploads
- Binary data

### Test Management
- Test case organization
- Environment configuration
- Variable management
- Test data management
- Test execution scheduling
</details>

[Back to top](#feature-list)

## Load Testing

### What is the Load Testing Feature?
The Load Testing feature allows users to optimize performance testing by controlling browser concurrency.

### Key Capabilities
- Customized testing configurations
- Multiple browser instances
- Performance optimization
- User-friendly interface
- Real-time monitoring
- Concurrent browser execution

<details>
<summary>Learn more about Load Testing</summary>

## What is Load Testing?
Load Testing is a type of performance testing that simulates real-world load on any software, application or website. It helps determine how the system behaves under normal and peak conditions.

## Key Capabilities
- Customized testing configurations
- Multiple browser instances
- Performance optimization
- User-friendly interface
- Real-time monitoring
- Concurrent browser execution

## Testing Features

### Configuration Options
- Number of virtual users
- Test duration
- Ramp-up period
- Think time
- Browser types
- Network conditions

### Monitoring Metrics
- Response time
- Throughput
- Error rate
- Resource utilization
- Network latency
- Browser metrics

### Test Scenarios
- Constant load
- Step load
- Spike testing
- Endurance testing
- Stress testing
- Scalability testing

### Reporting
- Real-time graphs
- Performance metrics
- Error analysis
- Resource utilization
- Test summary
- Detailed reports
</details>

[Back to top](#feature-list)

## Historical Analysis Feature

### What is the Historical Analysis Feature?
The Historical Analysis Feature provides comprehensive capabilities for analyzing test execution history, trends, and patterns over time. It enables teams to track test performance, identify recurring issues, and make data-driven decisions about test maintenance and optimization.

### Key Capabilities
- Test execution history tracking
- Performance trend analysis
- Failure pattern identification
- Test coverage evolution
- Execution time tracking
- Test result visualization
- Custom report generation
- Data export capabilities

<details>
<summary>Learn more about Historical Analysis</summary>

## What is the Historical Analysis Feature?
The Historical Analysis Feature provides comprehensive capabilities for analyzing test execution history, trends, and patterns over time. It enables teams to track test performance, identify recurring issues, and make data-driven decisions about test maintenance and optimization.

## Key Capabilities
- Test execution history tracking
- Performance trend analysis
- Failure pattern identification
- Test coverage evolution
- Execution time tracking
- Test result visualization
- Custom report generation
- Data export capabilities

## Analysis Components

### Test Execution History
- Complete test run history
- Execution status tracking
- Environment information
- Test duration metrics
- Screenshot history
- Video recordings
- Log archives

### Performance Metrics
- Execution time trends
- Resource utilization
- Response time analysis
- Throughput measurements
- Error rate tracking
- Success rate calculations

### Visualization Tools
- Interactive charts
- Trend graphs
- Heat maps
- Timeline views
- Comparative analysis
- Custom dashboards

## Data Management

### Storage Options
- Local database storage
- Cloud storage integration
- Data retention policies
- Backup and restore
- Data archiving
</details>

[Back to top](#feature-list)

## Data Driven Testing

### What is the Data Driven Testing Feature?
The Data Driven Testing Feature allows testing with multiple data sets from various sources.

### Key Capabilities
- Excel file integration
- Auto-saving data changes
- Multiple data source support
- Dynamic data handling
- Test case parameterization

<details>
<summary>Learn more about Data Driven Testing</summary>

## What is the Data Driven Testing Feature?
The Data Driven Testing Feature enables testing with multiple data sets from various sources, allowing for comprehensive test coverage and efficient test maintenance through data-driven approaches.

## Key Capabilities
- Excel file integration
- Auto-saving data changes
- Multiple data source support
- Dynamic data handling
- Test case parameterization
- Data set management
- Variable substitution
- Data validation
- Test iteration control
- Data-driven reporting

## Supported Data Sources

### File-based Sources
- Excel (.xlsx, .xls)
- CSV files
- JSON files
- XML files
- YAML files

### Database Sources
- SQL databases
- NoSQL databases
- Custom database connections
- Query results
- Stored procedures

### API Sources
- REST API responses
- GraphQL queries
- SOAP services
- Custom API endpoints
- Web service responses

## Implementation Methods

### Excel Integration
- Direct Excel file upload
- Sheet selection
- Range specification
- Header row configuration
- Data type mapping
- Auto-save functionality

### Data Management
- Data set creation
- Data set modification
- Data validation rules
- Data refresh options
- Version control
- Data set sharing

### Test Configuration
- Test case parameterization
- Data-driven test design
- Test iteration control
- Data validation rules
- Error handling
- Reporting configuration
</details>

[Back to top](#feature-list)

## Database Testing

### What is the Database Testing Feature?
The Database Testing Feature enables direct database interactions and validations, providing comprehensive support for both SQL and NoSQL databases through SQLAlchemy and other database drivers.

### Key Capabilities
- SQL and NoSQL database support
- Database connection management
- CRUD operations execution
- Data validation and assertions
- Query execution and result analysis
- JQ pattern support for data processing
- Secure credential management
- JSON output conversion

<details>
<summary>Learn more about Database Testing</summary>

## What is the Database Testing Feature?
The Database Testing Feature enables direct database interactions and validations, providing comprehensive support for both SQL and NoSQL databases through SQLAlchemy and other database drivers.

## Key Capabilities
- SQL and NoSQL database support
- Database connection management
- CRUD operations execution
- Data validation and assertions
- Query execution and result analysis
- JQ pattern support for data processing
- Secure credential management
- JSON output conversion

## Supported Databases

### SQL Databases
- SQLite
- MySQL/MariaDB
- PostgreSQL
- Microsoft SQL Server
- Oracle
- IBM DB2

### NoSQL Databases
- MongoDB
- Redis
- Cassandra
- Elasticsearch
- Graph Databases (Neo4j+)

## Database Drivers Installation

Install the required database drivers using Poetry:

| Database | Poetry Install Command |
|----------|----------------------|
| SQLAlchemy | `poetry add sqlalchemy` |
| MySQL (PyMySQL) | `poetry add pymysql` |
| MySQL (MySQL Connector) | `poetry add mysql-connector-python` |
| PostgreSQL (Psycopg2) | `poetry add psycopg2` |
| SQLite | `poetry add sqlite` |
| MSSQL (PyODBC) | `poetry add pyodbc` |
| Oracle (cx_Oracle) | `poetry add cx_oracle` |
| IBM Db2 | `poetry add ibm_db_sa` |
</details>

[Back to top](#feature-list)

## Mobile Testing

### What is the Mobile Testing Feature?
The Mobile Testing feature enables automated testing on mobile devices through emulators and real devices.

### Key Capabilities
- Mobile device emulation
- APK installation and management
- noVNC remote device visualization
- Appium Inspector integration
- Real-time device monitoring
- Screenshot capture
- Multi-user access
- CI/CD integration

<details>
<summary>Learn more about Mobile Testing</summary>

## Introduction

Automated tests on mobile devices are crucial for ensuring software quality, efficiency, and consistency. 

They help detect errors quickly, reduce testing time, and are scalable, allowing for testing across multiple device configurations without manual intervention. 

Statistics show that 80% of companies adopting automated testing report increased software quality and shorter delivery times. By implementing a feature that automates these steps with a mobile emulator, you can significantly improve workflow and application reliability.

### Start Mobile

Why is the Start button activated for mobile device containers?

Once manually activated, access to the mobile device is available through the predefined steps provided in the Feature's Step Editor.

These mobile containers can be initialized, paused, and restarted.

Mobile containers can be accessed in two ways:

  * Through the Feature.
  * Through the Landing Tree.

To work with the feature, follow these steps:

Go to the feature of the desired department and click on Modify.

### Main view

Once all steps are completed, the result will appear as the second icon (a camera).
If there is one mobile, it will display directly; if multiple, a dropdown will allow selection.
Additionally, there is a 'Mobile' column that shows the mobile name.

<img src="https://raw.githubusercontent.com/cometa-rocks/cometa_documentation/main/img/mobile_feature/result.png" width="1000px">

### NoVNC Inspect

<h4>1. noVNC</h4> 
noVNC enables web-based access to VNC servers via browsers.
<img src="https://raw.githubusercontent.com/cometa-rocks/cometa_documentation/main/img/mobile_feature/novnc.png" width="400px">

<!-- noVNC Functionalities Table -->
<table>
  <thead>
    <tr>
      <th>Feature</th>
      <th>Description</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td>Remote Device Visualization</td>
      <td>View the device screen in real-time via a web browser, ideal for debugging and monitoring automated tests.</td>
    </tr>
    <tr>
      <td>Remote Device Control</td>
      <td>Interact with the device using the keyboard and mouse to simulate taps, swipes, and other gestures.</td>
    </tr>
    <tr>
      <td>Test Automation Monitoring</td>
      <td>Run Appium automated tests while observing live progress, quickly identifying visual or functional issues.</td>
    </tr>
    <tr>
      <td>Session Recording</td>
      <td>Record interactions during tests or debugging for later review and analysis.</td>
    </tr>
    <tr>
      <td>Screenshot Capturing</td>
      <td>Take screenshots directly from the noVNC interface for comparison or visual testing.</td>
    </tr>
    <tr>
      <td>Multi-User Access</td>
      <td>Allow multiple users to observe or interact with a device simultaneously, ideal for team collaboration.</td>
    </tr>
    <tr>
      <td>Application Debugging</td>
      <td>Test user interactions in real-time across various devices and resolutions to identify design or functionality issues.</td>
    </tr>
    <tr>
      <td>Virtual Device Management</td>
      <td>Monitor and control emulated devices, adjust emulator settings, or restart devices remotely.</td>
    </tr>
    <tr>
      <td>CI/CD Integration</td>
      <td>Observe automated test runs as part of CI/CD pipelines, ensuring devices are active and functional.</td>
    </tr>
  </tbody>
</table>

<h4>2. Inspector</h4> 
Appium Inspector identifies mobile app elements for automated testing.
<img src="https://raw.githubusercontent.com/cometa-rocks/cometa_documentation/main/img/mobile_feature/inspect.png" width="400px">
</details>

[Back to top](#feature-list)

## Accessibility Testing

### What is the Accessibility Testing Feature?
The Accessibility Testing Feature enables automated testing of web applications for compliance with accessibility standards and guidelines, ensuring your applications are accessible to users with disabilities.

### Key Capabilities
- WCAG 2.1 compliance testing
- Automated accessibility scanning
- Detailed violation reporting
- Screen reader compatibility testing
- Keyboard navigation testing
- Color contrast validation
- ARIA attribute verification
- Accessibility score generation
- PDF report generation
- Integration with existing test suites

<details>
<summary>Learn more about Accessibility Testing</summary>

## What is the Accessibility Testing Feature?
The Accessibility Testing Feature enables automated testing of web applications for compliance with accessibility standards and guidelines, ensuring your applications are accessible to users with disabilities.

## Key Capabilities
- WCAG 2.1 compliance testing
- Automated accessibility scanning
- Detailed violation reporting
- Screen reader compatibility testing
- Keyboard navigation testing
- Color contrast validation
- ARIA attribute verification
- Accessibility score generation
- PDF report generation
- Integration with existing test suites

## Supported Standards

### WCAG Guidelines
- WCAG 2.0 Level A
- WCAG 2.0 Level AA
- WCAG 2.1 Level A
- WCAG 2.1 Level AA
- WCAG 2.1 Level AAA

### Additional Standards
- Section 508
- ADA Compliance
- EN 301 549
- ISO/IEC 40500

## Testing Categories

### Visual Accessibility
- Color contrast ratios
- Text size and scaling
- Image alt text
- Focus indicators
- Visual hierarchy

### Structural Accessibility
- Semantic HTML
- ARIA landmarks
- Heading structure
- List markup
- Table structure

### Interactive Accessibility
- Keyboard navigation
- Focus management
- Form labels
- Error handling
- Dynamic content updates
</details>

[Back to top](#feature-list)

## Multi-Factor Authentication

### What is the MFA Feature?
The MFA Feature enables testing of multi-factor authentication systems, including OTP generation and validation.

### Key Capabilities
- OTP generation
- Secret key management
- Encrypted variable storage
- MFA flow automation
- Integration with authentication systems

<details>
<summary>Learn more about Multi-Factor Authentication</summary>

# Automation of Multi Factor Authentication with Cometa
Multi factor authentication which are done by One time password, those can be automated using Cometa 

## 1. MFA and OTP

* **MFA (Multi Factor Authentication)**
    Multi-factor authentication (**MFA**, **two-factor authentication**, or **2FA**, along with similar terms) is an electronic authentication method in which a user is granted access to a website or application only after successfully presenting two or more pieces of evidence (or factors) to an authentication mechanism. 
    <br>
    <br>
    **Source [Wikipedia](https://en.wikipedia.org/wiki/Multi-factor_authentication)** 
    <br>
    <br>
* **OTP (One Time Password)**
    A one-time password (OTP), also known as a one-time PIN, one-time authorization code (OTAC) or dynamic password, is a password that is valid for only one login session or transaction, on a computer system or other digital device.
    <br>
    
    OTP generation algorithms make use of pseudorandomness to generate a shared key.
    <br> 
    <br> 
    <b>Source: [Wikipedia](https://en.wikipedia.org/wiki/One-time_password) </b>
    <br>
    <br>

### Steps of MFA Automation and Prerequisite  

The automation of two-factor authentication with Cometa requires two steps.

* **Step 1: Get Secret Key**  
    Get the secret key from your authenticator app. This key is used to generate OTPs.
    <br>
    <br>
    <i> Note: OTP will be valid for 60 seconds</i>
    <br>
    <br>
        For more information, use the pyAuth library to generate OTPs – see: https://github.com/pyauth/pyotp.
    <br>
    <br>

* **Step 2: Create Test**  Store the <i>secret key</i> in Cometa as a <i>secret variable</i>. Once the authentication token is stored, you can proceed to generate OTP using Cometa by following the next step. 

      Create one-time password of "{x}" digits using pairing-key "{value}" and save it to the encrypted variable "{variable_name}
        
    Refer to the <a target="_blank" href="https://github.com/Cometa-rocks/Cometa_documentation/blob/main/docs/user/cometa_actions.md#:~:text=online%20excel%20viewer.-,Create%20one%2Dtime%20password%20of%20%22%7Bx%7D%22%20digits%20using,-pairing%2Dkey%20%22%7Bvalue">Create one-time password using Cometa </a>


    #### For illustration, you can automate the login screen of Cometa to test the functionality of the MFA automation feature

    **Steps to be automated**

    #### Manual Steps of Cometa login 
    * Fill Captcha

    * Select Login with Gitlab

    * Enter your "Gitlab_UserID"

    * Enter your "Gitlab_Password"

    * Click Sign In

    * Get OTP(Verification Code)

    * Enter OTP
    
    * Your will be logged into Cometa with MFA.


    #### Automation steps of MFA in Cometa login.

    * Create a feature in Cometa <br>

    * Provide a feature name and description<br>

    * Please follow the steps, as shown in the screenshot below
    <br>
    <br>
    <img src="https://raw.githubusercontent.com/cometa-rocks/cometa_documentation/main/img/mfa_screens/MFA_login_test.png" width="700px"/> 
</details>

[Back to top](#feature-list)

## Email Feature

### What is the Email Feature?
The Email Feature enables sending notifications upon completion or failure of test executions, with customizable email templates and screenshot attachments.

### Key Capabilities
- Configure recipient email addresses (To, CC, BCC)
- Custom email subject and message body
- HTML template support
- Screenshot attachments
- Conditional email sending (Always/On error)
- PDF report attachments
- Custom template options

<details>
<summary>Learn more about Email Feature</summary>

## Steps to Configure the Email Feature

1. **In the create Feature screen navigate to the EMAIL TEMPLATE section**
   <br>
   <br>
    <img src="https://raw.githubusercontent.com/cometa-rocks/cometa_documentation/main/img/email/email_template.png" alt="Email Template" style="display: block; max-width: 1000px;">

2. **Add Recipient Email Addresses**:
    - In the field labeled "Email address, use tab to separate emails," enter the email addresses of the recipients. Separate multiple email addresses by pressing the `Tab` key.
    - Example: `abc@xyz.com`

3. **CC (Carbon Copy)**:
    - This field allows you to include additional recipients who will receive a copy of the email. The recipients listed here can see each other's email addresses. Use tabs to separate multiple email addresses. 
    - Separate multiple email addresses by pressing the `Tab` key.
      - Example: `abc@xyz.com`

4. **BCC (Blind Carbon Copy)**:
    - This field is used for entering email addresses of recipients who will receive the email without other recipients being aware of it. 
    - Each recipient added here will not be able to see the other addresses listed in this field. Use tabs to separate multiple email addresses.
    - Separate multiple email addresses by pressing the `Tab` key.
      - Example: `abc@xyz.com`

5. **Subject**:
    - Enter the subject of your email in the "Subject" field. If you leave this field empty, a default subject will be used.
    - Example: `Subject. Leave it empty for a default subject.`

6. **Message Body**:
    - Enter the body of your email in the "Message Body" field. If left empty, a default message with information about the feature will be used.
    - You can create a custom body using an HTML template and include screenshots as shown below.
   Example:
    ```html
    Hi Mr, ABC
    <br>
    Please find attached Screenshots for details
    <br>
    $screenshot[1]
    <br>
    <br> Screen shot for second screen
    <br>
    $screenshot[2]
    <br>
    <br>
    $screenshot[3]
    <br>
    <br>
    <br>Thanks, 
    <br><b>Feature Name</b>
    <br><b>Co.meta</b>
    ```
    - Screenshots will be included in the email body in the sequence they are enabled in the steps. The placeholders $screenshot[1], $screenshot[2], etc., correspond to the screenshots of the steps that have the screenshot option enabled.
    - When an email is received, you will see that the screenshots are attached as images in the same sequence as they are mentioned in the mail body template above.

7. **Email Sending Conditions**: Choose when to send the email:
    - **Always**: Sends an email regardless of the task's outcome.
    - **On error**: Sends an email only if the task encounters an error.

8. **Additional Options**:
    - **Do not use default template**: Check this option if you do not want to use the default email template, By default this is Off.
    - **Attach PDF report to email**: Check this option if you want to attach a PDF report to the email, By default this is On.
</details>

[Back to top](#feature-list)

## Telegram Notifications

### What is the Telegram Notifications Feature?
The Telegram Notifications Feature enables sending test execution results and updates directly to Telegram channels or groups, providing real-time notifications with customizable templates and attachments.

### Key Capabilities
- Custom Telegram bot integration
- Real-time test execution notifications
- Customizable notification templates
- PDF report attachments
- Screenshot attachments (up to 10)
- Variable content inclusion
- Conditional notification sending
- Maximum error notification limits
- Department-level configuration
- Group topic support

> [!TIP]
> Watch our <a href="https://www.youtube.com/watch?v=j-hTiwg5o30" target="_blank">video tutorial</a> to see Telegram Notifications in action!

<details>
<summary>Learn more about Telegram Notifications</summary>

## What is the Telegram Notifications Feature?
The Telegram Notifications Feature provides a seamless way to receive test execution updates and results directly in your Telegram channels or groups. It offers flexible configuration options and supports both default and custom notification templates.

## Key Capabilities
- Custom Telegram bot integration
- Real-time test execution notifications
- Customizable notification templates
- PDF report attachments
- Screenshot attachments (up to 10)
- Variable content inclusion
- Conditional notification sending
- Maximum error notification limits
- Department-level configuration
- Group topic support

## Configuration Options

### Bot Settings
- Use default Cometa chatbot
- Override with custom bot token
- Custom chat ID configuration
- Message thread ID for group topics
- Department-level chat ID management

### Notification Content
- Department information
- Application environment details
- Test execution status
- Step results
- Pixel differences
- Execution date and time
- Browser timezone information
- Custom variable inclusion
- PDF report attachments
- Screenshot attachments (up to 10)

### Sending Conditions
- Always send notifications
- Send on error only
- Maximum error notification limit
- Custom error thresholds

### Template Options
- Default template with basic information
- Custom message templates
- Variable substitution
- HTML formatting support
- Attachment configuration

## Setup Instructions

1. **Enable Telegram Notifications**:
   - Navigate to the feature settings
   - Click on "Set notifications on finish"
   - Select "Telegram" option

2. **Configure Bot Settings**:
   - Choose between default Cometa bot or custom bot
   - For custom bot:
     - Enter your bot token
     - Specify chat ID
     - Add message thread ID (optional)
   - For default bot:
     - Add chat IDs in department admin panel
     - Separate multiple chat IDs with commas

3. **Customize Notification Content**:
   - Select notification template
   - Configure custom message
   - Choose attachments (PDF report, screenshots)
   - Set notification conditions

4. **Set Sending Conditions**:
   - Choose between "Always" or "On error only"
   - Configure maximum error notifications
   - Set custom error thresholds

## Best Practices
- Use custom variables for dynamic content
- Configure appropriate error thresholds
- Utilize group topics for better organization
- Regularly update chat IDs in department settings
- Monitor notification delivery
- Test notification templates before deployment
</details>

[Back to top](#feature-list)

## Need Help?

### Where can I get help?
- Join our [Discord community](https://discord.gg/PUxt5bsRej)
- Contact us at [tec_dev@cometa.rocks](mailto:tec_dev@cometa.rocks)

Happy testing! 🚀 
