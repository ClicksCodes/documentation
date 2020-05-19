# Deleting an account

{% api-method method="delete" host="https://api.clicksminuteper.net/connectmypairs" path="/users/" %}
{% api-method-summary %}
Delete Account
{% endapi-method-summary %}

{% api-method-description %}
This endpoint allows you to delete a user account.
{% endapi-method-description %}

{% api-method-spec %}
{% api-method-request %}
{% api-method-headers %}
{% api-method-parameter name="Authentication" type="string" required=true %}
The authentication token of the users account to delete.
{% endapi-method-parameter %}

{% api-method-parameter name="Confirmation" type="integer" required=true %}
A `1` to confirm the deletion of the account.
{% endapi-method-parameter %}

{% endapi-method-headers %}

{% endapi-method-request %}

{% api-method-response %}
{% api-method-response-example httpCode=200 %}
{% api-method-response-example-description %}
User account was successfully deleted.
{% endapi-method-response-example-description %}

```
{    
  "name": "Username",
  "code": "Success"
}
```
{% endapi-method-response-example %}

{% api-method-response-example httpCode=400 %}
{% api-method-response-example-description %}
Syntax was not valid
{% endapi-method-response-example-description %}

```
{    
  "name": "Username",
  "code": "invalid_syntax"
  "description": "Invalid syntax was given."
}
```
{% endapi-method-response-example %}

{% api-method-response-example httpCode=401 %}
{% api-method-response-example-description %}
Unauthorised
{% endapi-method-response-example-description %}

```
{    
  "name": "Username",
  "code": "unauthorized",
  "description": "You did not provide the correct details to delete the account"
}
```
{% endapi-method-response-example %}

{% api-method-response-example httpCode=410 %}
{% api-method-response-example-description %}
Account does not exist
{% endapi-method-response-example-description %}

```
{    
  "name": "Username",
  "code": "no_account",
  "description": "The acocunt provided does not exist"
}
```
{% endapi-method-response-example %}
{% endapi-method-response %}
{% endapi-method-spec %}
{% endapi-method %}

{% hint style="danger" %}
 Descriptions may not be exactly as listed here. Please use the code instead.
{% endhint %}
