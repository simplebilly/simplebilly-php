# OpenAPI\Client\AuthApi

Authentication endpoints (login, register, verify, password reset, TOTP, magic link). Public endpoints.

All URIs are relative to https://demo.simplebilly.com, except if the operation defines another base path.

| Method | HTTP request | Description |
| ------------- | ------------- | ------------- |
| [**acceptInvite()**](AuthApi.md#acceptInvite) | **POST** /auth/accept-invite | Accept an invite: create the account (or reuse an existing one) and join the inviting tenant. The invite token proves control of the mailbox. |
| [**forgotPassword()**](AuthApi.md#forgotPassword) | **POST** /auth/forgot-password | Send a password reset email to the user |
| [**login()**](AuthApi.md#login) | **POST** /auth/login | Authenticate a user with email + password (optional TOTP) |
| [**logout()**](AuthApi.md#logout) | **POST** /auth/logout | Log out the current user (kills the assay session) |
| [**magicLinkLogin()**](AuthApi.md#magicLinkLogin) | **POST** /auth/magic-link | Request a magic link login (sends an email with a one-time link) |
| [**magicLinkVerify()**](AuthApi.md#magicLinkVerify) | **POST** /auth/magic-link/verify | Verify a magic link token and log the user in |
| [**register()**](AuthApi.md#register) | **POST** /auth/register | Register a new user account |
| [**resetPassword()**](AuthApi.md#resetPassword) | **POST** /auth/reset-password | Reset the user&#39;s password using a reset token |
| [**totpEnable()**](AuthApi.md#totpEnable) | **POST** /auth/totp/enable | Enable TOTP two-factor authentication by verifying a code |
| [**totpSetup()**](AuthApi.md#totpSetup) | **GET** /auth/totp/setup | Set up TOTP two-factor authentication (generates secret + backup codes) |
| [**verifyEmail()**](AuthApi.md#verifyEmail) | **POST** /auth/verify-email | Verify a user&#39;s email address using a verification token |


## `acceptInvite()`

```php
acceptInvite($accept_invite_request)
```

Accept an invite: create the account (or reuse an existing one) and join the inviting tenant. The invite token proves control of the mailbox.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure Bearer (JWT) authorization: bearer_token
$config = OpenAPI\Client\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new OpenAPI\Client\Api\AuthApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$accept_invite_request = new \OpenAPI\Client\Model\AcceptInviteRequest(); // \OpenAPI\Client\Model\AcceptInviteRequest

try {
    $apiInstance->acceptInvite($accept_invite_request);
} catch (Exception $e) {
    echo 'Exception when calling AuthApi->acceptInvite: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **accept_invite_request** | [**\OpenAPI\Client\Model\AcceptInviteRequest**](../Model/AcceptInviteRequest.md)|  | |

### Return type

void (empty response body)

### Authorization

[bearer_token](../../README.md#bearer_token)

### HTTP request headers

- **Content-Type**: `application/json`
- **Accept**: Not defined

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `forgotPassword()`

```php
forgotPassword($forgot_password_request)
```

Send a password reset email to the user

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure Bearer (JWT) authorization: bearer_token
$config = OpenAPI\Client\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new OpenAPI\Client\Api\AuthApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$forgot_password_request = new \OpenAPI\Client\Model\ForgotPasswordRequest(); // \OpenAPI\Client\Model\ForgotPasswordRequest

try {
    $apiInstance->forgotPassword($forgot_password_request);
} catch (Exception $e) {
    echo 'Exception when calling AuthApi->forgotPassword: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **forgot_password_request** | [**\OpenAPI\Client\Model\ForgotPasswordRequest**](../Model/ForgotPasswordRequest.md)|  | |

### Return type

void (empty response body)

### Authorization

[bearer_token](../../README.md#bearer_token)

### HTTP request headers

- **Content-Type**: `application/json`
- **Accept**: Not defined

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `login()`

```php
login($login_request): \OpenAPI\Client\Model\AuthResponse
```

Authenticate a user with email + password (optional TOTP)

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure Bearer (JWT) authorization: bearer_token
$config = OpenAPI\Client\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new OpenAPI\Client\Api\AuthApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$login_request = new \OpenAPI\Client\Model\LoginRequest(); // \OpenAPI\Client\Model\LoginRequest

try {
    $result = $apiInstance->login($login_request);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling AuthApi->login: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **login_request** | [**\OpenAPI\Client\Model\LoginRequest**](../Model/LoginRequest.md)|  | |

### Return type

[**\OpenAPI\Client\Model\AuthResponse**](../Model/AuthResponse.md)

### Authorization

[bearer_token](../../README.md#bearer_token)

### HTTP request headers

- **Content-Type**: `application/json`
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `logout()`

```php
logout()
```

Log out the current user (kills the assay session)

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure Bearer (JWT) authorization: bearer_token
$config = OpenAPI\Client\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new OpenAPI\Client\Api\AuthApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);

try {
    $apiInstance->logout();
} catch (Exception $e) {
    echo 'Exception when calling AuthApi->logout: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

This endpoint does not need any parameter.

### Return type

void (empty response body)

### Authorization

[bearer_token](../../README.md#bearer_token)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: Not defined

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `magicLinkLogin()`

```php
magicLinkLogin($magic_link_request)
```

Request a magic link login (sends an email with a one-time link)

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure Bearer (JWT) authorization: bearer_token
$config = OpenAPI\Client\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new OpenAPI\Client\Api\AuthApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$magic_link_request = new \OpenAPI\Client\Model\MagicLinkRequest(); // \OpenAPI\Client\Model\MagicLinkRequest

try {
    $apiInstance->magicLinkLogin($magic_link_request);
} catch (Exception $e) {
    echo 'Exception when calling AuthApi->magicLinkLogin: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **magic_link_request** | [**\OpenAPI\Client\Model\MagicLinkRequest**](../Model/MagicLinkRequest.md)|  | |

### Return type

void (empty response body)

### Authorization

[bearer_token](../../README.md#bearer_token)

### HTTP request headers

- **Content-Type**: `application/json`
- **Accept**: Not defined

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `magicLinkVerify()`

```php
magicLinkVerify($magic_link_verify_request): \OpenAPI\Client\Model\AuthResponse
```

Verify a magic link token and log the user in

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure Bearer (JWT) authorization: bearer_token
$config = OpenAPI\Client\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new OpenAPI\Client\Api\AuthApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$magic_link_verify_request = new \OpenAPI\Client\Model\MagicLinkVerifyRequest(); // \OpenAPI\Client\Model\MagicLinkVerifyRequest

try {
    $result = $apiInstance->magicLinkVerify($magic_link_verify_request);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling AuthApi->magicLinkVerify: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **magic_link_verify_request** | [**\OpenAPI\Client\Model\MagicLinkVerifyRequest**](../Model/MagicLinkVerifyRequest.md)|  | |

### Return type

[**\OpenAPI\Client\Model\AuthResponse**](../Model/AuthResponse.md)

### Authorization

[bearer_token](../../README.md#bearer_token)

### HTTP request headers

- **Content-Type**: `application/json`
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `register()`

```php
register($register_request): \OpenAPI\Client\Model\AuthResponse
```

Register a new user account

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure Bearer (JWT) authorization: bearer_token
$config = OpenAPI\Client\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new OpenAPI\Client\Api\AuthApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$register_request = new \OpenAPI\Client\Model\RegisterRequest(); // \OpenAPI\Client\Model\RegisterRequest

try {
    $result = $apiInstance->register($register_request);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling AuthApi->register: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **register_request** | [**\OpenAPI\Client\Model\RegisterRequest**](../Model/RegisterRequest.md)|  | |

### Return type

[**\OpenAPI\Client\Model\AuthResponse**](../Model/AuthResponse.md)

### Authorization

[bearer_token](../../README.md#bearer_token)

### HTTP request headers

- **Content-Type**: `application/json`
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `resetPassword()`

```php
resetPassword($reset_password_request)
```

Reset the user's password using a reset token

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure Bearer (JWT) authorization: bearer_token
$config = OpenAPI\Client\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new OpenAPI\Client\Api\AuthApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$reset_password_request = new \OpenAPI\Client\Model\ResetPasswordRequest(); // \OpenAPI\Client\Model\ResetPasswordRequest

try {
    $apiInstance->resetPassword($reset_password_request);
} catch (Exception $e) {
    echo 'Exception when calling AuthApi->resetPassword: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **reset_password_request** | [**\OpenAPI\Client\Model\ResetPasswordRequest**](../Model/ResetPasswordRequest.md)|  | |

### Return type

void (empty response body)

### Authorization

[bearer_token](../../README.md#bearer_token)

### HTTP request headers

- **Content-Type**: `application/json`
- **Accept**: Not defined

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `totpEnable()`

```php
totpEnable($totp_enable_request)
```

Enable TOTP two-factor authentication by verifying a code

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure Bearer (JWT) authorization: bearer_token
$config = OpenAPI\Client\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new OpenAPI\Client\Api\AuthApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$totp_enable_request = new \OpenAPI\Client\Model\TotpEnableRequest(); // \OpenAPI\Client\Model\TotpEnableRequest

try {
    $apiInstance->totpEnable($totp_enable_request);
} catch (Exception $e) {
    echo 'Exception when calling AuthApi->totpEnable: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **totp_enable_request** | [**\OpenAPI\Client\Model\TotpEnableRequest**](../Model/TotpEnableRequest.md)|  | |

### Return type

void (empty response body)

### Authorization

[bearer_token](../../README.md#bearer_token)

### HTTP request headers

- **Content-Type**: `application/json`
- **Accept**: Not defined

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `totpSetup()`

```php
totpSetup(): \OpenAPI\Client\Model\TotpSetupResponse
```

Set up TOTP two-factor authentication (generates secret + backup codes)

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure Bearer (JWT) authorization: bearer_token
$config = OpenAPI\Client\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new OpenAPI\Client\Api\AuthApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);

try {
    $result = $apiInstance->totpSetup();
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling AuthApi->totpSetup: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

This endpoint does not need any parameter.

### Return type

[**\OpenAPI\Client\Model\TotpSetupResponse**](../Model/TotpSetupResponse.md)

### Authorization

[bearer_token](../../README.md#bearer_token)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `verifyEmail()`

```php
verifyEmail($verify_email_request)
```

Verify a user's email address using a verification token

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure Bearer (JWT) authorization: bearer_token
$config = OpenAPI\Client\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new OpenAPI\Client\Api\AuthApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$verify_email_request = new \OpenAPI\Client\Model\VerifyEmailRequest(); // \OpenAPI\Client\Model\VerifyEmailRequest

try {
    $apiInstance->verifyEmail($verify_email_request);
} catch (Exception $e) {
    echo 'Exception when calling AuthApi->verifyEmail: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **verify_email_request** | [**\OpenAPI\Client\Model\VerifyEmailRequest**](../Model/VerifyEmailRequest.md)|  | |

### Return type

void (empty response body)

### Authorization

[bearer_token](../../README.md#bearer_token)

### HTTP request headers

- **Content-Type**: `application/json`
- **Accept**: Not defined

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)
