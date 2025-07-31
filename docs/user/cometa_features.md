
<picture>
  <source media="(prefers-color-scheme: dark)" srcset="https://raw.githubusercontent.com/cometa-rocks/cometa_documentation/main/img/logos/COMETAROCKS_LogoEslog_Y_W.png">
  <source media="(prefers-color-scheme: light)" srcset="https://raw.githubusercontent.com/cometa-rocks/cometa_documentation/main/img/logos/COMETAROCKS_LogoEslog_Y_B.png">
  <img alt="Shows a black logo in light color mode and a white one in dark color mode." src="https://raw.githubusercontent.com/cometa-rocks/cometa_documentation/main/img/logos/COMETAROCKS_LogoEslog_Y_B.png" style="display: block; max-width: 800px;">
</picture>

# Co.meta Features Documentation

> [!TIP]
> - Use your browser's search (Ctrl+F or Cmd+F) to find specific features

## Feature List
1. [End to End Monitoring](#end-to-end-monitoring)
2. [Basic Security Feature](#security-feature)
3. [AI & Automation Feature](#ai-feature)
4. [API Testing](#api-testing)
5. [Load Testing](#load-testing)
6. [Historical Analysis Feature](#historical-analysis-feature)
7. [Data Driven Testing](#data-driven-testing)
8. [Database Testing](#database-testing)
9. [Random Data Generation](#random-data-generation)
10. [Mobile Testing](#mobile-testing)
11. [Mobile Automation Testing](#mobile-automation-testing)
12. [Accessibility Testing](#accessibility-testing)
13. [Multi-Factor Authentication](#multi-factor-authentication)
14. [Email Feature](#email-feature)
15. [Telegram Notifications](#telegram-notifications)

## End to End Monitoring

### Key Capabilities
- Real-time test execution monitoring
- WebSocket-based live updates
- Test progress visualization
- Results analysis and reporting
- Screenshot comparison
- Video recording of test execution
- PDF report generation
- Performance metrics tracking

[See full documentation + Video Tutorial →](../user/e2e_monitoring.md) 

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

[See full documentation + Video Tutorial →](../user/security_feature.md)

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

[See full documentation + Video Tutorial →](../user/ai_feature.md)

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

[See full documentation + Video Tutorial →](../user/api_test.md)

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

[See full documentation + Video Tutorial →](../user/LOAD_TESTING.md)

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

[See full documentation + Video Tutorial →](../user/historical_analysis.md)

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

[See full documentation + Video Tutorial →](../user/data_driven_testing.md)

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

[See full documentation + Video Tutorial →](../user/database_testing.md)

[Back to top](#feature-list)

## Random Data Generation

### What is the Random Data Generation Feature?
The Random Data Generation feature enables you to create realistic fake data and random strings for your test automation, supporting a wide variety of data types and custom patterns.

### Key Capabilities
- Generate fake data using the Faker library
- Create random strings from regex patterns
- Store generated data in runtime variables
- Support for many data types (names, emails, addresses, etc.)
- Easy integration with test steps

[See full documentation + Video Tutorial →](../user/Random_Data_Generation.md)

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

[See full documentation + Video Tutorial →](../user/mobile_feature.md)

[Back to top](#feature-list)

## Mobile Automation Testing

### What is the Mobile Automation Testing Feature?
The Mobile Automation Testing feature enables end-to-end automation of mobile app testing using emulators, APK upload, and intuitive test case creation. It streamlines the process from uploading your APK to running automated test cases, supporting collaboration and flexible test creation.

### Key Capabilities
- End-to-end automation from APK upload to test execution
- Emulator management and sharing for collaborative testing
- Intuitive interface for APK upload, app info extraction, and test case building
- Flexible test creation with locator and inspector tools
- Real-time monitoring of test execution
- Collaboration features for sharing emulator state
- Support for cleanup steps (e.g., uninstalling apps after tests)

[See full documentation + Video Tutorial →](../user/mobile_automation_testing.md)

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

[See full documentation + Video Tutorial →](../user/accessibility_testing.md)

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

[See full documentation + Video Tutorial →](../user/mfa_authentication_using_cometa.md)

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

[See full documentation + Video Tutorial →](../user/email_feature.md)

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

[See full documentation + Video Tutorial →](../user/telegram_feature.md)

[Back to top](#feature-list)

## Need Help?

### Where can I get help?
- Join our [Discord community](https://discord.gg/PUxt5bsRej)
- Contact us at [tec_dev@cometa.rocks](mailto:tec_dev@cometa.rocks)

Happy testing! 🚀 
