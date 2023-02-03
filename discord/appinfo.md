---
title: Application Information
layout: default
parent: Discord
nav_order: 1
---
STABLE
{: .label .label-green }

# **Discord Application Information**
You can use this endpoint to fetch information about an application on Discord.

## Information
**Endpoint:** `https://logic.rest/api/v1/discord/application/:id`

### Versions 
<table>
  <tr>
    <th>Supported Versions</th>
    <th>Latest Version</th>
  </tr>
  <tr>
    <td>v1</td>
    <td>v1</td>
  </tr>
</table>

### Parameters 
<table>
  <tr>
    <th>Name</th>
    <th>Required</th>
    <th>Description</th>
  </tr>
  <tr>
    <td>:id</td>
    <td>true</td>
    <td>The ID of a Discord Application</td>
  </tr>
</table>

### Example Response
```json
{
  "status":200,
  "data": {
    "id":"1065368179494359071",
    "name":"logic.rest",
    "description":"The official application for https://logic.rest",
    "icon_code":"b012035185190963be7a49a51e732ddb",
    "type":null,
    "hook":true,
    "terms_of_service_url":"https://logic.rest/terms",
    "privacy_policy_url":"https://logic.rest/privacy",
    "tags":["API","Viality Software"],
    "verify_key":"7f04f960f814b27de63641866c31cb52fccf67c59f09fcb920f8345783a4b5ec",
    "flags":2662400,
    "bot": {
       "id":"1065368179494359071",
       "username":"logic.rest",
       "discriminator":"9232",
       "avatar_code":"b012035185190963be7a49a51e732ddb",
       "is_public?":false,
       "requires_code_grant?":false,
       "approximate_guild_count":1
    }
  }
}
```

### JavaScript Example
```javascript
const fetch = (...args) => import('node-fetch').then(({default: fetch}) => fetch(...args));

const id = 123; // Replace with a Discord Application ID

const response = await fetch(`https://logic.rest/api/v1/discord/application/${id}`);
const data = await response.json();
console.log(data);
```
