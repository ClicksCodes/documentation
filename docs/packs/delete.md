# Deleting a pack

{% api-method method="delete" host="https://api.clicksminuteper.net/connectmypairs" path="/packs/" %}
{% api-method-summary %}
Delete pack
{% endapi-method-summary %}
{% api-method-description %}
This endpoint allows you to delete a pack.
{% endapi-method-description %}
{% api-method-spec %}
{% api-method-request %}
{% api-method-headers %}
{% api-method-parameter name="Authentication" type="string" required=true %}
Authentication of the user deleting the pack.
{% endapi-method-parameter %}
{% api-method-parameter name="Name" type="string" required=true %}
The name of the pack to delete.
{% endapi-method-parameter %}
{% api-method-parameter name="Confirmation" type="integer" required=true %}
Confirmation (`1`) to delete the pack. 
{% endapi-method-parameter %}
{% endapi-method-headers %}
{% endapi-method-request %}
{% api-method-response %}
{% api-method-response-example httpCode=200 %}
{% api-method-response-example-description %}
The deck was created successfully.
{% endapi-method-response-example-description %}
```
{    
  "code": "success",
  "description": "Deck was successfully deleted."
  "name": "name"
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
{% api-method-response-example httpCode=403 %}
{% api-method-response-example-description %}
You do not own this pack
{% endapi-method-response-example-description %}
```
{    
  "name": "name",
  "code": "forbidden",
  "description": "You do not have permission to delete this pack."
}
```
{% endapi-method-response-example %}
{% api-method-response-example httpCode=410 %}
{% api-method-response-example-description %}
Pack does not exist.
{% endapi-method-response-example-description %}
```
{    
  "name": "name",
  "code": "pack_not_found",
  "description": "The pack name provided could not be found."
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
