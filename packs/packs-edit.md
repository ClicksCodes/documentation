# Editing a pack

{% api-method method="patch" host="https://api.clicksminuteper.net/connectmypairs" path="/packs/" %}
{% api-method-summary %}
Edit Pack
{% endapi-method-summary %}
{% api-method-description %}
This endpoint allows you to edit a current packs.
{% endapi-method-description %}
{% api-method-spec %}
{% api-method-request %}
{% api-method-headers %}
{% api-method-parameter name="Authentication" type="string" required=true %}
Authentication of the user editing the pack.
{% endapi-method-parameter %}
{% api-method-parameter name="Name" type="string" required=true %}
The name of the pack.
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
  "description": "Deck was successfully edited."
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
Forbidden
{% endapi-method-response-example-description %}
```
{    
  "name": "name",
  "code": "forbidden",
  "description": "You do not have permission to edit this deck."
}
```
{% endapi-method-response-example %}
{% endapi-method-response %}
{% endapi-method-spec %}
{% api-method-body-parameters %}
{% api-method-parameter name="Privacy" type="integer" required=false %}
The privacy integer of the pack.
{% endapi-method-parameter %}
{% api-method-parameter name="Name" type="string" required=false %}
The name of the pack.
{% endapi-method-parameter %}
{% api-method-parameter name="Description" type="string" required=false %}
The description of the pack.
{% endapi-method-parameter %}
{% api-method-parameter name="Questions" type="string" required=false %}
The question cards in the pack.
{% endapi-method-parameter %}
{% api-method-parameter name="Answers" type="string" required=false %}
The answer cards in the pack.
{% endapi-method-parameter %}
{% endapi-method-body-parameters %}
{% endapi-method %}

{% hint style="danger" %}
 Descriptions may not be exactly as listed here. Please use the code instead.
{% endhint %}
