
# Subscriber Request

The subscriber request information .

## Structure

`SubscriberRequest`

## Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `name` | [`Name`](../../doc/models/name.md) | Optional | The name of the party. |
| `phone` | [`PhoneWithType`](../../doc/models/phone-with-type.md) | Optional | The phone information. |
| `shipping_address` | [`ShippingDetails`](../../doc/models/shipping-details.md) | Optional | The shipping details. |
| `payment_source` | [`SubscriptionPaymentSource`](../../doc/models/subscription-payment-source.md) | Optional | The payment source definition. To be eligible to create subscription using debit or credit card, you will need to sign up here (https://www.paypal.com/bizsignup/entry/product/ppcp). Please note, its available only for non-3DS cards and for merchants in US and AU regions. |

## Example

```python
from paypalserversdk.models.card_type import CardType
from paypalserversdk.models.fulfillment_type import FulfillmentType
from paypalserversdk.models.money import Money
from paypalserversdk.models.name import Name
from paypalserversdk.models.phone_number import PhoneNumber
from paypalserversdk.models.phone_number_with_country_code import PhoneNumberWithCountryCode
from paypalserversdk.models.phone_type import PhoneType
from paypalserversdk.models.phone_with_type import PhoneWithType
from paypalserversdk.models.shipping_details import ShippingDetails
from paypalserversdk.models.shipping_name import ShippingName
from paypalserversdk.models.shipping_option import ShippingOption
from paypalserversdk.models.shipping_type import ShippingType
from paypalserversdk.models.subscriber_request import SubscriberRequest
from paypalserversdk.models.subscription_card_request import SubscriptionCardRequest
from paypalserversdk.models.subscription_payment_source import SubscriptionPaymentSource

subscriber_request = SubscriberRequest(
    name=Name(
        given_name='given_name2',
        surname='surname8'
    ),
    phone=PhoneWithType(
        phone_number=PhoneNumber(
            national_number='national_number6'
        ),
        phone_type=PhoneType.OTHER
    ),
    shipping_address=ShippingDetails(
        name=ShippingName(
            full_name='full_name6'
        ),
        email_address='email_address8',
        phone_number=PhoneNumberWithCountryCode(
            country_code='country_code2',
            national_number='national_number6'
        ),
        mtype=FulfillmentType.PICKUP_IN_STORE,
        options=[
            ShippingOption(
                id='id2',
                label='label2',
                selected=False,
                mtype=ShippingType.SHIPPING,
                amount=Money(
                    currency_code='currency_code6',
                    value='value0'
                )
            )
        ]
    ),
    payment_source=SubscriptionPaymentSource(
        card=SubscriptionCardRequest(
            name='name6',
            number='number6',
            expiry='expiry4',
            security_code='security_code8',
            mtype=CardType.UNKNOWN
        )
    )
)
```

