---
page_type: sample
products:
- office-sp
languages:
- javascript
- typescript
extensions:
  contentType: samples
  technologies:
  - SharePoint Framework
  platforms:
  - react
  createdDate: 5/1/2017 12:00:00 AM
---
# Using @pnp/js with Async / Await

## Summary

This web part demonstrates how to use [PnPJS](https://pnp.github.io/pnpjs/) with Async functions into the SharePoint Framework as well as integrating [PnP JS and SPFx Logging systems](https://blog.josequinto.com/2017/04/30/how-to-integrate-pnp-js-core-and-sharepoint-framework-logging-systems/). Real example querying SharePoint library to show document sizes.

![React-sp-pnp-js-async-await](./assets/async-await-sp-pnp-js.png)


# Compatibility

![SPFx 1.4.1](https://img.shields.io/badge/SPFx-1.4.1-green.svg) 
![Node.js v8 | v6](https://img.shields.io/badge/Node.js-v8%20%7C%20v6-green.svg) 
![Compatible with SharePoint Online](https://img.shields.io/badge/SharePoint%20Online-Compatible-green.svg)
![Compatible with SharePoint 2019](https://img.shields.io/badge/SharePoint%20Server%202019-Compatible-green.svg)
![Does not work with SharePoint 2016 (Feature Pack 2)](https://img.shields.io/badge/SharePoint%20Server%202016%20(Feature%20Pack%202)-Incompatible-red.svg "SharePoint Server 2016 Feature Pack 2 requires SPFx 1.1")
![Local Workbench Compatible](https://img.shields.io/badge/Local%20Workbench-Compatible-green.svg)
![Hosted Workbench Compatible](https://img.shields.io/badge/Hosted%20Workbench-Compatible-green.svg)


## Applies to

* [SharePoint Framework](https://docs.microsoft.com/sharepoint/dev/spfx/sharepoint-framework-overview)
* [Office 365 developer tenant](https://docs.microsoft.com/sharepoint/dev/spfx/set-up-your-developer-tenant)

## Solution

Solution|Author(s)
--------|---------
react-async-await-sp-pnp-js | Jose Quinto ([@jquintozamora](https://twitter.com/jquintozamora) , [blog.josequinto.com](https://blog.josequinto.com))

## Version history

Version|Date|Comments
-------|----|--------
1.2|Jul 20, 2018|Replaced deprecated sp-pnp-js with @pnp/js
1.1|Mar 6, 2018|Update to 1.4.1
1.0|May 1, 2017|Initial release



## Minimal Path to Awesome

- clone this repo
- `$ npm i`
- `$ gulp trust-dev-cert`
- `$ gulp serve `

### Local Mode

A browser in local mode (localhost) will be opened.
https://localhost:4321/temp/workbench.html

### SharePoint Mode

If you want to try on a real environment, open:
https://your-domain.sharepoint.com/_layouts/15/workbench.aspx

## Usage

![React-sp-pnp-js-async-await-code](./assets/async-await-sp-pnp-js-2.png)


## Features

- [Async / Await functionality working with PnP JS sample](https://github.com/jquintozamora/spfx-react-async-await-sp-pnp-js/blob/master/src/webparts/asyncAwaitPnPJs/components/AsyncAwaitPnPJs.tsx#L93)
  - Tested and working on IE11 (as TypeScript config provides Promise polyfill)
- React Container for the initial load. [Smart Component](https://github.com/jquintozamora/spfx-react-async-await-sp-pnp-js/blob/master/src/webparts/asyncAwaitPnPJs/components/IAsyncAwaitPnPJsState.ts)
- [Interface best practices](https://github.com/jquintozamora/spfx-react-async-await-sp-pnp-js/tree/master/src/webparts/asyncAwaitPnPJs/interfaces)
- [PnP JS and SPFx Logging systems integration](https://blog.josequinto.com/2017/04/30/how-to-integrate-pnp-js-core-and-sharepoint-framework-logging-systems)
![React-sp-pnp-js-async-await-code](./assets/pnp-js-logging-spfx.png)


## Disclaimer

**THIS CODE IS PROVIDED *AS IS* WITHOUT WARRANTY OF ANY KIND, EITHER EXPRESS OR IMPLIED, INCLUDING ANY IMPLIED WARRANTIES OF FITNESS FOR A PARTICULAR PURPOSE, MERCHANTABILITY, OR NON-INFRINGEMENT.**


<img src="https://pnptelemetry.azurewebsites.net/sp-dev-fx-webparts/samples/react-async-await-sp-pnp-js" />
