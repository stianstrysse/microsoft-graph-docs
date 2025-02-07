---
title: "group: renew"
description: "Renews a group's expiration. When a group is renewed, the group expiration is extended by the number of days defined in the policy."
ms.localizationpriority: medium
author: "Jordanndahl"
ms.prod: "groups"
doc_type: apiPageType
---

# group: renew

Namespace: microsoft.graph

[!INCLUDE [beta-disclaimer](../../includes/beta-disclaimer.md)]

Renews a group's expiration. When a group is renewed, the group expiration is extended by the number of days defined in the policy.

## Permissions

One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).
 

|Permission type      | Permissions (from least to most privileged)              |
|:--------------------|:---------------------------------------------------------|
|Delegated (work or school account) | Group.ReadWrite.All or Directory.ReadWrite.All    |
|Delegated (personal Microsoft account) | Not supported |
|Application | Group.ReadWrite.All or Directory.ReadWrite.All |

## HTTP request
<!-- { "blockType": "ignored" } -->
```http
POST /groups/{id}/renew
```

## Request headers
| Name       | Description|
|:---------------|:----------|
| Authorization  | Bearer {token}. Required. |


## Request body

Do not supply a request body for this method.

## Response

If successful, this method returns `204 No Content` response code. It does not return anything in the response body.

## Example

### Request


<!-- {
  "blockType": "request",
  "name": "group_renew"
}-->
```http
POST https://graph.microsoft.com/beta/groups/{id}/renew
```


### Response
<!-- {
  "blockType": "response"
} -->
```http
HTTP/1.1 204 No Content
```