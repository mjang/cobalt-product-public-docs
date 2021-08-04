---
title: "Glossary"
linkTitle: "Glossary"
weight: 100
description: >
 Learn more about the language of software security.
---

{{% pageinfo %}}
The [Internet Security Glossary](https://datatracker.ietf.org/doc/html/rfc4949#section-4) includes
terms defined by the Internet Engineering Task Force. Use this glossary to supplement your knowledge.
{{% /pageinfo %}}


## API Endpoint

An endpoint is typically a URL used to allow two software applications to communicate with each other.
For example, `https://api.cobalt.io/orgs` is one endpoint that you can find at `https://docs.cobalt.io`.

Some endpoints include additional information that may make them seem different. For example, the
following two URLs are in fact the same endpoint, as the content after the ampersand (&) describes an
action on data sent from that URL:

- https://www.example.com/endpoint1&_prettyPrint=true
- https://www.example.com/endpoint1&_prettyPrint=false

## Asset

For pentesting, an asset is a software component of value. Cobalt can perform pentests on assets in the
following categories:

{{% asset-categories %}}

## Dynamic Page

Web applications typically include _static_ and _dynamic_ web pages. A Dynamic Page includes content
that can be customized, either through an application server (server-side) or through code such as
JavaScript running in the browser (client-side).

## Mobile Screen

A mobile screen is what you see on a mobile device, such as an iPhone or an Android system. As
described by [Codepath](https://guides.codepath.com/android/Mobile-Screen-Archetypes), mobile 
screens fall into several archetypes. 

You may have multiple screens of an archtype. For example, you may have 10 mobile screens for
the onboarding archtype.

## Operations Security (OpSec)

Operations Security, commonly known as OpSec, identifes critical information, and if/how it
may be used by opponents or enemies. OpSec measures can reduce security risks.

## Single-page Application

For more information, see https://developer.mozilla.org/en-US/docs/Glossary/SPA

## User Role

A User Role specifies the permissions or privileges associated with a user. Common examples of User Roles include:

- Global Administrator (such as a UNIX root user)
- Administrator
- Group Owner
- Workspace Administrator
- Full User
- Guest

This is not a comprehensive list. When scoping an Asset, it's important to include a complete number of user roles. If you miss a user role, you may sacrifice quality in penetration testing. 


### Header 3

```
This is a code block following a header.
```
