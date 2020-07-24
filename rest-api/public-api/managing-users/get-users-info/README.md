---
description: Get a user's information by their Autoshares Trader identifier
---

# Get User's Info

### Overview

This endpoint enables you to request a user's information by supplying their unique Autoshares Trader identifier in the header. In response, you'll receive a JSON file with the user's information.

There are four required parameters that must be provided in the request:

1. **Et-App-Key** \(header\). This is the unique key of your app that identifies your app when communicating with our service. Contact your administrator to get this key.
2. **Authorization** \(header\). This is the authorization token from the very first [token request](../../authentication/requesting-tokens/).
3. **Internal user ID** \(path\). This is the numeric ID of the user  whose information you'd like to receive. 
4. **API version** \(path\). Unless necessary, leave it at "1.0"

The user information request must be sent to the following URL:

```text
apiURL/v1.0/users/644(userID)/info
```

### Response

As a response, you'll receive a JSON file with the information about this user:

```javascript
{
    "UserId": 644, //this is the ID from the path
    "FirstName": "Robert",
    "MiddleName": "",
    "LastName": "Zakiev",
    "Login": "robert.zak",
    "Email": "someEmail@etnatrader.com",
    "AddedDate": "2019-01-14T12:27:37.6205663Z",
    "Salutation": "NoSalutation",
    "Suffix": "NoSuffix"
}
```

where:

| Parameter | Description |
| :--- | :--- |
| UserId | This is the internal ID of the user in Autoshares Trader. |
| FirstName | This is the first name of the user. |
| MiddleName | This is the middle name of the user. |
| LastName | This is the last name of the user. |
| Login | This is the user's login in Autoshares Trader. |
| Email | This is the email address of the user in Autoshares Trader. |
| AddedDate | This is the date on which this user account was added to Autoshares Trader. |
| Salutation | This is a special salutation used to address this user in emails. |
| Suffix | This is the suffix used when addressing the user \(Jr, Sr, I, II, III, etc.\) |

### Common Mistakes

Here are some of the common mistakes that developers make when requesting a user's information:

#### Failing to Specify the Et-App-Key Parameter

If you specify the wrong Et-App-Key parameter or fail to include it in the header altogether, you'll get the following error:

```javascript
{
    "error": "Application key is not defined or does not exist"
}
```

#### Specifying the Regular User ID Instead of the Internal One

Another common mistake when making this request is specifying the regular user ID instead of the internal Autoshares Trader ID. Doing so will result in the 400 status code and the following error message:

```javascript
{
    "Message": "The request is invalid."
}
```

