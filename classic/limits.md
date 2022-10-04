---

copyright:
  years: 2020, 2022
lastupdated: "2022-10-03"

keywords: known limitations, rules, limits, configuration, ibm remediation, ssh key

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


# Known issues and limits
{: #known-issues-limits}

{{site.data.keyword.compliance_full}} includes the following known issues and limits that might impact your experience.
{: shortdesc}


## Known issues
{: #known-issues}

Review the following known issues that you might encounter while you work with the service.
 
| Issue  | Workaround |
|:-------|:-----------|
| Remediation is unavailable for {{site.data.keyword.cloud_notm}}. | If you're working with Amazon Web Services (AWS) or Azure, you can [remediate issues](/docs/security-compliance?topic=security-compliance-remediation) directly from the service UI. If you're working in {{site.data.keyword.cloud_notm}}, you must manually remediate your issues. |
| Results for {{site.data.keyword.cloud_notm}} Classic Infrastructure are not returned. | It is not possible to scan classic infrastructure as a cloud-based resource. To monitor security and compliance for classic infrastructure, configure an on-prem collector. |
| Results for the resource view are not returned. | The resource view is unavailable if the total number of goals in a profile that is attached to your scan exceeds 560. If you are processing a large scan, you can use the control view or drift view to see your results. |
| Your scan does not run when you're working with an IBM-managed collector. | IBM-managed collectors are configured to scan a maximum of 350 resources at a time. To use an IBM-managed collector, you can narrow your scope to a smaller set of resources, or you can use a customer-managed collector. |
| You cannot create a second integration. | Only one integration can be created for each name or URL. If you need to update your integration in some way, delete the integration and create a new one. |
{: caption="Table 1. Known issues and workarounds" caption-side="top"}


## Limits
{: #limits}

When you're working with {{site.data.keyword.compliance_short}}, there are a few limits on rules and templates that you need to be aware of.

### Rule limits
{: #rule-limits}

Review the following table to see the limits that apply to rules.

|  | Limit |
|----------------|-----------|
| Total rules | 500 rules per enterprise account</br>100 rules per stand-alone account |
| Rule length | 4096 characters |
| Name length | 32 characters |
| Description length | 256 characters |
| Targets | 1 per rule |
| Conditions | 16 per rule |
| Properties | 24 per condition |
| Enforcement actions | 2 per rule |
| Labels | 32 per rule |
| Label length | 64 characters </br> **Note**: Commas (,) and slashes (/) cannot be used in labels. |
| Attachments | 10 per rule |
| Excluded scopes | 8 per attachment |
| Results | Kept for 7 days |
{: row-headers}
{: caption="Table 2. Rule limits" caption-side="top"}


### Template limits
{: #template-limits}

Review the following table to see the limits that apply to templates.

|  | Limit |
|----------------|-----------|
| Total templates | 500 templates per enterprise account</br>100 templates per stand-alone account |
| Template length | 4096 characters |
| Name length | 32 characters |
| Description length | 256 characters |
| Properties | 24 per template |
| Attachments | 10 per template |
| Excluded scopes | 8 per attachment |
{: row-headers}
{: caption="Table 3. Template limits" caption-side="top"}


### IBM-managed collector limits
{: #ibm-collector-limits}

Review the following table to see the limits that apply to IBM-managed collectors.

|  | Limit |
|----------------|-----------|
| Number of collectors | 1 per account |
| Number of scannable resources | 900 resources per managed-collector |
| Scanable environments | Collectors that are managed by IBM are deployed on IBM owned infrastructure, which means that they cannot access a customer's owned servers. If you're working within an *On-premises* environment, you must you a customer-managed collector. |
{: row-headers}
{: caption="Table 4. Collector limits" caption-side="top"}
