# Testing page

## Getting Super Powers

Becoming a super hero is a fairly straight forward process:

```
$ give me super-powers
```

{% hint style="info" %}
 Super-powers are granted randomly so please submit an issue if you're not happy with yours.
{% endhint %}

Once you're strong enough, save the world:

{% code title="hello.sh" %}
```bash
# Ain't no code for that yet, sorry
echo 'You got to trust me on this, I saved the world'
```
{% endcode %}

{% api-method method="get" host="https://example.com" path="/user/:id/packs" %}
{% api-method-summary %}
this
{% endapi-method-summary %}

{% api-method-description %}
Get all the packs for a user
{% endapi-method-description %}

{% api-method-spec %}
{% api-method-request %}
{% api-method-path-parameters %}
{% api-method-parameter name="id" type="string" required=false %}
Your randomly assigned user ID
{% endapi-method-parameter %}
{% endapi-method-path-parameters %}
{% endapi-method-request %}

{% api-method-response %}
{% api-method-response-example httpCode=200 %}
{% api-method-response-example-description %}

{% endapi-method-response-example-description %}

```

```
{% endapi-method-response-example %}
{% endapi-method-response %}
{% endapi-method-spec %}
{% endapi-method %}

{% tabs %}
{% tab title="First Tab" %}
tab
{% endtab %}

{% tab title="Second Tab" %}
another tab  
{% endtab %}
{% endtabs %}

{% hint style="warning" %}
info
{% endhint %}

{% hint style="danger" %}
warn
{% endhint %}

{% hint style="success" %}
success
{% endhint %}

| title 1 | title 2 |
| :--- | :--- |
| content 1 | content 2 |
| content 1 lower | content 2 lower |
|  |  |
| another thing |  |
|  |  |

> quote

```bash
code
block
```

$$
maths*equation=strange
$$

* bullet 
* point
* list

1. ordered
2. list

* [ ] task
* [ ] list
* [x] completed

![A happy birthday treat](../.gitbook/assets/bunting.png)

{% api-method method="delete" host="" path="" %}
{% api-method-summary %}

{% endapi-method-summary %}

{% api-method-description %}

{% endapi-method-description %}

{% api-method-spec %}
{% api-method-request %}
{% api-method-path-parameters %}
{% api-method-parameter name="" type="string" required=false %}

{% endapi-method-parameter %}
{% endapi-method-path-parameters %}
{% endapi-method-request %}

{% api-method-response %}
{% api-method-response-example httpCode=403 %}
{% api-method-response-example-description %}
You can never delete the all-seeing Minion
{% endapi-method-response-example-description %}

```
Minion cannot be deleted
```
{% endapi-method-response-example %}

{% api-method-response-example httpCode=405 %}
{% api-method-response-example-description %}
You are not allowed to delete the all-seeing Minion
{% endapi-method-response-example-description %}

```
Minion cannot be deleted
```
{% endapi-method-response-example %}

{% api-method-response-example httpCode=500 %}
{% api-method-response-example-description %}
Minion is too powerful for the server
{% endapi-method-response-example-description %}

```
Minion cannot be deleted
```
{% endapi-method-response-example %}
{% endapi-method-response %}
{% endapi-method-spec %}
{% endapi-method %}

