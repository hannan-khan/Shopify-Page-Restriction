# Shopify-Page-Restriction
collection page like wholesale restrict with pasword

add first copy the collection page from template file
then name this file for example collection.wholesale.liquid

then paste my code top of the code

{% unless customer %}
    {% if template contains 'customers' %}
        {% assign send_to_login = false %}
    {% else %}
        {% assign send_to_login = true %}
    {% endif %}
{% endunless %}

{% if send_to_login %}
<meta content="0; url=/account/login?checkout_url=https://truairbrushmakeup.myshopify.com/collections/wholesale-items" http-equiv="refresh" />
{% else %}

/* here goes your collection code */

at the end code add

{% endif %}

now all done
