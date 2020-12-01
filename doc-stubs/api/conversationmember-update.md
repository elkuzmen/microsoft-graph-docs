---
title: "Update conversationMember"
description: "Update the properties of a conversationMember object."
author: "**TODO: Provide Github Name. See [topic-level metadata reference](https://msgo.azurewebsites.net/add/document/guidelines/metadata.html#topic-level-metadata)**"
localization_priority: Normal
ms.prod: "**TODO: Add MS prod. See [topic-level metadata reference](https://msgo.azurewebsites.net/add/document/guidelines/metadata.html#topic-level-metadata)**"
doc_type: apiPageType
---

# Update conversationMember
Namespace: microsoft.graph

Update the properties of a [conversationMember](../resources/conversationmember.md) object.

## Permissions
One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).

|Permission type|Permissions (from most to least privileged)|
|:---|:---|
|Delegated (work or school account)|**TODO: Provide applicable permissions.**|
|Delegated (personal Microsoft account)|**TODO: Provide applicable permissions.**|
|Application|**TODO: Provide applicable permissions.**|

## HTTP request

<!-- {
  "blockType": "ignored"
}
-->
``` http
PATCH /chats/{chatsId}/members/{conversationMemberId}
PATCH /teams/{teamsId}/members/{conversationMemberId}
PATCH /teams/{teamsId}/channels/{channelId}/members/{conversationMemberId}
```

## Request headers
|Name|Description|
|:---|:---|
|Authorization|Bearer {token}. Required.|
|Content-Type|application/json. Required.|

## Request body
In the request body, supply a JSON representation of the [conversationMember](../resources/conversationmember.md) object.

The following table shows the properties that are required when you update the [conversationMember](../resources/conversationmember.md).

|Property|Type|Description|
|:---|:---|:---|
|id|String|**TODO: Add Description** Inherited from [entity](../resources/entity.md)|
|roles|String collection|**TODO: Add Description**|
|displayName|String|**TODO: Add Description**|
|visibleHistoryStartDateTime|DateTimeOffset|**TODO: Add Description**|



## Response

If successful, this method returns a `200 OK` response code and an updated [conversationMember](../resources/conversationmember.md) object in the response body.

## Examples

### Request
<!-- {
  "blockType": "request",
  "name": "update_conversationmember"
}
-->
``` http
PATCH https://graph.microsoft.com/beta/chats/{chatsId}/members/{conversationMemberId}
Content-Type: application/json
Content-length: 178

{
  "@odata.type": "#microsoft.graph.conversationMember",
  "roles": [
    "String"
  ],
  "displayName": "String",
  "visibleHistoryStartDateTime": "String (timestamp)"
}
```


### Response
**Note:** The response object shown here might be shortened for readability.
<!-- {
  "blockType": "response",
  "truncated": true
}
-->
``` http
HTTP/1.1 200 OK
Content-Type: application/json

{
  "@odata.type": "#microsoft.graph.conversationMember",
  "id": "1e8dc7a5-c7a5-1e8d-a5c7-8d1ea5c78d1e",
  "roles": [
    "String"
  ],
  "displayName": "String",
  "visibleHistoryStartDateTime": "String (timestamp)"
}
```

