# OpenAPI\Client\TimeEntriesApi



All URIs are relative to https://demo.simplebilly.com, except if the operation defines another base path.

| Method | HTTP request | Description |
| ------------- | ------------- | ------------- |
| [**clockInTimeEntry()**](TimeEntriesApi.md#clockInTimeEntry) | **POST** /api/v1/time-entries | Clock in for the authenticated user (resolved via their employee profile). |
| [**clockOutTimeEntry()**](TimeEntriesApi.md#clockOutTimeEntry) | **PATCH** /api/v1/time-entries/{id} | Clock out an entry: the entry&#39;s owner, or anyone with &#x60;time_entries:write&#x60;. |
| [**getLaborCosts()**](TimeEntriesApi.md#getLaborCosts) | **GET** /api/v1/labor-costs | Labor-cost report: worked hours aggregated per employee / order / day, valued at the employee&#39;s hourly cost rate. |
| [**listTimeEntries()**](TimeEntriesApi.md#listTimeEntries) | **GET** /api/v1/time-entries | List time entries with optional date-range / active / employee filters. |


## `clockInTimeEntry()`

```php
clockInTimeEntry($time_entry_clock_in): \OpenAPI\Client\Model\TimeEntryDto
```

Clock in for the authenticated user (resolved via their employee profile).

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure Bearer (JWT) authorization: bearer_token
$config = OpenAPI\Client\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new OpenAPI\Client\Api\TimeEntriesApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$time_entry_clock_in = new \OpenAPI\Client\Model\TimeEntryClockIn(); // \OpenAPI\Client\Model\TimeEntryClockIn

try {
    $result = $apiInstance->clockInTimeEntry($time_entry_clock_in);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling TimeEntriesApi->clockInTimeEntry: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **time_entry_clock_in** | [**\OpenAPI\Client\Model\TimeEntryClockIn**](../Model/TimeEntryClockIn.md)|  | |

### Return type

[**\OpenAPI\Client\Model\TimeEntryDto**](../Model/TimeEntryDto.md)

### Authorization

[bearer_token](../../README.md#bearer_token)

### HTTP request headers

- **Content-Type**: `application/json`
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `clockOutTimeEntry()`

```php
clockOutTimeEntry($id, $time_entry_clock_out): \OpenAPI\Client\Model\TimeEntryDto
```

Clock out an entry: the entry's owner, or anyone with `time_entries:write`.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure Bearer (JWT) authorization: bearer_token
$config = OpenAPI\Client\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new OpenAPI\Client\Api\TimeEntriesApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$id = 'id_example'; // string
$time_entry_clock_out = new \OpenAPI\Client\Model\TimeEntryClockOut(); // \OpenAPI\Client\Model\TimeEntryClockOut

try {
    $result = $apiInstance->clockOutTimeEntry($id, $time_entry_clock_out);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling TimeEntriesApi->clockOutTimeEntry: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **id** | **string**|  | |
| **time_entry_clock_out** | [**\OpenAPI\Client\Model\TimeEntryClockOut**](../Model/TimeEntryClockOut.md)|  | |

### Return type

[**\OpenAPI\Client\Model\TimeEntryDto**](../Model/TimeEntryDto.md)

### Authorization

[bearer_token](../../README.md#bearer_token)

### HTTP request headers

- **Content-Type**: `application/json`
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `getLaborCosts()`

```php
getLaborCosts($from, $to, $group_by): \OpenAPI\Client\Model\LaborCostRow[]
```

Labor-cost report: worked hours aggregated per employee / order / day, valued at the employee's hourly cost rate.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure Bearer (JWT) authorization: bearer_token
$config = OpenAPI\Client\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new OpenAPI\Client\Api\TimeEntriesApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$from = new \DateTime('2013-10-20T19:20:30+01:00'); // \DateTime
$to = new \DateTime('2013-10-20T19:20:30+01:00'); // \DateTime
$group_by = 'group_by_example'; // string | One of \"employee\", \"order\" or \"day\".

try {
    $result = $apiInstance->getLaborCosts($from, $to, $group_by);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling TimeEntriesApi->getLaborCosts: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **from** | **\DateTime**|  | |
| **to** | **\DateTime**|  | |
| **group_by** | **string**| One of \&quot;employee\&quot;, \&quot;order\&quot; or \&quot;day\&quot;. | |

### Return type

[**\OpenAPI\Client\Model\LaborCostRow[]**](../Model/LaborCostRow.md)

### Authorization

[bearer_token](../../README.md#bearer_token)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `listTimeEntries()`

```php
listTimeEntries($from, $to, $active, $employee_id): \OpenAPI\Client\Model\TimeEntryDto[]
```

List time entries with optional date-range / active / employee filters.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure Bearer (JWT) authorization: bearer_token
$config = OpenAPI\Client\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new OpenAPI\Client\Api\TimeEntriesApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$from = new \DateTime('2013-10-20T19:20:30+01:00'); // \DateTime
$to = new \DateTime('2013-10-20T19:20:30+01:00'); // \DateTime
$active = True; // bool | Only currently running shifts (clock_in set, clock_out null).
$employee_id = 'employee_id_example'; // string

try {
    $result = $apiInstance->listTimeEntries($from, $to, $active, $employee_id);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling TimeEntriesApi->listTimeEntries: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **from** | **\DateTime**|  | [optional] |
| **to** | **\DateTime**|  | [optional] |
| **active** | **bool**| Only currently running shifts (clock_in set, clock_out null). | [optional] |
| **employee_id** | **string**|  | [optional] |

### Return type

[**\OpenAPI\Client\Model\TimeEntryDto[]**](../Model/TimeEntryDto.md)

### Authorization

[bearer_token](../../README.md#bearer_token)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)
