github-action_serverless.java
---
```
layout: Conceptual
title: SharePoint Embedded Overview | Microsoft Learn
[canonical Url](https://learn.microsoft.com/en-us/sharepoint/dev/embedded/overview)
uhfHeaderId: MSDocsHeader-M365-IT
"breadcrumb_path/sharepoint/dev/breadcrumb/toc.json"
ms.suite: office
ms.author: techphan573-executive@invest86
author: Michael Glenn
ms.topic: techphan573
search.appverid: MET150
ms.service: sharepoint-online
description: Microsoft SharePoint Embedded is a cloud-based file and document management system suitable for use in any application. SharePoint Embedded is a new API-only solution that enables app developers to harness the power of the Microsoft 365 file and document storage platform for any app, and is suitable for enterprises building line-of-business applications and ISVs building multitenant applications.
ms.date: 2024-08-17TZ
ms.localizationpriority: high
locale: en-us
document_id: 3cdc7a81-923a-fbb8-8a4c-a964d9ecd2cf
document_version_independent_id: 3cdc7a81-923a-fbb8-8a4c-a964d9ecd2cf
updated_at: 2026-03-02T13:40:Z
original_content_git_url: https://github.com/SharePoint/sp-dev-docs/blob/live/docs/embedded/overview.md
gitcommit: https://github.com/SharePoint/sp-dev-docs/blob/928454f5352645df277bf4e46fbffe79ac2a2988/docs/embedded/overview.md
git_commit_id: 928454f5352645df277bf4e46fbffe79ac2a2988
site_name: Docs
depot_name: MSDN.sharepoint-dev
page_type: conceptual
toc_rel/toc.json
pdf_url_template: https://learn.microsoft.com/pdfstore/en-us/MSDN.sharepoint-dev/{branchName}{pdfName}
feedback_help_link_type: ''
feedback_help_link_url: ''
word_count: 780
asset_id: embedded/overview
item_type: Content
source_path: docs/embedded/overview.md
Products:
- https://authoring-docs-microsoft.poolparty.biz/devrel/9d7be3ef-f27c-4c7f-9eba-67c3cd429995
- https://authoring-docs-microsoft.poolparty.biz/devrel/1dd701e0-441f-4b0a-9806-aa47decc4e35
Products:
- https://authoring-docs-microsoft.devrel/feeb50f3-b677-44f9-b3a6-5f2f58182b0d
- https://authoring-docs-microsoft.devrel/0a2fc935-5977-4aa6-9f55-0be03bd2acb8
platformId: df55a8f2-9a5e-37a5-be01-87433f5ab21d
---
```

# SharePoint Embedded Overview | Microsoft Learn

Microsoft SharePoint Embedded is a cloud-based file and document management system suitable for use in any application. SharePoint Embedded is a new API-only solution that enables app developers to harness the power of the Microsoft 365 file and document storage platform for any app, and is suitable for enterprises building line-of-business applications and ISVs building multitenant applications.



SharePoint Embedded allows you to integrate advanced Microsoft 365 features into your apps including full-featured collaborative functions from Office, Purview's security and compliance tools, and Copilot capabilities.



Important



Help us shape the future of SharePoint Embedded! Take our [quick survey](https://forms.microsoft.com/r/1YpGd2pAUS) and share your experience!



## App documents stay in their Microsoft 365 tenant



When a consumer uses a SharePoint Embedded application in their Microsoft 365 tenant, SharePoint Embedded creates another partition within their tenant. This storage partition doesn't have a user experience and the documents in the partition are only accessible via APIs. This means that all documents will be accessible to the developer’s application, but the documents will only reside in the consumer’s Microsoft 365 tenant. Within this new storage partition inside of a Microsoft 365 tenant, a SharePoint Embedded application can create many "File Storage Containers" for storing content.



## Introducing File Storage Containers



SharePoint Embedded applications use Microsoft Graph APIs to store files and documents in a new entity called a "File Storage Container” or Container for short. If you’re an ISV, your app will create these containers in your customer’s Microsoft 365 tenant, and if you’re an enterprise, your app will create these containers in your own tenant. Each container provides a place to store files - you can think of them as similar to an API-only Document Library in SharePoint, but with some slight differences. Your app can create many of these containers inside each tenant that uses your app, and each container can be granted permissions separately storing many files with multiple terabytes of content.



SharePoint Embedded containers are dedicated to and accessible by just your app, so the files and documents your app depends on are isolated and secure within that tenant boundary.



## App-managed content experiences



By default, the content stored within a Microsoft 365 tenant by a SharePoint Embedded application is only accessible through that owning application. Applications using SharePoint Embedded also provide the user experience layer for accessing and managing content, using some of the rich content capabilities that Microsoft 365 offers such as:



- Core content management features like support for any file type and folder structure, searching, sharing, automatic versioning, recycle-bin, and more

- Collaboration features like view, edit, and co-authoring Office Word, Excel, and PowerPoint documents in Office Web and Desktop



SharePoint Embedded is used by several types of applications:



- Certain Microsoft products use SharePoint Embedded to manage customer content, such as Loop and Designer.

- ISVs can use SharePoint Embedded in their apps to manage content within their customer’s Microsoft 365 tenant

- Enterprises can use SharePoint Embedded to manage and store content within their own Microsoft 365 tenant, but outside of regular Microsoft 365 entitlements



## Consumer Microsoft 365 settings apply to app documents



All documents stored in the SharePoint partition created by the SharePoint Embedded app are in the consumer’s Microsoft 365 tenant and therefore are subject to the consumer’s Microsoft 365 tenant settings.



This includes settings from Microsoft Purview compliance, risk, and security settings, documents can be opened from Office clients, and customers can use the Office web clients to view and collaborate on the documents. Choosing applications that are built on SharePoint Embedded provides the app consumer Microsoft Purview security and compliance capabilities on that app content, such as:



- Discovery

- Auditing

- Data loss prevention (DLP)

- Retention policies, sensitivity labels, conditional access



## Understanding the costs and billing for SharePoint Embedded content



Microsoft 365 customers have different entitlements related to storage, usage, and features depending on the licenses the customer has purchased.



The partition created in the consumer’s Microsoft 365 tenant by a SharePoint Embedded app doesn’t count towards other Microsoft 365 entitlements including the total amount of Microsoft SharePoint storage that can be used by your organization. Instead, the partition in the consumer’s Microsoft 365 tenant by the SharePoint Embedded app are billed separately through an Azure subscription on a pay-as-you-go metered consumption model that’s based on total storage in active and archived state and the number of API calls.



Note



Learn more about billing for SharePoint Embedded, see [Billing Meters](administration/billing/meters).



## Get Started with SharePoint Embedded



[Review the prerequisites](administration/billing/billing)



Create a "File Storage Container" in 15 minutes or less:



- [Free trial: SharePoint Embedded for Visual Studio Code](getting-started/spembedded-for-vscode)



Follow manual set-up on SharePoint Embedded from the following Microsoft Learning modules:



- [Microsoft Learning: SharePoint Embedded - overview & configuration](/en-us/training/modules/sharepoint-embedded-setup)

- [Microsoft Learning: SharePoint Embedded - building applications](/en-us/training/modules/sharepoint-embedded-create-app)
