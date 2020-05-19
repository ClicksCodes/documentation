# Creating an account

{% api-method method="post" host="https://api.clicksminuteper.net/connectmypairs" path="/users/" %}
{% api-method-summary %}
Create Account
{% endapi-method-summary %}
{% api-method-description %}
This endpoint allows you to create a new user account.
{% endapi-method-description %}
{% api-method-spec %}
{% api-method-request %}
{% api-method-headers %}
{% api-method-parameter name="Username" type="string" required=true %}
The username of the account being created.
{% endapi-method-parameter %}
{% api-method-parameter name="Privacy" type="integer" %}
The default privacy setting of the user creating the account. `0`, public, is default, `1` is unlisted, `2` is private.
{% endapi-method-parameter %}
{% endapi-method-headers %}
{% endapi-method-request %}
{% api-method-response %}
{% api-method-response-example httpCode=201 %}
{% api-method-response-example-description %}
User account was successfully created.
{% endapi-method-response-example-description %}
```
{    
  "code": "success",
  "description": "User account was successfully created."
  "name": "Username",
  "privacy": 0
}
```
{% endapi-method-response-example %}
{% api-method-response-example httpCode=400 %}
{% api-method-response-example-description %}
Syntax was not valid
{% endapi-method-response-example-description %}
```
{    
  "code": "invalid_privacy" or "invalid_username",
  "description": "Privacy was an invalid integer."
}
```
{% endapi-method-response-example %}
{% api-method-response-example httpCode=409 %}
{% api-method-response-example-description %}
Name already in use.
{% endapi-method-response-example-description %}
```
{    
  "name": "Username",
  "code": "409"
}
```
{% endapi-method-response-example %}
{% endapi-method-response %}
{% endapi-method-spec %}
{% endapi-method %}

{% hint style="danger" %}
 Descriptions may not be exactly as listed here. Please use the code instead.
{% endhint %}
