# Budibase Keycloak Redirect

budi-keycloak-redirect is a Budibase plugin that navigates the app to Keycloak login page when the user is not authenticated.

## Component schema

| Field | Type | Required | Description |
| --- | --- | --- | --- |
| id | String | Yes | Provider ID |
| appPath | String | Yes | Path of published app |
| userId | String | Yes | User ID |

## Description

A Budibase plugin is a Svelte component under the hood. On component mount, the app navigates to the login page if the user is not authenticated. No additional condition is required.

## Instructions

```bash
# To build your new  plugin run the following in your Budibase CLI:
budi plugins --build

# You can also re-build everytime you make a change to your plugin with the command:
budi plugins --watch
```

## Usage

<aside>
💡 You must provide a path to your plugins folder so that Budibase knows where to import the plugins that you update while developing.

</aside>

1. Add this plugin
2. Configure the following parameters
    1. Provider ID
    2. App Path
    3. User ID

<aside>
💡 You can find the Provider ID at /api/global/configs/public/oidc?tenantId=default

</aside>