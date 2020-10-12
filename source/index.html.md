---
title: API Reference

language_tabs: # must be one of https://git.io/vQNgJ
  - shell
  - python
  - javascript
  - http
  - java


includes:
  - errors

search: true

code_clipboard: true
---

# PayGv2 Documentation

version : V1

baseUri : uatapi.payg.in/payment/api/order/

protocols : HTTPS

mediaType : application/json

# Description

Simplify and grow your business.With the easiest integration and best in class payment solutions, experience seamless transactions with PayG. Check daily transactions and settlement details, generate instant refunds, access all payment features from a single powerful dashboard.
> /create post:


```python
# PYTHON EXAMPLE

import http.client
```

```shell
# CURL EXAMPLE

curl -X POST "uatapi.payg.in/payment/api/order/create" \
    -H "Authorization: key:"Authorization" value:"OTcwNDU0MTVkMzkyNDlhODk5NmM0MmUxYzk1OThlZDE6NDNiNDI1YTYxNDhiNGQ5NDk4YTQ5YmU2MTMyMThkYjc6TTo3ODc1"" \
    -d @request_body
```

```javascript
# JAVASCRIPT EXAMPLE

const headers = new Headers();
```

```http
# HTTP EXAMPLE

POST /payment/api/order/create HTTP/1.1
Host: uatapi.payg.in:443
```

```java
# java EXAMPLE

RestTemplate rest = new RestTemplate();
HttpHeaders headers = new HttpHeaders();
```
# / Create

## /Create post

POST: /create

# Header Parameters
> REQUEST HEADERS


```python
headers = {'Authorization': 'key:"Authorization" value:"OTcwNDU0MTVkMzkyNDlhODk5NmM0MmUxYzk1OThlZDE6NDNiNDI1YTYxNDhiNGQ5NDk4YTQ5YmU2MTMyMThkYjc6TTo3ODc1"'}
```

```shell
Authorization: key:"Authorization" value:"OTcwNDU0MTVkMzkyNDlhODk5NmM0MmUxYzk1OThlZDE6NDNiNDI1YTYxNDhiNGQ5NDk4YTQ5YmU2MTMyMThkYjc6TTo3ODc1"
```

```javascript
headers.append('Authorization', 'key:"Authorization" value:"OTcwNDU0MTVkMzkyNDlhODk5NmM0MmUxYzk1OThlZDE6NDNiNDI1YTYxNDhiNGQ5NDk4YTQ5YmU2MTMyMThkYjc6TTo3ODc1"');
```

```http
Authorization: key:"Authorization" value:"OTcwNDU0MTVkMzkyNDlhODk5NmM0MmUxYzk1OThlZDE6NDNiNDI1YTYxNDhiNGQ5NDk4YTQ5YmU2MTMyMThkYjc6TTo3ODc1"
```

```java
headers.add("Authorization", "key:"Authorization" value:"OTcwNDU0MTVkMzkyNDlhODk5NmM0MmUxYzk1OThlZDE6NDNiNDI1YTYxNDhiNGQ5NDk4YTQ5YmU2MTMyMThkYjc6TTo3ODc1"");
```
## Authorization

Property | Value 
--------- | -------
required | true 
type | string 
example | key:"Authorization" value:"OTcwNDU0MTVkMzkyNDlhODk5NmM0MmUxYzk1OThlZDE6NDNiNDI1YTYxNDhiNGQ5NDk4YTQ5YmU2MTMyMThkYjc6TTo3ODc1"
> REQUEST BODY:

```python
body = """{
  "MerchantKeyId": 292,
  "AuthenticationKey": "12959e563133424a9576e541c2670a83",
  "AuthenticationToken": "ca66b41b8e4f4187819d559a591ccfb7",
  "UniqueRequestId": "AA10030",
  "TransactionDate": {
    "PaymentType": "ALL"
  },
  "OrderAmount": 15,
  "OrderId": 225,
  "OrderAmountData": "12.00",
  "ProductData": {
    "ProductId": 1,
    "ProductDescription": "Test1",
    "Amount": 0,
    "Quantity": 0
  },
  "NextStepFlowData": {
    "RedirectLabel": "Test12",
    "Text": "Submit"
  },
  "TransactionType": "Charge",
  "CustomerData": {
    "CustomerId": 1,
    "FirstName": "test",
    "LastName": "m",
    "MobileNo": "33333333333",
    "email": "praveen@gmail.com",
    "EmailReceipt": false,
    "BillingAddress": "Telangana",
    "BillingCity": "test",
    "BillingState": "TS",
    "BillingCountry": "IN",
    "BillingZipCode": "TEST",
    "ShippingFirstName": "",
    "ShippingLastName": "",
    "ShippingAddress": "",
    "ShippingCity": "",
    "ShippingState": "",
    "ShippingCountry": "",
    "ShippingZipCode": "",
    "ShippingMobileNo": ""
  },
  "UserDefinedData": {
    "UserDefined1": "",
    "UserDefined2": "",
    "UserDefined3": "",
    "UserDefined4": "",
    "UserDefined5": "",
    "UserDefined6": "",
    "UserDefined7": "",
    "UserDefined8": "",
    "UserDefined9": "",
    "UserDefined10": "",
    "UserDefined11": "",
    "UserDefined12": "",
    "UserDefined13": "",
    "UserDefined14": "",
    "UserDefined15": "",
    "UserDefined16": "",
    "UserDefined17": "",
    "UserDefined18": "",
    "UserDefined19": "",
    "UserDefined20": ""
  },
  "RequestDateTime": "",
  "RedirectUrl": "https://payg.in"
}"""

conn = http.client.HTTPSConnection('uatapi.payg.in')
conn.request('POST','/payment/api/order/create', body, headers)
res = conn.getresponse()

data = res.read()
print(res.status, res.reason)
print(data.decode('utf-8'))
print(res.getheaders())
```

```shell
{
  "OrderKeyId": "",
  "MerchantKeyId": 2,
  "ApiKey": "",
  "UniqueRequestId": "ae021dg",
  "OrderAmount": 5,
  "OrderType": "",
  "OrderId": "",
  "OrderStatus": "",
  "OrderAmountData": {
    "AmountDetail": [
      {
        "AmountTypeDesc": "",
        "Amount": 0
      }
    ]
  },
  "ProductData": "",
  "NextStepFlowData": "",
  "TransactionData": {
    "AcceptedPaymentTypes": "",
    "PaymentType": "",
    "SurchargeType": "",
    "SurchargeValue": 0,
    "Card": {
      "CardNo": "",
      "CardType": 0,
      "NameOnCard": "",
      "ExpiryDate": "",
      "Cvv": "",
      "TrackData": "",
      "ChipData": "",
      "PassCode": "",
      "Ksn": "",
      "PinBlock": "",
      "AdditionalData1": "",
      "AdditionalData2": ""
    },
    "Ach": {
      "BankCodeType": 0,
      "BankCode": "",
      "AccountNo": "",
      "BankAccountType": 0,
      "CheckNo": "",
      "SecCode": 1,
      "MicrData": "",
      "CheckFrontImage": "",
      "CheckBackImage": "",
      "NameOnCard": "",
      "First6Digit": "",
      "Last4Digit": ""
    },
    "Wallet": {
      "BarQrCode": "",
      "UserName": "",
      "WalletType": 1,
      "FirstName": "",
      "LastName": ""
    },
    "Upi": {
      "Vpa": "",
      "AccountNumber": "",
      "Ifsc": "",
      "AdhAadhaarNo": ""
    },
    "Card3DSecure": {
      "AuthenticateTransaction": true,
      "Secure3DAuthenticationRequest": {
        "MD": "",
        "PaRes": ""
      }
    },
    "RefTransactionId": "",
    "IndustrySpecicationCode": "",
    "PartialPaymentOption": ""
  },
  "CustomerData": {
    "CustomerId": "12",
    "CustomerNotes": "Sample",
    "FirstName": "First",
    "LastName": "Last",
    "MobileNo": "9011001100",
    "Email": "test@gmail.com",
    "EmailReceipt": true,
    "BillingAddress": "",
    "BillingCity": "",
    "BillingState": "",
    "BillingCountry": "",
    "BillingZipCode": "",
    "ShippingFirstName": "",
    "ShippingLastName": "",
    "ShippingAddress": "",
    "ShippingCity": "",
    "ShippingState": "",
    "ShippingCountry": "",
    "ShippingZipCode": "",
    "ShippingMobileNo": ""
  },
  "UserDefinedData": {
    "UserDefined1": "",
    "UserDefined2": "",
    "UserDefined3": "",
    "UserDefined4": "",
    "UserDefined5": "",
    "UserDefined6": "",
    "UserDefined7": "",
    "UserDefined8": "",
    "UserDefined9": "",
    "UserDefined10": "",
    "UserDefined11": "",
    "UserDefined12": "",
    "UserDefined13": "",
    "UserDefined14": "",
    "UserDefined15": "",
    "UserDefined16": "",
    "UserDefined17": "",
    "UserDefined18": "",
    "UserDefined19": "",
    "UserDefined20": ""
  },
  "IntegrationData": {
    "UserName": "",
    "Source": "",
    "IntegrationType": "",
    "HashData": "",
    "PlatformId": ""
  },
  "ShipmentData": "",
  "RequestDateTime": "",
  "RedirectUrl": ""
}
```

```javascript
const body = `{
  "MerchantKeyId": 292,
  "AuthenticationKey": "12959e563133424a9576e541c2670a83",
  "AuthenticationToken": "ca66b41b8e4f4187819d559a591ccfb7",
  "UniqueRequestId": "AA10030",
  "TransactionDate": {
    "PaymentType": "ALL"
  },
  "OrderAmount": 15,
  "OrderId": 225,
  "OrderAmountData": "12.00",
  "ProductData": {
    "ProductId": 1,
    "ProductDescription": "Test1",
    "Amount": 0,
    "Quantity": 0
  },
  "NextStepFlowData": {
    "RedirectLabel": "Test12",
    "Text": "Submit"
  },
  "TransactionType": "Charge",
  "CustomerData": {
    "CustomerId": 1,
    "FirstName": "test",
    "LastName": "m",
    "MobileNo": "33333333333",
    "email": "praveen@gmail.com",
    "EmailReceipt": false,
    "BillingAddress": "Telangana",
    "BillingCity": "test",
    "BillingState": "TS",
    "BillingCountry": "IN",
    "BillingZipCode": "TEST",
    "ShippingFirstName": "",
    "ShippingLastName": "",
    "ShippingAddress": "",
    "ShippingCity": "",
    "ShippingState": "",
    "ShippingCountry": "",
    "ShippingZipCode": "",
    "ShippingMobileNo": ""
  },
  "UserDefinedData": {
    "UserDefined1": "",
    "UserDefined2": "",
    "UserDefined3": "",
    "UserDefined4": "",
    "UserDefined5": "",
    "UserDefined6": "",
    "UserDefined7": "",
    "UserDefined8": "",
    "UserDefined9": "",
    "UserDefined10": "",
    "UserDefined11": "",
    "UserDefined12": "",
    "UserDefined13": "",
    "UserDefined14": "",
    "UserDefined15": "",
    "UserDefined16": "",
    "UserDefined17": "",
    "UserDefined18": "",
    "UserDefined19": "",
    "UserDefined20": ""
  },
  "RequestDateTime": "",
  "RedirectUrl": "https://payg.in"
}`;

const init = {
  method: 'POST',
  headers,
  body
};

fetch('https://uatapi.payg.in/payment/api/order/create', init)
.then((response) => {
  return response.json(); // or .text() or .blob() ...
})
.then((text) => {
  // text is the response body
})
.catch((e) => {
  // error in e.message
});
```
```http
{
  "MerchantKeyId": 292,
  "AuthenticationKey": "12959e563133424a9576e541c2670a83",
  "AuthenticationToken": "ca66b41b8e4f4187819d559a591ccfb7",
  "UniqueRequestId": "AA10030",
  "TransactionDate": {
    "PaymentType": "ALL"
  },
  "OrderAmount": 15,
  "OrderId": 225,
  "OrderAmountData": "12.00",
  "ProductData": {
    "ProductId": 1,
    "ProductDescription": "Test1",
    "Amount": 0,
    "Quantity": 0
  },
  "NextStepFlowData": {
    "RedirectLabel": "Test12",
    "Text": "Submit"
  },
  "TransactionType": "Charge",
  "CustomerData": {
    "CustomerId": 1,
    "FirstName": "test",
    "LastName": "m",
    "MobileNo": "33333333333",
    "email": "praveen@gmail.com",
    "EmailReceipt": false,
    "BillingAddress": "Telangana",
    "BillingCity": "test",
    "BillingState": "TS",
    "BillingCountry": "IN",
    "BillingZipCode": "TEST",
    "ShippingFirstName": "",
    "ShippingLastName": "",
    "ShippingAddress": "",
    "ShippingCity": "",
    "ShippingState": "",
    "ShippingCountry": "",
    "ShippingZipCode": "",
    "ShippingMobileNo": ""
  },
  "UserDefinedData": {
    "UserDefined1": "",
    "UserDefined2": "",
    "UserDefined3": "",
    "UserDefined4": "",
    "UserDefined5": "",
    "UserDefined6": "",
    "UserDefined7": "",
    "UserDefined8": "",
    "UserDefined9": "",
    "UserDefined10": "",
    "UserDefined11": "",
    "UserDefined12": "",
    "UserDefined13": "",
    "UserDefined14": "",
    "UserDefined15": "",
    "UserDefined16": "",
    "UserDefined17": "",
    "UserDefined18": "",
    "UserDefined19": "",
    "UserDefined20": ""
  },
  "RequestDateTime": "",
  "RedirectUrl": "https://payg.in"
}
```

```java
StringBuilder sb = new StringBuilder();
sb.append("{\n");
sb.append("  \"MerchantKeyId\": 292,\n");
sb.append("  \"AuthenticationKey\": \"12959e563133424a9576e541c2670a83\",\n");
sb.append("  \"AuthenticationToken\": \"ca66b41b8e4f4187819d559a591ccfb7\",\n");
sb.append("  \"UniqueRequestId\": \"AA10030\",\n");
sb.append("  \"TransactionDate\": {\n");
sb.append("    \"PaymentType\": \"ALL\"\n");
sb.append("  },\n");
sb.append("  \"OrderAmount\": 15,\n");
sb.append("  \"OrderId\": 225,\n");
sb.append("  \"OrderAmountData\": \"12.00\",\n");
sb.append("  \"ProductData\": {\n");
sb.append("    \"ProductId\": 1,\n");
sb.append("    \"ProductDescription\": \"Test1\",\n");
sb.append("    \"Amount\": 0,\n");
sb.append("    \"Quantity\": 0\n");
sb.append("  },\n");
sb.append("  \"NextStepFlowData\": {\n");
sb.append("    \"RedirectLabel\": \"Test12\",\n");
sb.append("    \"Text\": \"Submit\"\n");
sb.append("  },\n");
sb.append("  \"TransactionType\": \"Charge\",\n");
sb.append("  \"CustomerData\": {\n");
sb.append("    \"CustomerId\": 1,\n");
sb.append("    \"FirstName\": \"test\",\n");
sb.append("    \"LastName\": \"m\",\n");
sb.append("    \"MobileNo\": \"33333333333\",\n");
sb.append("    \"email\": \"praveen@gmail.com\",\n");
sb.append("    \"EmailReceipt\": false,\n");
sb.append("    \"BillingAddress\": \"Telangana\",\n");
sb.append("    \"BillingCity\": \"test\",\n");
sb.append("    \"BillingState\": \"TS\",\n");
sb.append("    \"BillingCountry\": \"IN\",\n");
sb.append("    \"BillingZipCode\": \"TEST\",\n");
sb.append("    \"ShippingFirstName\": \"\",\n");
sb.append("    \"ShippingLastName\": \"\",\n");
sb.append("    \"ShippingAddress\": \"\",\n");
sb.append("    \"ShippingCity\": \"\",\n");
sb.append("    \"ShippingState\": \"\",\n");
sb.append("    \"ShippingCountry\": \"\",\n");
sb.append("    \"ShippingZipCode\": \"\",\n");
sb.append("    \"ShippingMobileNo\": \"\"\n");
sb.append("  },\n");
sb.append("  \"UserDefinedData\": {\n");
sb.append("    \"UserDefined1\": \"\",\n");
sb.append("    \"UserDefined2\": \"\",\n");
sb.append("    \"UserDefined3\": \"\",\n");
sb.append("    \"UserDefined4\": \"\",\n");
sb.append("    \"UserDefined5\": \"\",\n");
sb.append("    \"UserDefined6\": \"\",\n");
sb.append("    \"UserDefined7\": \"\",\n");
sb.append("    \"UserDefined8\": \"\",\n");
sb.append("    \"UserDefined9\": \"\",\n");
sb.append("    \"UserDefined10\": \"\",\n");
sb.append("    \"UserDefined11\": \"\",\n");
sb.append("    \"UserDefined12\": \"\",\n");
sb.append("    \"UserDefined13\": \"\",\n");
sb.append("    \"UserDefined14\": \"\",\n");
sb.append("    \"UserDefined15\": \"\",\n");
sb.append("    \"UserDefined16\": \"\",\n");
sb.append("    \"UserDefined17\": \"\",\n");
sb.append("    \"UserDefined18\": \"\",\n");
sb.append("    \"UserDefined19\": \"\",\n");
sb.append("    \"UserDefined20\": \"\"\n");
sb.append("  },\n");
sb.append("  \"RequestDateTime\": \"\",\n");
sb.append("  \"RedirectUrl\": \"https://payg.in\"\n");
sb.append("}");
String body = sb.toString();

HttpEntity<String> requestEntity = new HttpEntity<String>(body, headers);
ResponseEntity<String> responseEntity = rest.exchange("https://uatapi.payg.in/payment/api/order/create", HttpMethod.POST, requestEntity, String.class);
HttpStatus httpStatus = responseEntity.getStatusCode();
int status = httpStatus.value();
String response = responseEntity.getBody();
System.out.println("Response status: " + status);
System.out.println(response);
```
## Possible Response

200

Status Success

400

Bad input parameter. Error message should indicate which one and why.

401

The client passed in the invalid Auth token. Client should refresh the token and then try again.

403

Merchant doesn’t exist. * Merchant not registered. * Application try to access to properties not belong to an App. * Application try to trash/purge root node. * Application try to update contentProperties. * Operation is blocked (for third-party apps). * Merchant account over quota.

404

Resource not found.

405

The resource doesn't support the specified HTTP verb.

409

Conflict

411

The Content-Length header was not specified.

412

Precondition failed.

429

Too many request for rate limiting.

500

Servers are not working as expected. The request is probably valid but needs to be requested again later.

503

Service Unavailable.

> Type 

> any

> RESPONSE BODY

>200


```python
{
  "OrderKeyId": "200915M292UAA10030",
  "MerchantKeyId": 292,
  "UniqueRequestId": "AA10030",
  "OrderType": "PAYMENT",
  "OrderAmount": 15,
  "OrderId": "225",
  "OrderStatus": null,
  "OrderPaymentStatus": 0,
  "OrderPaymentStatusText": null,
  "PaymentStatus": 0,
  "PaymentTransactionId": null,
  "PaymentResponseCode": 0,
  "PaymentApprovalCode": null,
  "PaymentResponseText": null,
  "PaymentMethod": null,
  "PaymentAccount": null,
  "OrderNotes": null,
  "PaymentDateTime": null,
  "UpdatedDateTime": null,
  "PaymentProcessUrl": "https://uat.payg.in/payment/payment?orderid=200915M292UAA10030",
  "OrderPaymentCustomerData": {
    "FirstName": "test",
    "LastName": null,
    "Address": null,
    "City": null,
    "State": null,
    "ZipCode": null,
    "Country": null,
    "MobileNo": "33333333333",
    "Email": "praveen@gmail.com",
    "UserId": null,
    "IpAddress": null
  },
  "UpiLink": "&sign=",
  "CustomerData": {
    "CustomerId": "1",
    "CustomerNotes": null,
    "FirstName": "test",
    "LastName": "m",
    "MobileNo": "33333333333",
    "Email": "praveen@gmail.com",
    "EmailReceipt": false,
    "BillingAddress": "Telangana",
    "BillingCity": "test",
    "BillingState": "TS",
    "BillingCountry": "IN",
    "BillingZipCode": "TEST",
    "ShippingFirstName": "",
    "ShippingLastName": "",
    "ShippingAddress": "",
    "ShippingCity": "",
    "ShippingState": "",
    "ShippingCountry": "",
    "ShippingZipCode": "",
    "ShippingMobileNo": ""
  }
}
```

```shell
{
  "OrderKeyId": "200915M292UAA10030",
  "MerchantKeyId": 292,
  "UniqueRequestId": "AA10030",
  "OrderType": "PAYMENT",
  "OrderAmount": 15,
  "OrderId": "225",
  "OrderStatus": null,
  "OrderPaymentStatus": 0,
  "OrderPaymentStatusText": null,
  "PaymentStatus": 0,
  "PaymentTransactionId": null,
  "PaymentResponseCode": 0,
  "PaymentApprovalCode": null,
  "PaymentResponseText": null,
  "PaymentMethod": null,
  "PaymentAccount": null,
  "OrderNotes": null,
  "PaymentDateTime": null,
  "UpdatedDateTime": null,
  "PaymentProcessUrl": "https://uat.payg.in/payment/payment?orderid=200915M292UAA10030",
  "OrderPaymentCustomerData": {
    "FirstName": "test",
    "LastName": null,
    "Address": null,
    "City": null,
    "State": null,
    "ZipCode": null,
    "Country": null,
    "MobileNo": "33333333333",
    "Email": "praveen@gmail.com",
    "UserId": null,
    "IpAddress": null
  },
  "UpiLink": "&sign=",
  "CustomerData": {
    "CustomerId": "1",
    "CustomerNotes": null,
    "FirstName": "test",
    "LastName": "m",
    "MobileNo": "33333333333",
    "Email": "praveen@gmail.com",
    "EmailReceipt": false,
    "BillingAddress": "Telangana",
    "BillingCity": "test",
    "BillingState": "TS",
    "BillingCountry": "IN",
    "BillingZipCode": "TEST",
    "ShippingFirstName": "",
    "ShippingLastName": "",
    "ShippingAddress": "",
    "ShippingCity": "",
    "ShippingState": "",
    "ShippingCountry": "",
    "ShippingZipCode": "",
    "ShippingMobileNo": ""
  }
}
```

```javascript
{
  "OrderKeyId": "200915M292UAA10030",
  "MerchantKeyId": 292,
  "UniqueRequestId": "AA10030",
  "OrderType": "PAYMENT",
  "OrderAmount": 15,
  "OrderId": "225",
  "OrderStatus": null,
  "OrderPaymentStatus": 0,
  "OrderPaymentStatusText": null,
  "PaymentStatus": 0,
  "PaymentTransactionId": null,
  "PaymentResponseCode": 0,
  "PaymentApprovalCode": null,
  "PaymentResponseText": null,
  "PaymentMethod": null,
  "PaymentAccount": null,
  "OrderNotes": null,
  "PaymentDateTime": null,
  "UpdatedDateTime": null,
  "PaymentProcessUrl": "https://uat.payg.in/payment/payment?orderid=200915M292UAA10030",
  "OrderPaymentCustomerData": {
    "FirstName": "test",
    "LastName": null,
    "Address": null,
    "City": null,
    "State": null,
    "ZipCode": null,
    "Country": null,
    "MobileNo": "33333333333",
    "Email": "praveen@gmail.com",
    "UserId": null,
    "IpAddress": null
  },
  "UpiLink": "&sign=",
  "CustomerData": {
    "CustomerId": "1",
    "CustomerNotes": null,
    "FirstName": "test",
    "LastName": "m",
    "MobileNo": "33333333333",
    "Email": "praveen@gmail.com",
    "EmailReceipt": false,
    "BillingAddress": "Telangana",
    "BillingCity": "test",
    "BillingState": "TS",
    "BillingCountry": "IN",
    "BillingZipCode": "TEST",
    "ShippingFirstName": "",
    "ShippingLastName": "",
    "ShippingAddress": "",
    "ShippingCity": "",
    "ShippingState": "",
    "ShippingCountry": "",
    "ShippingZipCode": "",
    "ShippingMobileNo": ""
  }
}
```
```http

{
  "OrderKeyId": "200915M292UAA10030",
  "MerchantKeyId": 292,
  "UniqueRequestId": "AA10030",
  "OrderType": "PAYMENT",
  "OrderAmount": 15,
  "OrderId": "225",
  "OrderStatus": null,
  "OrderPaymentStatus": 0,
  "OrderPaymentStatusText": null,
  "PaymentStatus": 0,
  "PaymentTransactionId": null,
  "PaymentResponseCode": 0,
  "PaymentApprovalCode": null,
  "PaymentResponseText": null,
  "PaymentMethod": null,
  "PaymentAccount": null,
  "OrderNotes": null,
  "PaymentDateTime": null,
  "UpdatedDateTime": null,
  "PaymentProcessUrl": "https://uat.payg.in/payment/payment?orderid=200915M292UAA10030",
  "OrderPaymentCustomerData": {
    "FirstName": "test",
    "LastName": null,
    "Address": null,
    "City": null,
    "State": null,
    "ZipCode": null,
    "Country": null,
    "MobileNo": "33333333333",
    "Email": "praveen@gmail.com",
    "UserId": null,
    "IpAddress": null
  },
  "UpiLink": "&sign=",
  "CustomerData": {
    "CustomerId": "1",
    "CustomerNotes": null,
    "FirstName": "test",
    "LastName": "m",
    "MobileNo": "33333333333",
    "Email": "praveen@gmail.com",
    "EmailReceipt": false,
    "BillingAddress": "Telangana",
    "BillingCity": "test",
    "BillingState": "TS",
    "BillingCountry": "IN",
    "BillingZipCode": "TEST",
    "ShippingFirstName": "",
    "ShippingLastName": "",
    "ShippingAddress": "",
    "ShippingCity": "",
    "ShippingState": "",
    "ShippingCountry": "",
    "ShippingZipCode": "",
    "ShippingMobileNo": ""
  }
}

```
```java
{
  "OrderKeyId": "200915M292UAA10030",
  "MerchantKeyId": 292,
  "UniqueRequestId": "AA10030",
  "OrderType": "PAYMENT",
  "OrderAmount": 15,
  "OrderId": "225",
  "OrderStatus": null,
  "OrderPaymentStatus": 0,
  "OrderPaymentStatusText": null,
  "PaymentStatus": 0,
  "PaymentTransactionId": null,
  "PaymentResponseCode": 0,
  "PaymentApprovalCode": null,
  "PaymentResponseText": null,
  "PaymentMethod": null,
  "PaymentAccount": null,
  "OrderNotes": null,
  "PaymentDateTime": null,
  "UpdatedDateTime": null,
  "PaymentProcessUrl": "https://uat.payg.in/payment/payment?orderid=200915M292UAA10030",
  "OrderPaymentCustomerData": {
    "FirstName": "test",
    "LastName": null,
    "Address": null,
    "City": null,
    "State": null,
    "ZipCode": null,
    "Country": null,
    "MobileNo": "33333333333",
    "Email": "praveen@gmail.com",
    "UserId": null,
    "IpAddress": null
  },
  "UpiLink": "&sign=",
  "CustomerData": {
    "CustomerId": "1",
    "CustomerNotes": null,
    "FirstName": "test",
    "LastName": "m",
    "MobileNo": "33333333333",
    "Email": "praveen@gmail.com",
    "EmailReceipt": false,
    "BillingAddress": "Telangana",
    "BillingCity": "test",
    "BillingState": "TS",
    "BillingCountry": "IN",
    "BillingZipCode": "TEST",
    "ShippingFirstName": "",
    "ShippingLastName": "",
    "ShippingAddress": "",
    "ShippingCity": "",
    "ShippingState": "",
    "ShippingCountry": "",
    "ShippingZipCode": "",
    "ShippingMobileNo": ""
  }
}
```

> Type:

> any
