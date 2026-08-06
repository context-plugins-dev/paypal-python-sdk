
# Error 1

The error details.

## Structure

`Error1`

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
from paypalserversdk.models.error_1 import Error1
from paypalserversdk.models.error_details_1 import ErrorDetails1
from paypalserversdk.models.error_link_description import ErrorLinkDescription
from paypalserversdk.models.link_http_method import LinkHttpMethod

error_1 = Error1(
    name='name6',
    message='message6',
    debug_id='debug_id8',
    details=[
        ErrorDetails1(
            issue='issue6',
            field='field4',
            value='value2',
            location='location4',
            links=[
                ErrorLinkDescription(
                    href='href6',
                    rel='rel0',
                    method=LinkHttpMethod.HEAD
                ),
                ErrorLinkDescription(
                    href='href6',
                    rel='rel0',
                    method=LinkHttpMethod.HEAD
                )
            ],
            description='description0'
        ),
        ErrorDetails1(
            issue='issue6',
            field='field4',
            value='value2',
            location='location4',
            links=[
                ErrorLinkDescription(
                    href='href6',
                    rel='rel0',
                    method=LinkHttpMethod.HEAD
                ),
                ErrorLinkDescription(
                    href='href6',
                    rel='rel0',
                    method=LinkHttpMethod.HEAD
                )
            ],
            description='description0'
        )
    ],
    links=[
        ErrorLinkDescription(
            href='href6',
            rel='rel0',
            method=LinkHttpMethod.HEAD
        ),
        ErrorLinkDescription(
            href='href6',
            rel='rel0',
            method=LinkHttpMethod.HEAD
        )
    ]
)
```

