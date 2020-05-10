# Org.OpenAPITools.Api.DefaultApi

All URIs are relative to *http://localhost*

Method | HTTP request | Description
------------- | ------------- | -------------
[**CreateNewModel**](DefaultApi.md#createnewmodel) | **PUT** /models | Create New Model
[**DeleteModel**](DefaultApi.md#deletemodel) | **DELETE** /models | Delete Model
[**GetModelsList**](DefaultApi.md#getmodelslist) | **GET** /models | Get Models List
[**TagImageByUrl**](DefaultApi.md#tagimagebyurl) | **GET** /predict_by_image_url | Tag Image by Using Image Url
[**TagLocalImage**](DefaultApi.md#taglocalimage) | **POST** /predict | Predict by Image
[**UpdateModel**](DefaultApi.md#updatemodel) | **POST** /models | Update Model



## CreateNewModel

> void CreateNewModel (string modelName)

Create New Model

Create a new custom image recognition model

### Example

```csharp
using System.Collections.Generic;
using System.Diagnostics;
using Org.OpenAPITools.Api;
using Org.OpenAPITools.Client;
using Org.OpenAPITools.Model;

namespace Example
{
    public class CreateNewModelExample
    {
        public static void Main()
        {
            Configuration.Default.BasePath = "http://localhost";
            // Configure API key authorization: x-api-key
            Configuration.Default.AddApiKey("x-api-key", "YOUR_API_KEY");
            // Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
            // Configuration.Default.AddApiKeyPrefix("x-api-key", "Bearer");

            var apiInstance = new DefaultApi(Configuration.Default);
            var modelName = {"model_name":"\"Test model name\""};  // string | Set a name for your model

            try
            {
                // Create New Model
                apiInstance.CreateNewModel(modelName);
            }
            catch (ApiException e)
            {
                Debug.Print("Exception when calling DefaultApi.CreateNewModel: " + e.Message );
                Debug.Print("Status Code: "+ e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **modelName** | **string**| Set a name for your model | 

### Return type

void (empty response body)

### Authorization

[x-api-key](../README.md#x-api-key)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: Not defined

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Successfully created |  -  |
| **400** | Bad request, parameter or format error. Please check your query. |  -  |
| **401** | You are not authorized to create a new model |  -  |

[[Back to top]](#)
[[Back to API list]](../README.md#documentation-for-api-endpoints)
[[Back to Model list]](../README.md#documentation-for-models)
[[Back to README]](../README.md)


## DeleteModel

> void DeleteModel (string modelId)

Delete Model

Delete Model

### Example

```csharp
using System.Collections.Generic;
using System.Diagnostics;
using Org.OpenAPITools.Api;
using Org.OpenAPITools.Client;
using Org.OpenAPITools.Model;

namespace Example
{
    public class DeleteModelExample
    {
        public static void Main()
        {
            Configuration.Default.BasePath = "http://localhost";
            // Configure API key authorization: x-api-key
            Configuration.Default.AddApiKey("x-api-key", "YOUR_API_KEY");
            // Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
            // Configuration.Default.AddApiKeyPrefix("x-api-key", "Bearer");

            var apiInstance = new DefaultApi(Configuration.Default);
            var modelId = modelId_example;  // string | You can find your model ids from Classify Dashboard.

            try
            {
                // Delete Model
                apiInstance.DeleteModel(modelId);
            }
            catch (ApiException e)
            {
                Debug.Print("Exception when calling DefaultApi.DeleteModel: " + e.Message );
                Debug.Print("Status Code: "+ e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **modelId** | **string**| You can find your model ids from Classify Dashboard. | 

### Return type

void (empty response body)

### Authorization

[x-api-key](../README.md#x-api-key)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: Not defined

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Successfully Deleted. |  -  |
| **400** | Bad request, parameter or format error. please check your query. |  -  |
| **401** | You are not authorized to delete this model. |  -  |

[[Back to top]](#)
[[Back to API list]](../README.md#documentation-for-api-endpoints)
[[Back to Model list]](../README.md#documentation-for-models)
[[Back to README]](../README.md)


## GetModelsList

> void GetModelsList ()

Get Models List

Get the list of of models created 

### Example

```csharp
using System.Collections.Generic;
using System.Diagnostics;
using Org.OpenAPITools.Api;
using Org.OpenAPITools.Client;
using Org.OpenAPITools.Model;

namespace Example
{
    public class GetModelsListExample
    {
        public static void Main()
        {
            Configuration.Default.BasePath = "http://localhost";
            // Configure API key authorization: x-api-key
            Configuration.Default.AddApiKey("x-api-key", "YOUR_API_KEY");
            // Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
            // Configuration.Default.AddApiKeyPrefix("x-api-key", "Bearer");

            var apiInstance = new DefaultApi(Configuration.Default);

            try
            {
                // Get Models List
                apiInstance.GetModelsList();
            }
            catch (ApiException e)
            {
                Debug.Print("Exception when calling DefaultApi.GetModelsList: " + e.Message );
                Debug.Print("Status Code: "+ e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

### Parameters

This endpoint does not need any parameter.

### Return type

void (empty response body)

### Authorization

[x-api-key](../README.md#x-api-key)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Query executed succesfully. |  -  |
| **204** | No projects created yet. |  -  |
| **401** | You don&#39;t have authorization to get the model list. |  -  |

[[Back to top]](#)
[[Back to API list]](../README.md#documentation-for-api-endpoints)
[[Back to Model list]](../README.md#documentation-for-models)
[[Back to README]](../README.md)


## TagImageByUrl

> void TagImageByUrl (string modelId, string imageUrl)

Tag Image by Using Image Url

Predict image tags by providing image url

### Example

```csharp
using System.Collections.Generic;
using System.Diagnostics;
using Org.OpenAPITools.Api;
using Org.OpenAPITools.Client;
using Org.OpenAPITools.Model;

namespace Example
{
    public class TagImageByUrlExample
    {
        public static void Main()
        {
            Configuration.Default.BasePath = "http://localhost";
            // Configure API key authorization: x-api-key
            Configuration.Default.AddApiKey("x-api-key", "YOUR_API_KEY");
            // Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
            // Configuration.Default.AddApiKeyPrefix("x-api-key", "Bearer");

            var apiInstance = new DefaultApi(Configuration.Default);
            var modelId = modelId_example;  // string | Type your trained model id to predict. You get your model's id from Classify Dashboard.
            var imageUrl = imageUrl_example;  // string | Provide image url to predict

            try
            {
                // Tag Image by Using Image Url
                apiInstance.TagImageByUrl(modelId, imageUrl);
            }
            catch (ApiException e)
            {
                Debug.Print("Exception when calling DefaultApi.TagImageByUrl: " + e.Message );
                Debug.Print("Status Code: "+ e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **modelId** | **string**| Type your trained model id to predict. You get your model&#39;s id from Classify Dashboard. | 
 **imageUrl** | **string**| Provide image url to predict | 

### Return type

void (empty response body)

### Authorization

[x-api-key](../README.md#x-api-key)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Custom trained model prediction response. |  -  |
| **400** | Bad request, parameter or format error. Please check your query, image format and image size. |  -  |
| **401** | You are not authorized for this operation. |  -  |

[[Back to top]](#)
[[Back to API list]](../README.md#documentation-for-api-endpoints)
[[Back to Model list]](../README.md#documentation-for-models)
[[Back to README]](../README.md)


## TagLocalImage

> void TagLocalImage (string modelId, System.IO.Stream file = null)

Predict by Image

Send a local image to tag

### Example

```csharp
using System.Collections.Generic;
using System.Diagnostics;
using Org.OpenAPITools.Api;
using Org.OpenAPITools.Client;
using Org.OpenAPITools.Model;

namespace Example
{
    public class TagLocalImageExample
    {
        public static void Main()
        {
            Configuration.Default.BasePath = "http://localhost";
            // Configure API key authorization: x-api-key
            Configuration.Default.AddApiKey("x-api-key", "YOUR_API_KEY");
            // Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
            // Configuration.Default.AddApiKeyPrefix("x-api-key", "Bearer");

            var apiInstance = new DefaultApi(Configuration.Default);
            var modelId = modelId_example;  // string | Type your trained model id to predict. You get your model's id from Classify Dashboard.
            var file = BINARY_DATA_HERE;  // System.IO.Stream |  (optional) 

            try
            {
                // Predict by Image
                apiInstance.TagLocalImage(modelId, file);
            }
            catch (ApiException e)
            {
                Debug.Print("Exception when calling DefaultApi.TagLocalImage: " + e.Message );
                Debug.Print("Status Code: "+ e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **modelId** | **string**| Type your trained model id to predict. You get your model&#39;s id from Classify Dashboard. | 
 **file** | **System.IO.Stream**|  | [optional] 

### Return type

void (empty response body)

### Authorization

[x-api-key](../README.md#x-api-key)

### HTTP request headers

- **Content-Type**: multipart/form-data
- **Accept**: application/json

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Custom trained model prediction response. |  -  |
| **400** | Bad request, parameter or format error. Please check your query, image format and image size. |  -  |
| **401** | You are not authorized for this operation. |  -  |

[[Back to top]](#)
[[Back to API list]](../README.md#documentation-for-api-endpoints)
[[Back to Model list]](../README.md#documentation-for-models)
[[Back to README]](../README.md)


## UpdateModel

> void UpdateModel (string modelName, string modelId)

Update Model

Update Model Name

### Example

```csharp
using System.Collections.Generic;
using System.Diagnostics;
using Org.OpenAPITools.Api;
using Org.OpenAPITools.Client;
using Org.OpenAPITools.Model;

namespace Example
{
    public class UpdateModelExample
    {
        public static void Main()
        {
            Configuration.Default.BasePath = "http://localhost";
            // Configure API key authorization: x-api-key
            Configuration.Default.AddApiKey("x-api-key", "YOUR_API_KEY");
            // Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
            // Configuration.Default.AddApiKeyPrefix("x-api-key", "Bearer");

            var apiInstance = new DefaultApi(Configuration.Default);
            var modelName = modelName_example;  // string | Model Name
            var modelId = modelId_example;  // string | Model id to be renamed.

            try
            {
                // Update Model
                apiInstance.UpdateModel(modelName, modelId);
            }
            catch (ApiException e)
            {
                Debug.Print("Exception when calling DefaultApi.UpdateModel: " + e.Message );
                Debug.Print("Status Code: "+ e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **modelName** | **string**| Model Name | 
 **modelId** | **string**| Model id to be renamed. | 

### Return type

void (empty response body)

### Authorization

[x-api-key](../README.md#x-api-key)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: Not defined

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Successfull |  -  |
| **400** | Bad request, parameter or format error. Please check your query. |  -  |
| **401** | You are not authorized to edit this model. |  -  |

[[Back to top]](#)
[[Back to API list]](../README.md#documentation-for-api-endpoints)
[[Back to Model list]](../README.md#documentation-for-models)
[[Back to README]](../README.md)
