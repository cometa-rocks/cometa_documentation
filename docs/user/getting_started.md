<picture>
  <source media="(prefers-color-scheme: dark)" srcset="https://raw.githubusercontent.com/cometa-rocks/cometa_documentation/main/img/logos/COMETAROCKS_LogoEslog_Y_W.png">
  <source media="(prefers-color-scheme: light)" srcset="https://raw.githubusercontent.com/cometa-rocks/cometa_documentation/main/img/logos/COMETAROCKS_LogoEslog_Y_B.png">
  <img alt="Shows a black logo in light color mode and a white one in dark color mode." src="https://raw.githubusercontent.com/cometa-rocks/cometa_documentation/main/img/logos/COMETAROCKS_LogoEslog_Y_B.png">
</picture>

# Getting Started with Cometa
> [!TIP]
> - Use your browser's search (Ctrl+F or Cmd+F) to find specific topics

## Table of Contents
- [Prerequisites](#prerequisites)
- [Creating Your First Test](#creating-your-first-test)
- [Running Your Test](#running-your-test)
- [Understanding Results](#understanding-results)
- [Next Steps](#next-steps)
- [Need Help?](#need-help)

## Prerequisites

### 1. What do I need before starting with Cometa?
Before you begin, make sure you have:
1. Cometa installed and running (see main README for installation instructions)
2. Access to the Cometa UI (typically at http://localhost:4200)
3. Basic understanding of web testing concepts

## Creating Your First Test

### 2. How can I create my first test using the example JSON?
1. **Download the Example**
   - Get the example test case from [feature_example_your_first_testcase.json](feature_example_your_first_testcase.json)

2. **Import the Test**
   - Open the Cometa UI
   - Navigate to the Features section
   - Click "Import JSON"
   - Select the downloaded example file

3. **Review the Test**
   - The example demonstrates basic web testing concepts
   - It includes common actions like:
     - Navigating to a webpage
     - Verifying page elements
     - Inputting data
     - Submitting forms

### 3. How can I create a test from scratch?
1. **Create New Feature**
   - Click "New Feature" in the UI
   - Give your feature a descriptive name
   - Select the appropriate browser(s)

2. **Add Steps**
   - Use the step library to add actions
   - Common first steps include:
     - `Navigate to URL`
     - `Verify element exists`
     - `Input text`
     - `Click element`

3. **Configure Settings**
   - Set browser preferences
   - Configure timeouts
   - Add any necessary variables

## Running Your Test

### 4. How do I run my test?
1. **Select the Feature**
   - Choose your feature from the list
   - Verify all steps are correct

2. **Execute**
   - Click "Run Feature"
   - Watch the test execution in real-time
   - Review the results and logs

## Understanding Results

### 5. What information will I see after test execution?
After test execution, you'll see:
- Pass/fail status
- Detailed logs
- Screenshots (if configured)
- Performance metrics

## Next Steps

### 6. What should I explore next?
Once you're comfortable with basic tests, explore:

#### Core Features
- [Cometa Features](cometa_features.md) - Learn about advanced capabilities
- [Step Library](cometa_actions.md) - Discover all available actions
- [Selectors Guide](css-xpath.md) - Master element targeting
- [REST API](REST-API.md) - Explore automation possibilities

#### Specialized Testing
- [Mobile Testing](mobile_feature.md) - Test on mobile devices
- [AI Features](ai_feature.md) - Leverage AI capabilities
- [Load Testing](LOAD_TESTING.md) - Performance testing guide

#### Additional Resources
- [Tutorials](tutorials.md) - Step-by-step guides
- [FAQ](FAQ.md) - Common questions and answers
- [Questions](questions.md) - Additional Q&A

## Need Help?

### 7. Where can I get help?
- Check the [FAQ](FAQ.md) for common questions
- Join our [Discord community](https://discord.gg/PUxt5bsRej)
- Contact us at [tec_dev@cometa.rocks](mailto:tec_dev@cometa.rocks)

Happy testing! 🚀 
