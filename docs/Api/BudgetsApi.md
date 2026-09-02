# OpenAPI\Client\BudgetsApi



All URIs are relative to https://demo.simplebilly.com, except if the operation defines another base path.

| Method | HTTP request | Description |
| ------------- | ------------- | ------------- |
| [**budgetsApi()**](BudgetsApi.md#budgetsApi) | **GET** /api/v1/bookkeeping/budgets |  |
| [**upsertBudgetGoalApi()**](BudgetsApi.md#upsertBudgetGoalApi) | **PUT** /api/v1/bookkeeping/budgets/goals/{category} |  |


## `budgetsApi()`

```php
budgetsApi($year, $month): \OpenAPI\Client\Model\BudgetErgebnis
```



### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure Bearer (JWT) authorization: bearer_token
$config = OpenAPI\Client\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new OpenAPI\Client\Api\BudgetsApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$year = 56; // int
$month = 56; // int

try {
    $result = $apiInstance->budgetsApi($year, $month);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling BudgetsApi->budgetsApi: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **year** | **int**|  | |
| **month** | **int**|  | |

### Return type

[**\OpenAPI\Client\Model\BudgetErgebnis**](../Model/BudgetErgebnis.md)

### Authorization

[bearer_token](../../README.md#bearer_token)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `upsertBudgetGoalApi()`

```php
upsertBudgetGoalApi($category, $budget_goal_request): \OpenAPI\Client\Model\Budget
```



### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure Bearer (JWT) authorization: bearer_token
$config = OpenAPI\Client\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new OpenAPI\Client\Api\BudgetsApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$category = 'category_example'; // string
$budget_goal_request = new \OpenAPI\Client\Model\BudgetGoalRequest(); // \OpenAPI\Client\Model\BudgetGoalRequest

try {
    $result = $apiInstance->upsertBudgetGoalApi($category, $budget_goal_request);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling BudgetsApi->upsertBudgetGoalApi: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **category** | **string**|  | |
| **budget_goal_request** | [**\OpenAPI\Client\Model\BudgetGoalRequest**](../Model/BudgetGoalRequest.md)|  | |

### Return type

[**\OpenAPI\Client\Model\Budget**](../Model/Budget.md)

### Authorization

[bearer_token](../../README.md#bearer_token)

### HTTP request headers

- **Content-Type**: `application/json`
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)
