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

For each asset, we provide guidance for each of the following asset categories:  

<!-- Pulls info from the layouts/shortcodes/<name>.html file --> 
{{% asset-categories %}}

We also support tests that span multiple categories, including:

- Web + API
- Web + External Network
- Web + Mobile

The following sections can help you understand:

- Different types of assets
- How to scope each asset
- The coverage you need for each asset.

## Coverage Levels

Cobalt includes the following coverage levels for each asset. The number of credits that we recommend
varies by coverage level:

| Coverage    | Size                                                              |
|-------------|-------------------------------------------------------------------|
| Extra Light | Covers up to two features.                                        |
| Light       | Sufficient for most general compliance test functionality.        |
| Standard    | Normal recommended coverage level for compliance tests.           |
| Large       | Extended coverage for critical assets with complex functionality. |
| Extra Large | Comprehensive test for assets with complex functionality.         |

These are general guidelines. Every situation is unique. You may choose more (or less)
rigorous testing levels.

{{% alert title="Note" color="note" %}}
By default, if you specify an "Extra Small" Asset size, we give you an "Extra Light"
coverage level. You can specify higher or lower coverage levels.
{{% /alert %}}

## Web

To scope a Web asset, you need to specify the number of the following
characteristics of that asset:

- [User Roles](../glossary#user-role)
- [Dynamic Pages](../glossary#dynamic-pages)

When scoping an Asset, do include every User Role and Dynamic Page.
If you forget some, you may sacrifice quality in penetration testing.

Cobalt subdivides the number of User Roles and Dynamic Pages into the following categories:

|               | Extra Small | Small   | Medium   | Large    | Extra Large |
|---------------|-------------|---------|----------|----------|-------------|
| User Roles    | 1           | 1 - 2   | 3 - 5    | 5 - 7    | > 8         |
| Dynamic Pages | 0 - 30      | 30 - 60 | 60 - 90  | 90 - 120 | > 120       |

If your numbers of User Roles and Dynamic Pages fit into different categories,
use your judgment. If you choose a "bigger" category, you're likely to
get a more complete test. You can also consult your Technical Account Manager for advice.

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

If your numbers of User Roles and Dynamic Pages fit into different categories,
use your judgment. If you choose a "bigger" category, you're likely to
get a more complete test. You can also consult your Technical Account Manager for advice.
