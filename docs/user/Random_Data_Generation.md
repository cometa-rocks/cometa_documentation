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
- `aba`
- `address`
- `administrative_unit`
- `am_pm`
- `android_platform_token`
- `ascii_company_email`
- `ascii_email`
- `ascii_free_email`
- `ascii_safe_email`
- `bank_country`
- `bban`
- `binary`
- `boolean`
- `bothify`
- `bs`
- `building_number`
- `catch_phrase`
- `century`
- `chrome`
- `city`
- `city_prefix`
- `city_suffix`
- `color`
- `color_name`
- `company`
- `company_email`
- `company_suffix`
- `coordinate`
- `country`
- `country_calling_code`
- `country_code`
- `credit_card_expire`
- `credit_card_full`
- `credit_card_number`
- `credit_card_provider`
- `credit_card_security_code`
- `cryptocurrency`
- `cryptocurrency_code`
- `cryptocurrency_name`
- `csv`
- `currency`
- `currency_code`
- `currency_name`
- `currency_symbol`
- `current_country`
- `current_country_code`
- `date`
- `date_between`
- `date_between_dates`
- `date_object`
- `date_of_birth`
- `date_this_century`
- `date_this_decade`
- `date_this_month`
- `date_this_year`
- `date_time`
- `date_time_ad`
- `date_time_between`
- `date_time_between_dates`
- `date_time_this_century`
- `date_time_this_decade`
- `date_time_this_month`
- `date_time_this_year`
- `day_of_month`
- `day_of_week`
- `dga`
- `domain_name`
- `domain_word`
- `dsv`
- `ean`
- `ean13`
- `ean8`
- `ein`
- `email`
- `file_extension`
- `file_name`
- `file_path`
- `firefox`
- `first_name`
- `first_name_female`
- `first_name_male`
- `first_name_nonbinary`
- `fixed_width`
- `free_email`
- `free_email_domain`
- `future_date`
- `future_datetime`
- `get_providers`
- `hex_color`
- `hexify`
- `hostname`
- `http_method`
- `iana_id`
- `iban`
- `image`
- `image_url`
- `internet_explorer`
- `invalid_ssn`
- `ios_platform_token`
- `ipv4`
- `ipv4_network_class`
- `ipv4_private`
- `ipv4_public`
- `ipv6`
- `isbn10`
- `isbn13`
- `iso8601`
- `items`
- `itin`
- `job`
- `json`
- `language_code`
- `language_name`
- `last_name`
- `last_name_female`
- `last_name_male`
- `last_name_nonbinary`
- `latitude`
- `latlng`
- `lexify`
- `license_plate`
- `linux_platform_token`
- `linux_processor`
- `local_latlng`
- `locale`
- `localized_ean`
- `localized_ean13`
- `localized_ean8`
- `location_on_land`
- `longitude`
- `mac_address`
- `mac_platform_token`
- `mac_processor`
- `md5`
- `military_apo`
- `military_dpo`
- `military_ship`
- `military_state`
- `mime_type`
- `month`
- `month_name`
- `msisdn`
- `name`
- `name_female`
- `name_male`
- `name_nonbinary`
- `nic_handle`
- `nic_handles`
- `null_boolean`
- `numerify`
- `opera`
- `paragraph`
- `paragraphs`
- `password`
- `past_date`
- `past_datetime`
- `phone_number`
- `port_number`
- `postalcode`
- `postalcode_in_state`
- `postalcode_plus4`
- `postcode`
- `postcode_in_state`
- `prefix`
- `prefix_female`
- `prefix_male`
- `prefix_nonbinary`
- `pricetag`
- `profile`
- `psv`
- `pybool`
- `pydecimal`
- `pydict`
- `pyfloat`
- `pyint`
- `pyiterable`
- `pylist`
- `pyset`
- `pystr`
- `pystr_format`
- `pystruct`
- `pytimezone`
- `pytuple`
- `random_choices`
- `random_digit`
- `random_digit_not_null`
- `random_digit_not_null_or_empty`
- `random_digit_or_empty`
- `random_element`
- `random_elements`
- `random_int`
- `random_letter`
- `random_letters`
- `random_lowercase_letter`
- `random_number`
- `random_sample`
- `random_uppercase_letter`
- `randomize_nb_elements`
- `rgb_color`
- `rgb_css_color`
- `ripe_id`
- `safari`
- `safe_color_name`
- `safe_domain_name`
- `safe_email`
- `safe_hex_color`
- `secondary_address`
- `seed_instance`
- `sentence`
- `sentences`
- `sha1`
- `sha256`
- `simple_profile`
- `slug`
- `ssn`
- `state`
- `state_abbr`
- `street_address`
- `street_name`
- `street_suffix`
- `suffix`
- `suffix_female`
- `suffix_male`
- `suffix_nonbinary`
- `swift`
- `swift11`
- `swift8`
- `tar`
- `text`
- `texts`
- `time`
- `time_delta`
- `time_object`
- `time_series`
- `timezone`
- `tld`
- `tsv`
- `unix_device`
- `unix_partition`
- `unix_time`
- `upc_a`
- `upc_e`
- `uri`
- `uri_extension`
- `uri_page`
- `uri_path`
- `url`
- `user_agent`
- `user_name`
- `uuid4`
- `windows_platform_token`
- `word`
- `words`
- `year`
- `zip`
- `zipcode`
- `zipcode_in_state`
- `zipcode_plus4`


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