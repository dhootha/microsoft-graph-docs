---
title: "Update identitySecurityDefaultsEnforcementPolicy"
description: "Update the properties of an identitySecurityDefaultsEnforcementPolicy object."
localization_priority: Normal
author: "davidmu1"
ms.prod: "microsoft-identity-platform"
doc_type: apiPageType
---

# Update identitySecurityDefaultsEnforcementPolicy

Namespace: microsoft.graph

[!INCLUDE [beta-disclaimer](../../includes/beta-disclaimer.md)]

Update the properties of an [identitySecurityDefaultsEnforcementPolicy](../resources/identitysecuritydefaultsenforcementpolicy.md) object.

## Permissions

One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).

| Permission type                        | Permissions (from least to most privileged) |
|:---------------------------------------|:--------------------------------------------|
| Delegated (work or school account)     | Policy.Readwrite.ConditionalAccess |
| Delegated (personal Microsoft account) | Not supported. |
| Application                            | Policy.Readwrite.ConditionalAccess |

## HTTP request

<!-- { "blockType": "ignored" } -->

```http
PATCH /policies/identitySecurityDefaultsEnforcementPolicy
```

## Request headers

| Name       | Description|
|:-----------|:-----------|
| Authorization | Bearer {token}. Required. |
| Content-type | application/json. Required. |

## Request body

In the request body, supply the values for relevant fields that should be updated. Existing properties that are not included in the request body will maintain their previous values or be recalculated based on changes to other property values. For best performance, don't include existing values that haven't changed.

| Property     | Type        | Description |
|:-------------|:------------|:------------|
|isEnabled|Boolean|If set to true, Azure Active Directory security defaults is enabled for the tenant.|

## Response

If successful, this method returns a `204 No Content` response code. It does not return anything in the response body.

## Examples

### Request

The following is an example of the request.
<!-- {
  "blockType": "request",
  "name": "update_identitysecuritydefaultsenforcementpolicy"
}-->

```http
PATCH https://graph.microsoft.com/beta/policies/identitySecurityDefaultsEnforcementPolicy
Content-type: application/json

{
  "isEnabled": false
}
```

### Response

The following is an example of the response.

<!-- {
  "blockType": "response",
  "truncated": true,
  "@odata.type": "microsoft.graph.identitySecurityDefaultsEnforcementPolicy"
} -->

```http
HTTP/1.1 204 No Content
```

<!-- uuid: 16cd6b66-4b1a-43a1-adaf-3a886856ed98
2019-02-04 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "Update identitysecuritydefaultsenforcementpolicy",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->
