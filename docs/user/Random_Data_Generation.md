# Faker Data Generator for Cometa Random Data Generator Steps

<picture>
  <source media="(prefers-color-scheme: dark)" srcset="https://raw.githubusercontent.com/cometa-rocks/cometa_documentation/main/img/logos/COMETAROCKS_LogoEslog_Y_W.png">
  <source media="(prefers-color-scheme: light)" srcset="https://raw.githubusercontent.com/cometa-rocks/cometa_documentation/main/img/logos/COMETAROCKS_LogoEslog_Y_B.png">
  <img alt="Shows a black logo in light color mode and a white one in dark color mode." src="https://raw.githubusercontent.com/cometa-rocks/cometa_documentation/main/img/logos/COMETAROCKS_LogoEslog_Y_B.png">
</picture>

> [!TIP]
> Use your browser's search (Ctrl+F or Cmd+F) to find specific data types or features.

## What is the Random Data Generator?

This module provides a custom Behave step to dynamically generate fake data using the [Faker](https://faker.readthedocs.io/en/master/) library and store it in a runtime variable for use across your test scenarios. It also supports generating random strings based on regular expressions using the `rstr` library.

## Key Capabilities
- Generate realistic fake data for test automation
- Store generated data in runtime variables for reuse
- Support for a wide variety of data types (see below)
- Generate random strings from custom regex patterns

## Faker Data Step Definition

This step generates fake data of a specified type and stores it in a runtime variable for use across your test scenarios.

```gherkin
Generate random "<information>" and store in "<variable>"
```
- **information**: Type of fake data to generate (e.g., `email`, `name`, `address`)
- **variable**: Name of the variable to store the generated value

### Example Usage
```gherkin
Generate random "email" and store in "random_value"
```

## Supported Random Data Types
The following information types are supported out of the box:

<details>
<summary>Show supported types</summary>

- `first_name`, `last_name`, `name`
- `email`, `safe_email`, `free_email`, `ascii_email`
- `phone_number`
- `address`, `street_address`, `city`, `state`, `country`, `postalcode`, `zip_code`
- `day_of_week`, `day_of_month`, `month`, `month_name`
- `timezone`
- `uid`, `uuid4`
- `company`, `company_email`, `company_suffix`
- `job`, `language_code`, `user_name`
- `credit_card_number`, `iban`, `bban`
- `ipv4`, `ipv6`, `mac_address`
- `date`, `date_of_birth`, `time`, `year`
- `paragraph`, `sentence`, `word`, `text`
- `url`, `domain_name`, `file_name`
- `color_name`, `hex_color`, `rgb_color`
- ...and many more (see Faker documentation)

</details>

## Regex-Based Random String Generator for Behave Steps

This step definition allows generating random strings based on regular expressions (regex) and storing them as runtime variables using the `rstr` library.

```gherkin
Generate random string based on "<regex_pattern>" and store in "<variable>"
```
- **regex_pattern**: A valid regex pattern supported by `rstr.xeger`.
- **variable**: Name of the runtime variable to store the generated value.

### Example Usage
```gherkin
Generate random string based on "[A-Za-z0-9]{8}" and store in "random_id"
Generate random string based on "[a-z]{5,10}" and store in "username"
```

### Sample Patterns & Generated Results

| Pattern Description       | Regex Pattern                                               | Sample Results             |
|--------------------------|-------------------------------------------------------------|----------------------------|
| Alphanumeric 8-char      | `[A-Za-z0-9]{8}`                                            | `Ax2Df7Lz`, `Hd82KaPz`     |
| Lowercase word (5–10)    | `[a-z]{5,10}`                                               | `tgdblmk`, `flanders`      |
| Email format             | `[a-z]{5,10}\.[a-z]{3,5}@[a-z]{4,8}\.com`                 | `bradley.port@oceanbay.com`, `elena.code@pixels.com` |
| Date (YYYY-MM-DD)        | `\d{4}-\d{2}-\d{2}`                                      | `2022-08-14`, `2023-04-17` |
| UUID format              | `[a-f0-9]{8}-[a-f0-9]{4}-[1-5][a-f0-9]{3}-[89ab][a-f0-9]{3}-[a-f0-9]{12}` | `9b2f4a87-b4c3-4a2c-9d9f-204d5a2e2f3b`, `a1b2c3d4-e5f6-4a7b-8c9d-e0f1a2b3c4d5` |
| IP Address               | Complex IPv4 regex                                         | `192.168.1.254`, `10.0.0.1`|
| US Phone Number          | `\(\d{3}\) \d{3}-\d{4}`                                | `(415) 555-0198`, `(202) 123-4567` |
| Hex Color Code           | `#[A-Fa-f0-9]{6}`                                          | `#4Bc91f`, `#1A2B3C`       |
| Strong Password Format   | `[A-Z]{1}[a-z]{3,5}[0-9]{3}`                               | `Nxyz123`, `Pabc456`       |
| US ZIP Code              | `\d{5}(-\d{4})?`                                         | `12345-6789`, `90210`      |

## Need Help?

### Where can I get help?
- Join our [Discord community](https://discord.gg/PUxt5bsRej)
- Contact us at [tec_dev@cometa.rocks](mailto:tec_dev@cometa.rocks)

Happy testing! 🚀