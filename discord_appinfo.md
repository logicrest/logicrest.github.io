---
title: Application Information
layout: default
parent: Discord
nav_order: 1
---
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

### JavaScript Example
```javascript
const fetch = (...args) => import('node-fetch').then(({default: fetch}) => fetch(...args));

const id = 123; // Replace with a Discord Application ID

const response = await fetch(`https://logic.rest/api/v1/discord/application/${id}`);
const data = await response.json();
console.log(data);
```
