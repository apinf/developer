## Getting started 

From this site you'll find detailed information about our practices. 

## What is APInf Platform? 

## Platform development

### Understand what you are dealing with

- Architecture
- Code practices

### Contribution process

### Contributor License Agreement

### Issues

Easiest way to follow development is to look at issues in Waffle. Other option is to use Github issues list. 
- [APInf Platform in Waffle.io](https://waffle.io/apinf/platform)
- [APInf Platform issues in Github](https://github.com/apinf/platform/issues)

For new issues we have template in Github which will guide you to fill in needed information. 

### Set up local development version 
Start developing the platform by installing APInf platform. You can do this multiple ways. [Here's more detailed information](https://github.com/apinf/platform/blob/develop/INSTALL.md) how to do it. 


## Platform API development

Our platform contains multiple APIs. What ever can be done from GUI, you can do it with API. For each platform API we have two branches:
- production (with multiple versions) and
- design (the future version)

Production API is the live one and fully functional version. The design has been frozen. It might change, but changes are not backwards breaking. Design branch is the next API version (minor/major changes). 

Currently we have following APIs: 
- **Catalog API** ([Production version 1](https://apinf.io/apis/apinf-catalog-rest-api-1) and [Development branch](https://apinf.io/apis/apinf-catalog-rest-api-design))
- **Management API** ([Production version 1](https://apinf.io/apis/apinf-management-rest-api))
- **Flow API** (Development branch)

In APInf we use unified process for Platform API development. Platform APIs are non-profit APIs. Our intention is not to charge clients for using them. They are part of the platform.

We use [OpenAPI spec version 2.0](https://github.com/OAI/OpenAPI-Specification/blob/master/versions/2.0.md) in API design and documentation. 


Code related to [APIs can be found from here](https://github.com/apinf/platform/tree/develop/apinf_packages/apis)

### API Design Guide
We have defined set of rules for API development. 
- [Read API Design Guide first.](https://apinf.gitbooks.io/api-guidelines/content/)
- [Overall process is good to understand](https://apinf.gitbooks.io/api-guidelines/content/process.html)


## UX development

### UX Design Guide

- [UX Design Guide]() 

## Automated testing

We use automated testing. This means that you start developing new features by defining test first. 
