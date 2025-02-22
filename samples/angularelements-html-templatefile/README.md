---
page_type: sample
products:
- office-sp
- office-365
languages:
- javascript
- typescript
extensions:
  contentType: samples
  technologies:
  - SharePoint Framework
  platforms:
  - AngularJS
  createdDate: 1/8/2019 12:00:00 AM
---

# Angular Elements with HTML Template File in SharePoint Framework

## Summary

A sample web part illustrating how to use Angular Elements in the SharePoint Framework with the help of separate template HTML File.

## Compatibility

![SPFx 1.4.1](https://img.shields.io/badge/SPFx-1.4.1-green.svg)
![Node.js v6 | v8](https://img.shields.io/badge/Node.js-LTS%206.x%20%7C%20v8-green.svg)
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
angularelements-html-templatefile| [Jayakumar Balasubramaniam](https://github.com/JayakumarB) (C# Corner MVP, Hubfly, [@jayakumrB](https://twitter.com/jayakumrB))

## Version history

Version|Date|Comments
-------|----|--------
1.0|Jan 8, 2019|Initial release

## Minimal Path to Awesome

* clone this repo
* in the command line run:
  * `npm i`
  * `gulp serve`

## Features

This web part illustrates the following concepts on top of the SharePoint Framework:

* adding Angular Elements to a no-framework SharePoint Framework project
* bootstrapping Angular Elements inside a SharePoint Framework web part
* extending the building configuration to build Angular Elements
* utilizing build pipeline to compile and run angular template files in gulpfile.js

## Implementation

The below piece of code in gulpfile.js is the key to update the build pipeline:
```typescript
//************START: Added to handle Template file url ************/

var inlineNgxTemplate = require('gulp-inline-ngx-template');
var ts = require('gulp-typescript');
var tsProject = ts.createProject('./tsconfig.json');

let tsInlines = build.subTask('tsInlines', function(gulp, buildOptions, done) {
  return  gulp.src('src/webparts/helloAngularTemplate/app/**/*.ts')
       .pipe(inlineNgxTemplate({ base: '/src/webparts/helloAngularTemplate/app/', useRelativePaths: true }))
       .pipe(tsProject())
       .pipe(gulp.dest('lib/webparts/helloAngularTemplate/app'));
})

build.rig.addPostTypescriptTask(tsInlines);

//************END: Added to handle Template file url ************/
```


## Help

We do not support samples, but we this community is always willing to help, and we want to improve these samples. We use GitHub to track issues, which makes it easy for  community members to volunteer their time and help resolve issues.

You can try looking at [issues related to this sample](https://github.com/pnp/sp-dev-fx-webparts/issues?q=label%3A%22sample%3A%20angularelements-html-templatefile") to see if anybody else is having the same issues.

You can also try looking at [discussions related to this sample](https://github.com/pnp/sp-dev-fx-webparts/discussions?discussions_q=angularelements-html-templatefile) and see what the community is saying.

If you encounter any issues while using this sample, [create a new issue](https://github.com/pnp/sp-dev-fx-webparts/issues/new?assignees=&labels=Needs%3A+Triage+%3Amag%3A%2Ctype%3Abug-suspected%2Csample%3A%20angularelements-html-templatefile=@JayakumarB&template=bug-report.yml&sample=angularelements-html-templatefile=@JayakumarB&title=angular-todo%20-%20).

For questions regarding this sample, [create a new question](https://github.com/pnp/sp-dev-fx-webparts/issues/new?assignees=&labels=Needs%3A+Triage+%3Amag%3A%2Ctype%3Aquestion%2Csample%3A%20angularelements-html-templatefile=@JayakumarB&template=question.yml&sample=angularelements-html-templatefile=@JayakumarB&title=angular-todo%20-%20).

Finally, if you have an idea for improvement, [make a suggestion](https://github.com/pnp/sp-dev-fx-webparts/issues/new?assignees=&labels=Needs%3A+Triage+%3Amag%3A%2Ctype%3Aenhancement%2Csample%3A%20angularelements-html-templatefile=@JayakumarB&template=question.yml&sample=angularelements-html-templatefile=@JayakumarB&title=angular-todo%20-%20).


## Disclaimer

**THIS CODE IS PROVIDED *AS IS* WITHOUT WARRANTY OF ANY KIND, EITHER EXPRESS OR IMPLIED, INCLUDING ANY IMPLIED WARRANTIES OF FITNESS FOR A PARTICULAR PURPOSE, MERCHANTABILITY, OR NON-INFRINGEMENT.**


<img src="https://pnptelemetry.azurewebsites.net/sp-dev-fx-webparts/samples/angularelements-helloworld" />
