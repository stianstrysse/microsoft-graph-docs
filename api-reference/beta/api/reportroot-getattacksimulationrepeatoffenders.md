---
title: "reportRoot: getAttackSimulationRepeatOffenders"
description: "List repeat offender users of a tenant in attack simulation and training campaigns."
author: "Gopal-MSFT"
ms.localizationpriority: medium
ms.prod: "reports"
doc_type: apiPageType
---

# reportRoot: getAttackSimulationRepeatOffenders
Namespace: microsoft.graph

[!INCLUDE [beta-disclaimer](../../includes/beta-disclaimer.md)]

List the users of a tenant who have yielded to attacks more than once in attack simulation and training campaigns.

This function supports `@odata.nextLink` for pagination.

## Permissions
One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).

| Permission type                        | Permissions (from least to most privileged) |
|:---------------------------------------|:--------------------------------------------|
| Delegated (work or school account)     | Reports.Read.All                            |
| Delegated (personal Microsoft account) | Not supported.                              |
| Application                            | Reports.Read.All                            |

## HTTP request

<!-- {
  "blockType": "ignored"
}
-->
``` http
GET /reports/getAttackSimulationRepeatOffenders
```

## Request headers
|Name|Description|
|:---|:---|
|Authorization|Bearer {token}. Required.|

## Request body
Do not supply a request body for this method.

## Response

If successful, this function returns a `200 OK` response code and a [attackSimulationRepeatOffender](../resources/attacksimulationrepeatoffender.md) collection in the response body.

## Examples

### Request

# [HTTP](#tab/http)
<!-- {
  "blockType": "request",
  "name": "reportroot_getattacksimulationrepeatoffenders"
}
-->
``` http
GET https://graph.microsoft.com/beta/reports/getAttackSimulationRepeatOffenders
```
# [C#](#tab/csharp)
[!INCLUDE [sample-code](../includes/snippets/csharp/reportroot-getattacksimulationrepeatoffenders-csharp-snippets.md)]
[!INCLUDE [sdk-documentation](../includes/snippets/snippets-sdk-documentation-link.md)]

# [JavaScript](#tab/javascript)
[!INCLUDE [sample-code](../includes/snippets/javascript/reportroot-getattacksimulationrepeatoffenders-javascript-snippets.md)]
[!INCLUDE [sdk-documentation](../includes/snippets/snippets-sdk-documentation-link.md)]

# [Objective-C](#tab/objc)
[!INCLUDE [sample-code](../includes/snippets/objc/reportroot-getattacksimulationrepeatoffenders-objc-snippets.md)]
[!INCLUDE [sdk-documentation](../includes/snippets/snippets-sdk-documentation-link.md)]

# [Java](#tab/java)
[!INCLUDE [sample-code](../includes/snippets/java/reportroot-getattacksimulationrepeatoffenders-java-snippets.md)]
[!INCLUDE [sdk-documentation](../includes/snippets/snippets-sdk-documentation-link.md)]

---



### Response
>**Note:** The response object shown here might be shortened for readability.
<!-- {
  "blockType": "response",
  "truncated": true,
  "@odata.type": "Collection(microsoft.graph.attackSimulationRepeatOffender)"
}
-->
``` http
HTTP/1.1 200 OK
Content-Type: application/json

{
  "value": [
    {
      "repeatOffenceCount": 1,
      "attackSimulationUser": {
        "userId": "99af58b9-ef1a-412b-a581-cb42fe8c8e21",
        "displayName": "Sample User",
        "email": "sampleuser@contoso.com"
      }
    }
  ]
}
```

