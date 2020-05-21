# Get all packs by a user

{% api-method method="get" host="https://api.clicksminuteper.net" path="/users/:id/get" %}
{% api-method-summary %}

{% endapi-method-summary %}

{% api-method-description %}

{% endapi-method-description %}

{% api-method-spec %}
{% api-method-request %}
{% api-method-path-parameters %}
{% api-method-parameter name="User ID" type="string" required=true %}
The ID of the user.
{% endapi-method-parameter %}
{% endapi-method-path-parameters %}

{% api-method-headers %}
{% api-method-parameter name="Authentication" type="number" required=false %}
Authentication to get private packs.
{% endapi-method-parameter %}
{% endapi-method-headers %}
{% endapi-method-request %}

{% api-method-response %}
{% api-method-response-example httpCode=200 %}
{% api-method-response-example-description %}
Packs retrieved successfully.
{% endapi-method-response-example-description %}

```text
{    
  "code": "success",
  "packs": []
  "name": "Username",
  "privacy": 0
}
```
{% endapi-method-response-example %}

{% api-method-response-example httpCode=404 %}
{% api-method-response-example-description %}
Syntax was not valid
{% endapi-method-response-example-description %}

```text
{    
  "code": "invalid_id"
  "description": "ID given was not a valid user."
}
```
{% endapi-method-response-example %}
{% endapi-method-response %}
{% endapi-method-spec %}
{% endapi-method %}

