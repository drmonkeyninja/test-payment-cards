Test Payment Cards
==================

A list of available test payment cards for various payment gateways. Please feel free to contribute cards for any payment gateways not currently listed here by making a pull request.

## Table of Contents

- [Payment Gateways](#payment-gateways)
    - [Authorize.Net](#authorizenet)
    - [Ogone](#ogone)
    - [PayPal](#paypal)
    - [RedSys](#redsys)
    - [Saferpay](#saferpay)
    - [SagePay](#sagepay)
    - [Stripe](#stripe)
    - [WePay](#wepay)
    - [WorldPay](#worldpay)
- [License](#license)

## Payment Gateways

Most payment gateways will accept any date set in the future for the card expiry date unless specified differently below.

### Authorize.Net

The following test credit card numbers will only work in the Authorize.Net sandbox. If the card code is required use any 3-digit combination except for American Express which requires a 4-digit combination. See the [Authorize.Net Testing Guide](http://developer.authorize.net/hello_world/testing_guide/) for further details.

Card Type                 | Card Number(s)
:-------------------------|:--------------------------------------------------
American Express          | 370000000000002
Diners Club/ Carte Blanch | 38000000000006
Discover                  | 6011000000000012
JCB                       | 3088000000000017
MasterCard                | 5424000000000015
Visa                      | 4007000000027, 4012888818888 and 4111111111111111

### Ogone

Card Type | Card Number
:---------|:----------------
Visa      | 4111111111111111

Details about using test cards in Ogone can be found here: [Create and configure your Ogone Test Account](https://payment-services.ingenico.com/int/en/ogone/support/guides/user%20guides/test-account-creation).

### PayPal

Card Type                  | Card Number(s)
:--------------------------|:-----------------------------------------------------
American Express           | 378282246310005 and 371449635398431
American Express Corporate | 378734493671000
Australian BankCard        | 5610591081018250
Diners Club                | 30569309025904 and 38520000023237
Discover                   | 6011111111111117 and 6011000990139424
JCB                        | 3530111333300000 and 3566002020360505
MasterCard                 | 5555555555554444 and 5105105105105100
Visa                       | 4111111111111111, 4012888888881881 and 4222222222222

### RedSys

Card Number      | Expiration | CVV2 | CIP Code
:----------------|:-----------|:-----|:---------
4548812049400004 | 12/20      | 123  | 123456

### Saferpay

Card Number      | Description
:----------------|:--------------------------------------------------------------------------------------------------
9451123100000111 | Saferpay test card "enrolled", returns `ECI=1`. Test card for 3D-Secure processing.
9451123100000004 | Saferpay test card "not enrolled", returns `ECI=2`. Normal test card without 3D-Secure processing.
9451123100000202 | Saferpay test card "unable to enroll", returns `ECI=0`. Test card for SSL processing only.
9451123100000103 | Saferpay test card "Result".

**Test card for special Result codes.**

The last two digits of the AMOUNT attributes define the result code of the authorization response. Only if the last two digits of the value are set to "00" or "01" will payment be authorized. In doing so requests with AMOUNT "00" receive `ECI=1` in the response, which means the 3-D Secure liability shift is given whilst a liability shift is not applicable for requests with AMOUNT "01" receiving `ECI=0` in the response. For all other requests where AMOUNT is not "00" or "01" Saferpay will send an answer with `RESULT="65"` where AUTHRESULT will contain the error code.

### SagePay

Card Type               | Card Number         | Issue | CV2
:-----------------------|:--------------------|:------|:---
American Express        | 374200000000004     |       | 123
Diner's Club            | 36000000000008      |       | 123
JCB                     | 3569990000000009    |       | 123
Laser                   | 6304990000000000044 |       | 123
Maestro (UK)            | 5641820000000005    | 01    | 123
Maestro (International) | 300000000000000004  |       | 123
MasterCard              | 5404000000000001    |       | 123
Visa                    | 4929000000006       |       | 123
Visa Debit / Delta      | 4462000000000003    |       | 123
Visa Electron           | 4917300000000008    |       | 123

All test cards use the address "88" and postcode "412".

### Stripe

Full details of Stipe's test cards can be found on their [Testing](https://stripe.com/docs/testing) page of their documentation.

Card Type            | Card Number
:--------------------|:--------------------------------------
American Express     | 378282246310005 and 371449635398431
Diners Club          | 30569309025904 and 38520000023237
Discover             | 6011111111111117 and 6011000990139424
JCB                  | 3530111333300000 and 3566002020360505
MasterCard           | 5555555555554444
MasterCard (Debit)   | 5200828282828210
MasterCard (Prepaid) | 5105105105105100
Visa                 | 4242424242424242 and 4012888888881881
Visa (Debit)         | 4000056655665556

### WePay

Full details of WePay's test cards can be found on their [Testing](https://www.wepay.com/developer/reference/testing) page of their documentation.

Card Type            | Card Number
:--------------------|:-----------------------------------
American Express     | 378282246310005 and 371449635398431
MasterCard           | 5496198584584769
Visa                 | 4003830171874018

### WorldPay

WorldPay test cards do not have a card verification code and issue number.

Card Type               | Card Number(s)
:-----------------------|:----------------------------------------------------
Airplus                 | 122000000000003
American Express        | 34343434343434
Cartebleue              | 5555555555554444
Dankort                 | 5019717010103742
Diners                  | 36700102000000 and 36148900647913
Discover card           | 6011000400000000
JCB                     | 3528000700000000
Laser                   | 630495060000000000 and 630490017740292441
Maestro                 | 6759649826438453 and 67999990100000000019
MasterCard              | 5555555555554444 and 5454545454545454
Visa                    | 4444333322221111, 4911830000000 and 4917610000000000
Visa Debit              | 4462030000000000 and 4917610000000000003
Visa Electron (UK only) | 4917300800000000
Visa Purchasing         | 4484070000000000

## License

[![license](https://i.creativecommons.org/l/by-sa/4.0/88x31.png)](http://creativecommons.org/licenses/by-sa/4.0/)

This work is licensed under a [Creative Commons Attribution-ShareAlike 4.0 International License](http://creativecommons.org/licenses/by-sa/4.0/).
