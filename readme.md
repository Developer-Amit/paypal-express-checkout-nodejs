PayPal Express Checkout Node.js
===============================

* Easy to use
* __No dependencies__
* [Full source-code of the eshop with PayPal written in node.js](http://www.totaljs.com/eshop/)

PayPal account
--------------

Read here: <https://developer.paypal.com/docs/classic/api/apiCredentials/#creating-an-api-signature>

- Log in to your PayPal business account at www.paypal.com. Click the profile icon ( Profile menu ) on the top right side of the page. From the Business Profile menu, select Profile and Settings.
- From the left menu, click My selling tools.
- In the Selling online section, click the Update link for the API access item.
- To generate the API signature, click Request API Credentials on the API Access page. ![Request API credentials](https://www.paypalobjects.com/webstatic/en_US/developer/docs/api/classicApiCerts/requestApiCreds.png)
- Select Request API signature and click Agree and Submit to generate the API signature. ![Signature](https://www.paypalobjects.com/webstatic/en_US/developer/docs/api/classicApiCerts/signatureCredentials.png)

***

```text
$ npm install paypal-express-checkout
```

***

## PayPal PAYMENTSTATUS

```
Canceled_Reversal: A reversal has been canceled. For example, you won a dispute with the customer, and the funds for the transaction that was reversed have been returned to you.
Completed: The payment has been completed, and the funds have been added successfully to your account balance.
Created: A German ELV payment is made using Express Checkout.
Denied: You denied the payment. This happens only if the payment was previously pending because of possible reasons described for the pending_reason variable or the Fraud_Management_Filters_x variable.
Expired: This authorization has expired and cannot be captured.
Failed: The payment has failed. This happens only if the payment was made from your customer’s bank account.
Pending: The payment is pending. See pending_reason for more information.
Refunded: You refunded the payment.
Reversed: A payment was reversed due to a chargeback or other type of reversal. The funds have been removed from your account balance and returned to the buyer. The reason for the reversal is specified in the ReasonCode element.
Processed: A payment has been accepted.
Voided: This authorization has been voided.
```

## How to prevent of pending paymentstatus?

> Login into your bussiness account and click here: https://www.sandbox.paypal.com/ca/cgi-bin/?cmd=_profile-pref&source=acct_setup&fli=true
