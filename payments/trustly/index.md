---
title: Swedbank Pay Payments Trustly
sidebar:
  navigation:
  - title: Trustly Payments
    items:
    - url: /payments/trustly
      title: Introduction
    - url: /payments/trustly/redirect
      title: Redirect
    - url: /payments/trustly/seamless-view
      title: Seamless View
    - url: /payments/trustly/after-payment
      title: After Payment
    - url: /payments/trustly/other-features
      title: Other Features
---

{% include alert-review-section.md %}

{% include jumbotron.html body="  100+ banks from 29 countries in one payment
instrument. " %}

Trustly Payments is a Direct Debit payment instrument which gathers over 100
banks from 29 European countries in one solution, making the payment easier for
both the consumers and you as a merchant. The consumers are likely to find their
bank of choice, and you as a merchant will only need one Direct Debit
integration. We offer it for both our Redirect and Seamless View platforms.

## Purchase flow

After the payment has been created, the payer is redirected to the payment page
(redirect) or it will appear in an `iframe` (Seamless View). The payer proceeds
to enter his or her's first and last name, before being redirected to
Trustly's payment page.

![screenshot of the Trustly name input page][trustly-name-input]{:height="500px" width="450px"}

Upon arriving at Trustly's payment page, the payer is asked to enter his or
her's Social Security Number and log in using BankID.

![screenshot of the Trustly social security number input page][trustly-ssn-input]{:height="360px" width="600px"}

The payer is redirected to a select a bank.

![screenshot of the Trustly BankID login page][trustly-bank-select]{:height="360px" width="600px"}

After selecting bank, the payer needs to choose which account the funds should
be drawn from, and confirm the payment with another BankID authentication.

![screenshot of the Trustly account selection page][trustly-account-select]{:height="600px" width="425px"}

![screenshot of the Trustly BankID payment authentication][trustly-bankid-authentication]{:height="600px" width="425px"}

The payer is then redirected back to the merchant.

## Good To Know

### Payment Type

Trustly is a Direct Debit payment instrument using one-phase payments. The
`sale` is done when the consumer successfully confirms in the app, capturing the
funds instantly. The `abort` operation is still available, but the `cancel` and
`capture` operations are not. The `reversal`, if this option is available for
the selected bank, is done by the merchant at a later time. Read more about the
[different operations][after-payment] and the [payment
resource][payment-resource]. 

### Demoshop

Trustly is unfortunately not available in our demoshop at the moment, but it
will be in the future. The demoshop in the test environments will use a
fakeservice which enables you to test a successful purchase without using the
MobilePay app.

{% include iterator.html
                         next_href="redirect"
                         next_title="Next: Redirect" %}

[trustly-name-input]: /assets/img/payments/.png
[trustly-ssn-input]: /assets/img/payments/.png
[trustly-bankid-input]: /assets/img/payments/.png
[trustly-account-select]: /assets/img/payments/.png
[payment-resource]: /payments/trustly/other-features#payment-resource
[other-features]: /payments/trustly/other-features#operations