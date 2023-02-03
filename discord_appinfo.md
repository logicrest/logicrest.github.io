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
| Supported Versions | Latest Version |
|:------ | :------ |
| v1 | v1 |

### Parameters 
| Name | Required? | Description |
|----------|----------|----------|
| :id | true | The ID of a Discord Application |

### JavaScript Example
```javascript
const fetch = (...args) => import('node-fetch').then(({default: fetch}) => fetch(...args));

const id = 123; // Replace with a Discord Application ID

const response = await fetch(`https://logic.rest/api/v1/discord/application/${id}`);
const data = await response.json();
console.log(data);
```
