---
group: rest
title: Generate the admin token
functional_areas:
  - Integration
  - Orders
---


Most REST calls to Magento require an {% glossarytooltip 34ecb0ab-b8a3-42d9-a728-0b893e8c0417 %}authorization{% endglossarytooltip %} token. The token allows Magento to verify that the caller is authorized to access a system resource. To get a token, you must specify the user's username and password in the payload.

By default, an admin token is valid for 4 hours. To change this value, log in to Admin and go to **Configuration** > **Services** > **OAuth** > **Access Token Expiration**.

See [Token-based authentication]({{ page.baseurl }}/get-started/authentication/gs-authentication-token.html) for more information about authorization tokens.

**Endpoint**

`POST http://<host>/rest/default/V1/integration/admin/token`

**Headers**

`Content-Type` `application/json`

**Payload**

``` json
{
"username": "admin",
"password": "123123q"
}
```

**Response**

Magento generates the admin's access token

`5r8cvmpr11j6gmau8990rcj2qk7unh8i`

This token must be specified in the authorization header of every call that requires {% glossarytooltip 29ddb393-ca22-4df9-a8d4-0024d75739b1 %}admin{% endglossarytooltip %} permissions.

### Verify this step {#verify-step}

There are no additional verification steps. Tokens are not displayed in Admin.
