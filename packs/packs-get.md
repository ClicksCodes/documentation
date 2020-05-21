# Get a pack

{% api-method method="get" host="https://api.clicksminuteper.net/connectmypairs" path="/packs/" %}
{% api-method-summary %}
Create Pack
{% endapi-method-summary %}

{% api-method-description %}
This endpoint allows you to get all cards in a pack.
{% endapi-method-description %}

{% api-method-spec %}
{% api-method-request %}
{% api-method-headers %}
{% api-method-parameter name="Authentication" type="string" required=false %}
Authentication if you are getting a private pack.
{% endapi-method-parameter %}

{% api-method-parameter name="Name" type="string" required=true %}
The name of the pack.
{% endapi-method-parameter %}

{% endapi-method-headers %}
{% endapi-method-request %}

{% api-method-response %}
{% api-method-response-example httpCode=201 %}
{% api-method-response-example-description %}
The deck was created successfully.
{% endapi-method-response-example-description %}

```text
{    
  "code": "success",
  "questions": [],
  "answers": [],
  "name": "name",
  "creator": "name"
}
```
{% endapi-method-response-example %}

{% api-method-response-example httpCode=400 %}
{% api-method-response-example-description %}
Syntax was not valid.
{% endapi-method-response-example-description %}

```text
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

```text
{    
  "name": "name",
  "code": "authorization_failed",
  "description": "The information provided to authorize was incorrect."
}
```
{% endapi-method-response-example %}

{% api-method-response-example httpCode=404 %}
{% api-method-response-example-description %}
The pack could not be found.
{% endapi-method-response-example-description %}

```text
{    
  "name": "name",
  "code": "not_found",
  "description": "A pack by that name could not be found."
}
```
{% endapi-method-response-example %}
{% endapi-method-response %}
{% endapi-method-spec %}
{% endapi-method %}

{% hint style="danger" %}
Descriptions may not be exactly as listed here. Please use the code instead.
{% endhint %}

