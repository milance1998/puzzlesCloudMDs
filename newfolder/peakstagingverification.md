Staging environments are protected with client certificate that can be obtained from your administrator and imported into browser.

Staging environments are connected with Mimas **production** environment and Adyen **test** environment. This means that products can be purchased with test cards.

After product purchase, cards needs to be cancelled from Mimas by providing values of `serial-number` and `batch-number` from order details.

They can be obtained from API response `/api/rest/v1/voucher-orders/{order-uuid}`. For example:

```json
{
  "data": {
    "type": "voucher-order",
    "id": "4efe4d2f-169a-4bac-a477-3c6e20cbc5d9",
    "attributes": {
      "notification-status": "delivered",
      "confirmation-status": "none",
      "notification-target": "ivica.vojinovic@gmail.com",
      "notification-type": "email",
      "order-fee-total": 1.95,
      "order-price-total": 16.95,
      "order-status": "pending",
      "order-tax-total": 0,
      "payment-method": "adyen mastercard",
      "payment-provider": "adyen",
      "payment-redirect-url": "",
      "payment-session-id": "863614938877300F",
      "payment-status": "reserved",
      "voucher-code": "TMOBDE15",
      "voucher-currency": "EUR",
      "voucher-status": "reserved",
      "voucher-value": 15,
      "created-date": 1614938858275,
      "short-id": "rp4N6r",
      "serial-number": "5699900436315",
      "provider-code": "TELECOM-D1",
      "confirmation-date": 0,
      "batch-number": "9828924414"
    }
  }
}
```

Staging environment deployments:

* DE - https://staging.de.www.shop1.rocks/
* CZ - https://staging.cz.www.shop1.rocks/
* PL - https://staging.pl.www.shop1.rocks/

#### Verification for DE shop

Products from **Prepaid-Aufladung** (Prepaid Cards) can be used for verification.

Product details, `serial-number` and `batch-number` should be sent to christiane.beyer@icp-innovation.lu and Holger.Krause@icp-innovation.lu for cancellation. Do not send the actual activation code, nor the screenshot of that page.

#### Verification for CZ shop

**Dárkové karty/Vivantis**, **Hry & Zábava/Xbox** and **Paysafecard/Paysafecard** can be used for verification.

Product details, `serial-number` and `batch-number` should be sent to christiane.beyer@icp-innovation.lu and Holger.Krause@icp-innovation.lu for cancellation. Do not send the actual activation code, nor the screenshot of that page.

#### Verification for PL shop

**Gry i rozrywka/Cda 20**, **Paysafecard/Paysafecard 20**, **Doładowania/Orange 10** and **Karty Podarunkowe/Answear 100** can be used for verification.

Product details, `serial-number` and `batch-number` should be sent to christiane.beyer@icp-innovation.lu and Holger.Krause@icp-innovation.lu for cancellation. Only send the actual activation code and the screenshot of the code delivery page in case of Paysafecard purchase (in other cases the activation code is not to be shared).