# Creating a pack

{% api-method method="post" host="https://api.clicksminuteper.net/connectmypairs" path="/packs/" %}
{% api-method-summary %}
Create Pack
{% endapi-method-summary %}
{% api-method-description %}
This endpoint allows you to create a new pack.
{% endapi-method-description %}
{% api-method-spec %}
{% api-method-request %}
{% api-method-headers %}
{% api-method-parameter name="Authentication" type="string" required=true %}
Authentication of the user creating the pack.
{% endapi-method-parameter %}
{% api-method-parameter name="Name" type="string" %}
The name of the pack. Randomised if a name is not provided.
{% endapi-method-parameter %}
{% api-method-parameter name="Privacy" type="integer" %}
Who can view and use the pack. Default is public, `0`. `1` means people in a server you are in, and `2` means only you can.
{% endapi-method-parameter %}
{% api-method-parameter name="Questions" type="string" %}
The set of questions that will be used.
{% endapi-method-parameter %}
{% api-method-parameter name="Answers" type="string" %}
The set of answers that will be used.
{% endapi-method-parameter %}
{% endapi-method-headers %}
{% endapi-method-request %}
{% api-method-response %}
{% api-method-response-example httpCode=201 %}
{% api-method-response-example-description %}
The deck was created successfully.
{% endapi-method-response-example-description %}
```
{    
  "code": "success",
  "description": "Deck was successfully created."
  "name": "name",
  "privacy": 0
}
```
{% endapi-method-response-example %}
{% api-method-response-example httpCode=400 %}
{% api-method-response-example-description %}
Syntax was not valid.
{% endapi-method-response-example-description %}
```
{    
  "name": "name"
  "code": "invalid_syntax",
  "description": "The syntax provided was invalid."
}
```
{% endapi-method-response-example %}
{% api-method-response-example httpCode=401 %}
{% api-method-response-example-description %}
Authorization failed.
{% endapi-method-response-example-description %}
```
{    
  "name": "name",
  "code": "authorization_failed",
  "description": "The information provided to authorize was incorrect."
}
```
{% endapi-method-response-example %}
{% api-method-response-example httpCode=409 %}
{% api-method-response-example-description %}
Pack name already in use.
{% endapi-method-response-example-description %}
```
{    
  "name": "name",
  "code": "name_in_use",
  "description": "The pack name provided is already in use."
}
```
{% endapi-method-response-example %}
{% endapi-method-response %}
{% endapi-method-spec %}
{% endapi-method %}

{% hint style="info" %}
 The questions and asnwers parameter can be left empty, creating a pack with no cards. This can be useful for reserving a deck name.
{% endhint %}

{% hint style="danger" %}
 Descriptions may not be exactly as listed here. Please use the code instead.
{% endhint %}
