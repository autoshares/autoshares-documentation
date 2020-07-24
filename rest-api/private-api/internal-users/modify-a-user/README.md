---
description: Modify an existing user in ETNA Trader
---

# Modify a User

### Overview

This PUT endpoint enables you to modify an existing user in ETNA Trader. Updated information about the user is provided in the request body in the JSON format. 

{% hint style="warning" %}
In order to modify an existing user, you must use an [authorization token](../../authentication/) of an administrator. Using authorization tokens of regular users will lead to the 401 status code.
{% endhint %}

There are six required parameters that must be provided in the request:

1. **Et-App-Key** \(header\). This is the unique key of your app that identifies your app when communicating with our service. It can be found it in the **BO Companies** widget. When editing the company's settings, navigate to the **WebApi** tab and look for the required key \(it could be a key for the web terminal, the mobile app, or a custom key\).
2. **Authorization** \(header\). This is the authorization token from the very first [token request](../../authentication/).
3. **API version** \(path\). Unless necessary, leave it at "1.0".
4. **userId** \(path\). This is the internal identifier of the modified user. 
5. **sendInvitationEmail** \(query\). This is a boolean parameter that indicates if the modified  user should receive an invitation email after their information is updated.
6. **user** \(body\). This a JSON file that contains information about the modified user.

Here's the final template for this API request:

```text
PUT apiURL/v1.0/users/{userID}
```

#### Request Body Sample

The body of the request represents a JSON file with mandatory parameters required for user modification.

```javascript
{
  "FirstName": "string", //required
  "Middle": "string", 
  "LastName": "string", //required
  "EmailAddress": "new@email.com", //required
  "Login": "string", //required
  "Salutation": "NoSalutation", 
  "Suffix": "NoSuffix",
  "Enabled": true, 
  "TimeZoneInfoId": "string", 
  "ExpirationDate": "2019-03-10T14:11:54.494Z",
  "PhoneNumber": "string",
  "EntitlementsPhoneNumber": "string"
}
```

where:

| Parameter | Description |
| :--- | :--- |
| FirstName | This is the first name of the user in ETNA Trader. |
| Middle | This is the middle name of the user in ETNA Trader. |
| LastName | This is the last name of the user in ETNA Trader. |
| EmailAddress | This is the email address of the modified user. |
| Login | This is the user's login. |
| Salutation | This is a special salutation used to address this user in emails. |
| Suffix | This is the suffix used when addressing the user \(Jr, Sr, I, II, III, etc.\). |
| Enabled | This field indicates if the user is active and can make trades in ETNA Trader. |
| TimeZoneInfoId | This field indicates the time zone in which the user lives. |
| ExpirationDate | This is the date on which the user's account will be disabled. |
| PhoneNumber / EntitlementsPhoneNumber | This the user's phone number. |

### Response

In response to this API request, you'll receive a JSON file that contains information you specified in the request body along with the modified user's internal identifier in ETNA Trader:

```javascript
{
  "Id": 7473,
  "FirstName": "string",
  "Middle": "s",
  "LastName": "string",
  "EmailAddress": "new@email.com",
  "Login": "string",
  "Salutation": "NoSalutation",
  "Suffix": "NoSuffix",
  "AddedDate": "2019-03-06T15:12:43.2333427Z",
  "Enabled": true,
  "Deleted": false,
  "TimeZoneInfoId": "string",
  "ExpirationDate": "2019-03-10T14:11:54.494Z",
  "PhoneNumber": "string",
  "EntitlementsPhoneNumber": "string"
}
```

### Common Mistakes

Here are some of the common mistakes that developers make when attempting to modify an existing user.

#### Requesting as a Non-Administrator

One of the most common mistakes that developers make when making this API request is to use the authorization token of a non-administrator. It's critical to understand that in order to be eligible for modifying users, the requester must be an administrator. Otherwise you'll receive the 401 status code with the following message:

```javascript
{
    "Message": "Authorization has been denied for this request."
}
```

So be sure to use the authorization token generated with an administrator's credentials.

#### Failing to Specify the Et-App-Key Parameter

If you specify the wrong Et-App-Key parameter or fail to include it in the header altogether, you'll get the following error:

```javascript
{
    "error": "Application key is not defined or does not exist"
}
```

#### Failing to Provide All Required Parameters

Another common mistake when making this API request is failing to provide all required parameters in the request's body. In the request body sample above we have highlighted all required parameters for this request, so ensure that you provide all of them; otherwise you'll receive the 500 status code and the following error message:

```javascript
{
  "message": "An error occurred while processing your request",
  "error": "Unexpected server error"
}
```

