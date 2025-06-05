# API Testing Guide

<picture>
  <source media="(prefers-color-scheme: dark)" srcset="https://raw.githubusercontent.com/cometa-rocks/cometa_documentation/main/img/logos/COMETAROCKS_LogoEslog_Y_W.png">
  <source media="(prefers-color-scheme: light)" srcset="https://raw.githubusercontent.com/cometa-rocks/cometa_documentation/main/img/logos/COMETAROCKS_LogoEslog_Y_B.png">
  <img alt="Shows a black logo in light color mode and a white one in dark color mode." src="https://raw.githubusercontent.com/cometa-rocks/cometa_documentation/main/img/logos/COMETAROCKS_LogoEslog_Y_B.png">
</picture>

## Setting Up API Tests

### Video Demonstration on API Call Editor: [Video](https://youtu.be/plC8qag08ZQ)

1. **Create a New Feature**: Start by creating a new feature in Cometa.
2. **Add API Step**: In the steps section, start by adding API calling step:

```jq
Make an API call with "{method}" to "{endpoint}" with "params:{parameters}" and "headers:{headers}" and "body:{json_body}" and "row_body:{row_body}"
```

3. **Configure Request**: Right clicking the step, displays the option to edit the request in the Edit API call window. This allows a fast and confortable way to edit the HTTP method, parameters, headers and body of the request.
<img src="../../img/APICallEditorButtoon.png" alt="API Call Editor Button" style="display: block; max-width: 500px;">
<br>
<br>
    <img src="../../img/APICallEditor1.png" alt="API Call Editor" style="display: block; max-width: 800px;">

4. **Define Assertions**: Configure assertions to validate the response meets your expectations.

## Need Help?

### Where can I get help?
- Join our [Discord community](https://discord.gg/PUxt5bsRej)
- Contact us at [tec_dev@cometa.rocks](mailto:tec_dev@cometa.rocks)

Happy testing! 🚀 