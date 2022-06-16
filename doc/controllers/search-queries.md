# Search Queries

```python
search_queries_controller = client.search_queries
```

## Class Name

`SearchQueriesController`


# Search

```python
def search(self,
          part,
          q)
```

## Parameters

| Parameter | Type | Tags | Description |
|  --- | --- | --- | --- |
| `part` | `string` | Query, Required | The part parameter specifies a comma-separated list of one or more search resource properties that the API response will include. Set the parameter value to snippet. |
| `q` | `string` | Query, Required | The q parameter specifies the query term to search for.  Your request can also use the Boolean NOT (-) and OR (\|) operators to exclude videos or to find videos that are associated with one of several search terms. For example, to search for videos matching either "boating" or "sailing", set the q parameter value to boating\|sailing. Similarly, to search for videos matching either "boating" or "sailing" but not "fishing", set the q parameter value to boating\|sailing -fishing. Note that the pipe character must be URL-escaped when it is sent in your API request. The URL-escaped value for the pipe character is %7C. |

## Response Type

`string`

## Example Usage

```python
part = 'snippet'
q = 'q0'

result = search_queries_controller.search(part, q)
```

## Errors

| HTTP Status Code | Error Description | Exception Class |
|  --- | --- | --- |
| 404 | There was a problem in your input. | `APIException` |

