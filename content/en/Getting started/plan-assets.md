---
title: "Plan Your Assets"
linkTitle: "Plan Your Assets"
weight: 10
description: >
  Security professionals perform pentests on your "assets". Collect the info they need.
---

{{% pageinfo %}}
Help our pentesters test your assets more quickly.
{{% /pageinfo %}}

To set up a pentest, you'll want to set up the following:

- Asset Image: Use it to help identify what you need from a list of many assets.
- Asset Title: Set up a descriptive name to attract attention from the best pentesters.
- Asset Type: Select one of the options described shortly.
- Asset Scoping: Use the guidance on this page to select a size and scope for your asset.
- Asset Description: Add information that can help your pentester fully analyze your asset.

For each asset, we provide guidance for each of the following asset categories:  

<!-- Pulls info from the layouts/shortcodes/<name>.html file --> 
{{% asset-categories %}}

We also support tests that span multiple categories, including:

- Web + API
- Web + External Network
- Web + Mobile

The following sections can help you understand the following characteristics of assets:

- Different types
- How to scope an asset
- The coverage you need

Scoping is a complex topic. The following sections include basic guidance on how to scope
each type of Asset. For more information on how scoping and coverage levels drive pentest
credit recommendations, see our [Scoping Guide](../scoping-guide).

## Web

To scope a Web asset, you need to specify the number of the following
characteristics of that asset:

- [User Roles](../glossary#user-role)
- [Dynamic Pages](../glossary#dynamic-pages)

When scoping an Asset, include every User Role and Dynamic Page.
If you forget some, you may sacrifice quality in penetration testing.

Cobalt subdivides the number of User Roles and Dynamic Pages into the following categories:

|               | Extra Small | Small   | Medium   | Large    | Extra Large |
|---------------|-------------|---------|----------|----------|-------------|
| User Roles    | 1           | 1 - 2   | 3 - 5    | 5 - 7    | > 8         |
| Dynamic Pages | 0 - 30      | 30 - 60 | 60 - 90  | 90 - 120 | > 120       |

If your numbers of User Roles and Dynamic Pages fit into different categories,
use your judgment. If you choose a "bigger" category, you're likely to
get a more complete test. You can also consult your Technical Account Manager for advice.

As part of our tests for Dynamic Pages, we may also test the backend API endpoints frequently used
to populate content on those pages.

### Web Asset Description

In addition, our pentesters need to know more about your Web asset. In the Asset Description, it's helpful
to include a high-level overview of the application. Pentesters can use also details such as:

- Application type, such as a page-driven website or a [single-page application](https://developer.mozilla.org/en-US/docs/Glossary/SPA)
- Language, such as JavaScript or Ruby on Rails
- A list of user roles, including associated permissions/rights
- Functions or features central to the functionality of your asset
  - Business risks associated with specific functions or features
- Special endpoints associated with your dynamic pages

## Mobile

To scope a Mobile asset, you need to specify the number of the following
characteristics of that asset:

- [User Roles](../glossary#user-role)
- Operating Systems (OS), such as Android, iOS, Windows Phone, and Tizen
- [Mobile Screens](../glossary#mobile-screens)

When scoping an Asset, include every User Role, Operating System, and Mobile Screen.
If you forget some, you may sacrifice quality in penetration testing.

Cobalt subdivides these properties into the following categories:

|               | Extra Small | Small   | Medium   | Large    | Extra Large |
|---------------|-------------|---------|----------|----------|-------------|
| User Roles    | 1           | 1 - 2   | 3 - 5    | 5 - 7    | > 8         |
| Operating Systems | 1       | 1       | 1 - 2    | 1 - 3    | 1 - 3       |
| Mobile Screens | 1 - 19     | 20 - 39 | 40 - 59  | 60 - 79  | > 80        |

If the properties for your mobile app fit into different categories,
use your judgment. If you choose a "bigger" category, you're likely to
get a more complete test. You can also consult your Technical Account Manager for advice.

## API

To scope an API, you need to specify the number of the following
characteristics of that asset:

- [User Roles](../glossary#user-role)
- [(API) Endpoints](../glossary#api-endpoints)

When scoping an Asset, do include every User Role and Endpoint.
If you forget some, you may sacrifice quality in penetration testing.

Cobalt subdivides the number of User Roles and Dynamic Pages into the following categories:

|               | Extra Small | Small   | Medium   | Large    | Extra Large |
|---------------|-------------|---------|----------|----------|-------------|
| User Roles    | 1           | 1 - 2   | 3 - 5    | 5 - 7    | > 8         |
| Endpoints     | 0 - 74      | 75-149  | 150-224  | 225-299  | 300-374     |

If your numbers of User Roles and Endpoints fit into different categories,
use your judgment. If you choose a "bigger" category, you're likely to
get a more complete test. You can also consult your Technical Account Manager for advice.

## External Network

To scope an External Network, you need to specify the number of affected public IP addresses:

|                        | Extra Small   | Small       | Medium     | Large      | Extra Large |
|------------------------|---------------|-------------|------------|------------|-------------|
| Public IP Addresses    | 1 - 149       | 150 - 299   | 300 - 449  | 450 - 599  | 600 - 749   |

If you're working with more external IP addresses, you can set up multiple external network
assets. One way to organize such assets is by subnet.

## Internal Network

To scope an Internal Network, you need to specify the number of affected IP addresses and servers:

|                        | Extra Small   | Small       | Medium     | Large      | Extra Large |
|------------------------|---------------|-------------|------------|------------|-------------|
| Private IP Addresses   | 1 - 149       | 150 - 299   | 300 - 449  | 450 - 599  | 600 - 749   |
| Servers                | 1 - 49        | 50 - 99     | 100 - 149  | 150 - 199  | 200 - 249   |

If you're working with more internal IP addresses, you can set up multiple internal network
assets. One way to organize such assets is by subnet.

If you're working with servers on the cloud, you can also set up a [Cloud Configuration](cloud-configuration)
asset.

## Cloud Configuration

Cobalt pentesters can test services on the following platforms:

- Google Cloud Platform (GCP)
- Amazon Web Services (AWS)
- Microsoft Azure Cloud (Azure)

Each platform includes different categories of services, such as EC2, databases, and machine
learning engines.

To scope a Cloud Configuration asset, total the number of services you use on that asset.

|                        | Extra Small  | Small     | Medium     | Large      | Extra Large |
|------------------------|--------------|-----------|------------|------------|-------------|
| Services               | 1 - 49       | 50 - 99   | 100 - 149  | 150 - 199  | 200 - 249   |

If you're working with more services, you can set up multiple cloud configuration assets.

## Assets of Multiple Types

In many cases, assets fit into multiple categories. To that end, Cobalt supports pentests on
assets in the following groups of categories:

- Web + API
- Web + Internal Network
- Web + Mobile 

The challenges with each of these combined asset types is different:

### Web + API

As described in the [Web](#web) section, the Web asset type already includes tests of _backend_ APIs.
Many web applications also include tests of _frontend_ APIs. If you want test coverage of those APIs,
this asset type may be for you.

The scoping criteria for a Web + API asset is a subset of that of a Web asset alone: 

(Split into three tables)

|                                         | Extra Small                         | Small                               | Medium                              | Large                               | Extra Large                         |
|-----------------------------------------|-------------------------------------|-------------------------------------|-------------------------------------|-------------------------------------|-------------------------------------|
| User Roles                              |                                     |                                     | 1 - 2                               | 1 - 4 <br>  5 - 7                   | 1 - 7 <br>  8+                      |
| User Roles: More Frontend Endpoints     |                                     | 0 - 75                              | 1                                   |                                     |                                     |
| User Roles: Fewer Frontend Endpoints    | 1                                   | 1 - 2                               | 3 - 5                               |                                     |                                     |
| Dynamic Pages                           | 0 - 29                              | 0 - 29 <br>  0 - 59                 | 0 - 29 <br>  0 - 59 <br>  0 - 89    | 0 - 29 <br>  0 - 119                | 0 - 29 <br>  0 - 149                |
| Dynamic Pages: More Frontend Endpoints  |                                     |                                     |                                     |                                     |                                     |
| Dynamic Pages: Fewer Frontend Endpoints |                                     |                                     |                                     |                                     |                                     |
| Frontend API Endpoints                  |                                     |                                     | 0 - 74                              |                                     |                                     |
| Frontend API Endpoints (more)           |                                     | 0 - 74                              | 0 - 149                             | 0 - 224                             | 0 - 299                             |
| Frontend API Endpoints (fewer)          | 0 - 9 or <br> 95% backend endpoints | 0 - 9 or <br> 95% backend endpoints | 0 - 9 or <br> 95% backend endpoints | 0 - 9 or <br> 95% backend endpoints | 0 - 9 or <br> 95% backend endpoints |

If your numbers of User Roles, Frontend endpoints, and Dynamic Pages fit into different categories,
use your judgment. If you choose a "bigger" category, you're likely to
get a more complete test. You can also consult your Technical Account Manager for advice.

In addition, our pentesters need to know more about your Web asset, including:

- Language, such as JavaScript or Ruby on Rails
- Application type, such as a page-driven website or a [single-page application](https://developer.mozilla.org/en-US/docs/Glossary/SPA)
- Special endpoints associated with your dynamic pages

As part of our tests for Dynamic Pages, we may also test the backend API endpoints frequently used
to populate content on those pages.

### Web + External Network

### Web + Mobile
