[![ Apache License Version 2.0](https://img.shields.io/badge/license-apache-v2.svg)](https://www.apache.org/licenses/LICENSE-2.0)


# Google Ads PHP API Oauth2 Web Application Refresh Token Generator

## Introduction

This PHP script allows you to generate an OAuth2 refresh token for the Google Ads API using the Desktop application flow. The refresh token can be used to obtain access tokens for authenticating requests against the Google Ads API. 

Tested up to V15

## Prerequisites

- PHP installed on your system. (PHP 8.1 Required)
- Google Ads API PHP client library installed. 

```
git clone https://github.com/googleads/google-ads-php.git
```

- You can install it using Composer:

```
composer install
```

## Usage

1. Clone or download the Google Ads PHP API client library from the official repository: [google-ads-php](https://github.com/googleads/google-ads-php).

2. Navigate to the directory where the script is located:

```
cd path/to/google-ads-php/examples/Authentication
```
3. Copy & open the auth.php file and set the REDIRECT_URI variable to your desired redirect URI. 

`private const REDIRECT_URI = 'INSERT_REDIRECT_URL_HERE';`

4. Run the script:

```
php path/to/google-ads-php/examples/Authentication/auth.php
```
or if you have copied the file into the google-ads-php root directory;

```
php path/to/google-ads-php/auth.php
```

5. Follow the prompts to enter the OAuth2 client ID, client secret, and any additional scopes (if needed).

6. Visit the generated authorization URL in your web browser.

7. Log into the Google account associated with your Google Ads.

8. Enter the state variable and the code when prompted by the script.

9. After approval, enter the authorization code provided by the Google OAuth2 server.

10. The script will output your refresh token. Copy this token.

11. Update your google_ads_php.ini file with the following information:

```
[GOOGLE_ADS]
developerToken = "INSERT_DEVELOPER_TOKEN_HERE"
; Optional: Specify the login customer ID used to authenticate API calls.
; loginCustomerId = "INSERT_LOGIN_CUSTOMER_ID_HERE"

[OAUTH2]
clientId = "YOUR_OAUTH2_CLIENT_ID"
clientSecret = "YOUR_OAUTH2_CLIENT_SECRET"
refreshToken = "YOUR_REFRESH_TOKEN"
```

Replace "INSERT_DEVELOPER_TOKEN_HERE", "INSERT_LOGIN_CUSTOMER_ID_HERE", "YOUR_OAUTH2_CLIENT_ID", "YOUR_OAUTH2_CLIENT_SECRET", and "YOUR_REFRESH_TOKEN" with your actual values.
## Contributing

Contributions are always welcome!



## Authors

- [@rolandfarkasCOM](https://www.github.com/rolandfarkascom)

