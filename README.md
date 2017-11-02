## For whom is this?

From this site you'll find detailed information about our platform development practices. This is not APInf Platform user guide. 

**Intended audience is people who develop the platform regardless of are they employees of APInf Oy or community members.**

<hr/>

## What is APInf Platform? 

APInf platform offers a comprehensive, yet easy to use API management tool. APInf provides simplified workflow for API owners for common API management tasks so you can focus on building your APIs.

![APInf Platform overview](https://raw.githubusercontent.com/apinf/developer/master/apinf-overview.png)

You can publish your API in the APInf catalog without connecting it to a proxy. But connecting the API provides you with the possibility to use traffic management features, authorization and logging. The proxy acts as a façade for your API: the API clients are not accessing your API directly.​ You can manage both REST APIs and Iot APIs (MQTT) with APInf.

Publishing your API in the catalog gives better visibility for your API. The API can be published with one single step: fill in the access URL, name and description and get going! We highly recommend also adding a logo for your API – after all the API should be an easily identifiable product.

You can provide an OpenAPI documentation file for your API by uploading a file or providing a link to your file. Good API documentation saves frustration from developers and minimizes support needs from them. They can not only read the document, they can try out the calls in practice.

If you connect your API to the proxy, you can follow your API traffic and different API KPIs in the dashboard. You can monitor API response times, HTTP response types, numbers of users and most frequent users for the selected time frames. This allows you to identify for example your most popular APIs, traffic peaks or performance problems.

## Platform development

### Understand what you are dealing with

- [System model](https://raw.githubusercontent.com/apinf/docs/master/docs/develop/Architecture/Apinf-systemModel.png)
- [Permission model](https://raw.githubusercontent.com/apinf/docs/master/docs/develop/Architecture/Apinf-permissionsModel.png)
- [APINf roles](https://github.com/apinf/docs/blob/master/docs/develop/Architecture/User-Roles-in-Apinf.md)
- Code practices

### Roadmap

APInf roadmap is decided inside the team. Decisions are business driven, but take into account technical requirements and limitations. Our roadmap is "event driven" which means that we pick bigger ICT events as milestones.   

- [Roadmap for development](https://waffle.io/apinf/roadmap)

### Licensing policy

We use EUPL license for core components. 

### Contribution process

### Contributor License Agreement

### Issues

Easiest way to follow development is to look at issues in Waffle. Other option is to use Github issues list. 
- [APInf Platform in Waffle.io](https://waffle.io/apinf/platform)
- [APInf Platform issues in Github](https://github.com/apinf/platform/issues)

For new issues we have template in Github which will guide you to fill in needed information. 

### Automated testing

We use automated testing. This means that you **start developing new features by defining test first**. 

### Set up local development version 
Start developing the platform by installing APInf platform. You can do this multiple ways. [Here's more detailed information](https://github.com/apinf/platform/blob/develop/INSTALL.md) how to do it. 

### Platform branches
We have three instances running. Each of them have different purpose. 

- **Our production enviroment** is available at [apinf.io](https://apinf.io) This is our SaaS version
- **Staging**, [https://staging.apinf.io](https://staging.apinf.io) is for maturing the next version before launch to production (see above)
- **Nightly**, [https://nightly.apinf.io](https://nightly.apinf.io) is our nightly build version of the platform. 

## Platform API development

Our platform contains multiple APIs. What ever can be done from GUI, you can do it with API. For each platform API we have two branches:
- production (with multiple versions) and
- design (the future version)

Production API is the live one and fully functional version. The design has been frozen. It might change, but changes are not backwards breaking. Design branch is the next API version (minor/major changes). 

### Currently we have following APIs 
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

## APIBot Development
What is APIBot? 

## Open API Designer
What is Open API Designer


