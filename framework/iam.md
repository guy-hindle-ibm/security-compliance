---

copyright:
  years: 2020, 2022
lastupdated: "2022-12-15"

keywords: IAM access for {{site.data.keyword.compliance_short}}, permissions for {{site.data.keyword.compliance_short}}, identity and access management for {{site.data.keyword.compliance_short}}, roles for {{site.data.keyword.compliance_short}}, actions for {{site.data.keyword.compliance_short}}, assigning access for {{site.data.keyword.compliance_short}}

subcollection: security-compliance

---

{:codeblock: .codeblock}
{:screen: .screen}
{:download: .download}
{:external: target="_blank" .external}
{:faq: data-hd-content-type='faq'}
{:gif: data-image-type='gif'}
{:important: .important}
{:note: .note}
{:pre: .pre}
{:tip: .tip}
{:preview: .preview}
{:deprecated: .deprecated}
{:beta: .beta}
{:term: .term}
{:shortdesc: .shortdesc}
{:script: data-hd-video='script'}
{:support: data-reuse='support'}
{:table: .aria-labeledby="caption"}
{:troubleshoot: data-hd-content-type='troubleshoot'}
{:help: data-hd-content-type='help'}
{:tsCauses: .tsCauses}
{:tsResolve: .tsResolve}
{:tsSymptoms: .tsSymptoms}
{:java: .ph data-hd-programlang='java'}
{:javascript: .ph data-hd-programlang='javascript'}
{:swift: .ph data-hd-programlang='swift'}
{:curl: .ph data-hd-programlang='curl'}
{:video: .video}
{:step: data-tutorial-type='step'}
{:tutorial: data-hd-content-type='tutorial'}
{:ui: .ph data-hd-interface='ui'}
{:cli: .ph data-hd-interface='cli'}
{:api: .ph data-hd-interface='api'}
{:release-note: data-hd-content-type='release-note'}


# Managing IAM access for {{site.data.keyword.compliance_short}}
{: #access-management}

Access to the {{site.data.keyword.compliance_full}} is controlled by {{site.data.keyword.iamshort}} (IAM). Every user that accesses the {{site.data.keyword.compliance_short}} in your account must be assigned an access policy, with a defined platform IAM role. The policy determines which actions that a user can perform within the context of the {{site.data.keyword.compliance_short}}.

Policies enable access to be granted at different levels. Some options include the following actions:

* Access to manage profiles and controls
* Access to view security and compliance posture and results
* Access to manage event notifications



## Roles and permissions
{: #iam-roles}

After you define the level of access that a user might need, you can assign them a platform access role. Review the following tables that outline which roles are required to perform actions within the {{site.data.keyword.compliance_short}}.

The following tables list the platform access roles that are required to manage collectors, credentials, scopes, validations, and profiles in your accounts.


| Action                          | Description                      | Minimum required role |
| :------------------------------ | :------------------------------- | :---------------- |
| `compliance.admin.settings-read`|	View {{site.data.keyword.compliance_short}} settings for your account.  | Viewer |
| `compliance.admin.settings-update` | Update {{site.data.keyword.compliance_short}} settings for your account. | Administrator |
| `compliance.admin.test-event-send` | Send a test event to a connected {{site.data.keyword.en_short}} service instance. | Administrator |
| `compliance.posture-management.attachments-create` | Create an attachment. | Editor[^attach-1] |
| `compliance.posture-management.attachments-delete` | Delete an attachment. | Editor[^attach-2] |
| `compliance.posture-management.attachments-read` | View the available attachments in your account. | Viewer[^attach-3] |
| `compliance.posture-management.attachments-update` | Update an attachment. | Editor[^attach-4] |
| `compliance.posture-management.collectors-create` | Create a collector. | Editor |
| `compliance.posture-management.collectors-delete` | Delete a collector. | Editor |
| `compliance.posture-management.collectors-read` | View collectors. | Viewer |
| `compliance.posture-management.collectors-update` | Update a collector. | Editor |
| `compliance.posture-management.control-libraries-create` | Create a control library. | Editor |
| `compliance.posture-management.control-libraries-delete` | Delete a control library. | Editor |
| `compliance.posture-management.control-libraries-read` | View the available control libraries in your account. | Viewer |
| `compliance.posture-management.control-libraries-update` | Update a control library. | Editor |
| `compliance.posture-management.control-library-create` | Create a control library. | Editor |
| `compliance.posture-management.control-library-delete` | Delete a control library. | Editor |
| `compliance.posture-management.control-library-read` | View the details of a control library.| Viewer |
| `compliance.posture-management.control-library-update` | Update a control library. | Editor |
| `compliance.posture-management.controls-create` | Add a control to a profile. | Editor |
| `compliance.posture-management.controls-delete` | Delete a control. | Editor |
| `compliance.posture-management.controls-read` | View the controls that you can add to a profile. | Viewer |
| `compliance.posture-management.controls-update` | Update an existing control. | Editor |
| `compliance.posture-management.credentials-create` | Create a credential. | Editor |
| `compliance.posture-management.credentials-delete` | Delete a credential. | Editor |
| `compliance.posture-management.credentials-read` | View credentials. | Viewer |
| `compliance.posture-management.credentials-update` | Update a credential. | Editor |
| `compliance.posture-management.credentialsmap-create` | Map credentials to a scope. | Editor |
| `compliance.posture-management.credentialsmap-delete` | Delete a credentials mapping. | Editor |
| `compliance.posture-management.credentialsmap-read` | View credential mappings. | Viewer |
| `compliance.posture-management.credentialsmap-update` | Edit an existing credential mapping. | Editor |
| `compliance.posture-management.dashboard-view` | View hybrid cloud results. | Viewer|
| `compliance.posture-management.integrations-create` | Create an integration in {{site.data.keyword.compliance_short}}. | Operator |
| `compliance.posture-management.integrations-delete` | Delete an integration in {{site.data.keyword.compliance_short}}. | Editor |
| `compliance.posture-management.integrations-read` | View an integration in {{site.data.keyword.compliance_short}}. | Viewer |
| `compliance.posture-management.integrations-update` | Update an integration in {{site.data.keyword.compliance_short}}. | Operator |
| `compliance.posture-management.keys-delete` | Enable/Disable BYOK configuration | Editor |
| `compliance.posture-management.keys-read` | Read BYOK/KYOK configuration | Viewer|
| `compliance.posture-management.keys-write` | Edit BYOK/KYOK configuration | Editor |
| `compliance.posture-management.profiles-create` | Create a profile. | Editor |
| `compliance.posture-management.profiles-delete` | Delete a profile. | Editor |
| `compliance.posture-management.profiles-read` | View profiles. | Viewer |
| `compliance.posture-management.profiles-update` | Update a profile. | Editor |
| `compliance.posture-management.reports-create` | Download a report. | Operator |
| `compliance.posture-management.reports-list` | View IBM Cloud results. | Operator |
| `compliance.posture-management.reports-read` | View IBM Cloud results. | Operator |
| `compliance.posture-management.scans-create` | Creat a scan. | Editor |
| `compliance.posture-management.scans-delete` | Delete a scan. | Editor |
| `compliance.posture-management.scans-read` | View scans. | Viewer |
| `compliance.posture-management.scans-update` | Update scans. | Editor |
| `compliance.posture-management.scopes-create` | Create a scope. | Editor |
| `compliance.posture-management.scopes-delete` | Delete a scope. | Editor |
| `compliance.posture-management.scopes-read` | View scopes. | Viewer |
| `compliance.posture-management.scopes-update` | Edit a scope. | Editor |
| `compliance.posture-management.tags-create` | Create tags. | Operator |
| `compliance.posture-management.tags-delete` | Delete a tag. | Operator |
| `compliance.posture-management.tags-read` | View tags. | Viewer |
| `compliance.posture-management.tags-update` | Update a tag. | Editor |
| `compliance.posture-management.validations-create` | Run a validation scan. | Editor |
| `compliance.posture-management.validations-delete` | Delete a validation scan. | Editor |
| `compliance.posture-management.validations-read` | View a validation scan. | Viewer |
| `compliance.posture-management.validations-update` | Update a validation scan. | Editor |
| `compliance.posture-management.values-create` | Add parameters to an existing goal. | Editor |
| `compliance.posture-management.values-read` | View the parameters that are associated with a goal. | Viewer |
| `compliance.posture-management.values-update` | Update the parameters of an existing goal. | Editor |
{: caption="Table 1. IAM user roles and actions" caption-side="top"}

[^attach-1]: To create an attachment within an Enterprise, you must also have Administrator access for the Enterprise service.

[^attach-2]: To create an attachment within an Enterprise, you must also have Administrator access for the Enterprise service.

[^attach-3]: To create an attachment within an Enterprise, you must also have Administrator access for the Enterprise service.

[^attach-4]: To create an attachment within an Enterprise, you must also have Administrator access for the Enterprise service.

