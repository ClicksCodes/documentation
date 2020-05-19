# Creating an account

{% api-method method="post" host="https://api.clicksminuteper.net" path="/connectmypairs/users/" %}
{% api-method-summary %}
Create Account
{% endapi-method-summary %}
{% api-method-description %}
This endpoint allows you to create a new user account.
{% endapi-method-description %}
{% api-method-spec %}
{% api-method-request %}
{% api-method-headers %}
{% api-method-parameter name="Authentication" type="string" required=true %}
Authentication token of the user creating the account.
{% endapi-method-parameter %}
{% api-method-parameter name="Username" type="string" required=true %}
The username of the user creating the account.
{% endapi-method-parameter %}
{% api-method-parameter name="Privacy" type="string" %}
The default privacy setting of the user creating the account. Public by default.
{% endapi-method-parameter %}
{% endapi-method-headers %}
{% endapi-method-request %}
{% api-method-response %}
{% api-method-response-example httpCode=200 %}
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
{% endapi-method-response %}
{% endapi-method-spec %}
{% endapi-method %}
