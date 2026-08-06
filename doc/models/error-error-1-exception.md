
# Error Error 1 Exception

The error details.

## Structure

`ErrorError1Exception`

## Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `name` | `str` | Required | The human-readable, unique name of the error. |
| `message` | `str` | Required | The message that describes the error. |
| `debug_id` | `str` | Required | The PayPal internal ID. Used for correlation purposes. |
| `details` | [`List[ErrorDetails1]`](../../doc/models/error-details-1.md) | Optional | An array of additional details about the error. |
| `links` | [`List[ErrorLinkDescription]`](../../doc/models/error-link-description.md) | Optional, Read-only | An array of request-related [HATEOAS links](/api/rest/responses/#hateoas-links). |

## Example

```python
try:
    # make the API call
except ErrorError1Exception as e:
    print(e)
except ApiException as e:
    print(e)
```

