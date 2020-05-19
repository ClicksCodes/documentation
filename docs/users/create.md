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
The username of the user creating the account.
{% endapi-method-parameter %}
{% api-method-parameter name="Privacy" type="string" %}
The default privacy setting of the user creating the account. Public by default.
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
  "name": "Username",    
  "privacy": "Privacy setting"
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
  "privacy": "Privacy setting",
  "code": "400"
  "description": "Privacy was invalid"
}
```
{% endapi-method-response-example %}
{% api-method-response-example httpCode=403 %}
{% api-method-response-example-description %}
You are not allowed to perform this action at this time.
{% endapi-method-response-example-description %}
```
{
  "description": "Your IP address was blocked.",
  "code": "403"
}
```
{% endapi-method-response-example %}
{% endapi-method-response %}
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
