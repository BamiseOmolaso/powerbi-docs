---
title: Overview of Copilot for Power BI (preview) 
description: Read all about how Copilot works in Power BI.
author: maggiesMSFT
ms.author: maggies
ms.reviewer: shlindsay
ms.service: powerbi
ms.subservice: pbi-reports-dashboards
ms.topic: conceptual
ms.date: 04/22/2024
LocalizationGroup: Create reports
no-loc: [Copilot]
---

# Overview of Copilot for Power BI (preview)

[!INCLUDE [applies-yes-desktop-yes-service](../includes/applies-yes-desktop-yes-service.md)]

Copilot for Microsoft Fabric Public Preview is available in Power BI. Copilot helps you use the transformational power of generative AI to get the most from your data. This article provides an overview of the Copilot capabilities for Power BI.

Before your business can start using Copilot capabilities in Power BI, your administrator needs to [enable Copilot in Microsoft Fabric](/fabric/get-started/copilot-fabric-overview#enable-copilot).

## Get ready to create reports

Power BI has introduced generative AI that allows you to create reports automatically by selecting the topic for a report or by prompting Copilot on a particular topic, and create a narrative visual that generates a summary of your report using generative AI. The following sections cover the details of the features and how to use Copilot.

:::image type="content" source="media/copilot-introduction/copilot-internet-sales-analysis.png" alt-text="Screenshot showing Copilot suggested report page." lightbox="media/copilot-introduction/copilot-internet-sales-analysis.png":::

## Before you start using Copilot

You may need to do some clean-up work on your dataset. Read the article [Update your data model to work well with Copilot](copilot-evaluate-data.md) to see if you need to modify your semantic model so that Copilot can get insights from it.

For answers to common questions related to business data security and privacy to help your organization get started with Copilot for Fabric, see the articles in the Fabric documentation: 

- [Overview of Copilot for Fabric (preview)](/fabric/get-started/copilot-fabric-overview) 
- [Privacy, security, and responsible use for Copilot for Fabric and Power BI](/fabric/get-started/copilot-power-bi-privacy-security) 

The Copilot button in Desktop report view is always visible in the ribbon. However, to start using Copilot, you need to meet these requirements:

- You need to sign in.
- Your admin needs to enable Copilot in the tenant settings.
- You need to have member or contributor access to at least one workspace that's assigned to a paid Fabric capacity (F64 or higher) or Power BI Premium capacity (P1 or higher).

[!INCLUDE [copilot-notes](../includes/copilot-notes.md)]

## Start using Copilot

The same report creation experience is available for preview in the Power BI service and in Power BI Desktop.

- [Create reports in the Power BI service with Copilot](copilot-create-report-service.md)
- [Create reports in Power BI Desktop with Copilot](copilot-create-desktop-report.md)

If you need help with writing prompts that get you the report page you want, see [Write Copilot prompts that produce results in Power BI](copilot-prompts-report-pages.md) for guidance.

## Feature overview: Copilot capabilities

You can interact with Copilot in several different ways in Power BI. The main and most obvious way is to open the Copilot pane and ask Copilot to create a report page, or a summary of a page. 

Copilot can also create a narrative visual that summarizes a page or a whole report. 

And Copilot can generate synonyms for Q&A, to help your report readers find what they're looking for in your reports.

Here are eight examples of what Copilot can generate.

- A [summary of the underlying semantic model](#a-summary-of-the-underlying-semantic-model).
- A [summary of your report in the Copilot pane](#a-summary-of-your-report-in-the-copilot-pane).
- A [summary visual on the report itself](#a-summary-visual-on-the-report-itself).
- [Suggested content for a report](#suggest-content-for-a-report).
- A [report page](#create-a-report-page).
- A [narrative visual](#a-narrative-visual).
- [Synonyms to enhance Q&A](#synonyms-to-enhance-qa).
- [Descriptions for your semantic model measures](#descriptions-for-semantic-model-measures).
- Write [DAX queries](#write-dax-queries).

### A summary of the underlying semantic model

Summarize a Power BI semantic model with Copilot. This summary can help you gain a better understanding of data in your semantic model, identify important insights, and improve your data exploration experience. Ultimately, this can help you build more meaningful reports.

:::image type="content" source="media/copilot-introduction/copilot-summarize-model.png" alt-text="Screenshot showing the Copilot pane with Summarize the model.":::

### A summary of your report in the Copilot pane

Even if you don't have edit permission for a report, with Copilot you can generate a summary of a report page in the Copilot pane. You have the flexibility to refine or guide the summary by customizing prompts, such as "summarize this page using bullet points" or "Provide a summary of sales on this page."
 
You can also pose specific questions about the visualized data on a report page and receive a tailored response. This response includes references to specific visuals, aiding you in understanding the specific data sources contributing to each part of the answer or summary within the report.

:::image type="content" source="media/copilot-introduction/summary-skill.png" alt-text="Screenshot showing Copilot can generate a summary of your report page." lightbox="media/copilot-introduction/summary-skill.png":::

Learn more about [Copilot creating a summary response to prompts about your report](copilot-pane-summarize-content.md).

### A summary visual on the report itself

In Power BI Desktop and the Power BI service, you can use Copilot for Power BI to quickly create a narrative about a report page with just a few clicks. This narrative can summarize the entire report, specific pages, or even specific visuals that you select. See [Create a narrative with Copilot for Power BI](copilot-create-narrative.md) for details.

### Suggest content for a report

Copilot can help you get started on a new report by suggesting topics based on your data. When you select this option directly in the chat, Copilot evaluates the data and provides a report outline with suggested pages that you can explore and choose to create for you.

- A [report outline of suggested pages for your report](copilot-create-report-service.md): for example, what each page in the report is about, and how many pages it creates.  
- The visuals for the individual pages.

Select **Create** next to the first page, and Copilot creates that page for you.

### Create a report page

Copilot for Power BI can help you create a report page by identifying the tables, fields, measures, and charts for your data. If you give Copilot a high-level prompt that's specific to your data, it can generate a report page that you can then customize and modify, using the existing editing tools. It can help you get started on your report page quickly and save you a lot of time and effort in the process. Here are some examples of high-level prompts to get you started: 

- Create a page to evaluate the performance of different shifts based on good count, reject count, and alarm count over time.
- Create a page to analyze the efficiency of the production line and overall equipment effectiveness.
- Create a page to compare the cost and material of each product and their impact on production.

### A narrative visual

With Copilot, you can create a visual that generates a text summary of the data visualized in your report canvas.  The visual offers suggested prompts, and a space that allows you to direct the summary for your specific needs, offering an easy to read, useful guide for the end user. The summary updates in keeping with slicers and filters, and as the data refreshes. 

Learn more about [narrative visuals](copilot-create-narrative.md).

:::image type="content" source="media/copilot-introduction/narrative-questions-leadership.png" alt-text="Screenshot showing Narrative visual answering questions." lightbox="media/copilot-introduction/narrative-questions-leadership.png":::

### Synonyms to enhance Q&A

Copilot can write [synonyms that you can add to Q&A](../natural-language/q-and-a-copilot-enhancements.md) to improve the Q&A visual's ability to understand user questions.

:::image type="content" source="media/copilot-introduction/q-and-a-copilot-suggestions.png" alt-text="Screenshot showing Copilot can add suggestions for synonyms.":::

### Descriptions for semantic model measures

Copilot can add descriptions to your semantic model measures. People who build reports from your semantic model can see the name and description of your measures, which makes the description property essential documentation.

[Use Copilot to create measure descriptions](../transform-model/desktop-measure-copilot-descriptions.md).

### Write DAX queries

Copilot can write a DAX query. For example, you can type in a prompt to describe what DAX query you would like it to generate, and select Send or press Enter. To run what is returned, select Keep it to add it to query tab. Then select Run or press F5 to see the results of the DAX query. Read more in the article [Write DAX queries](/dax/dax-copilot).

## Start using Copilot to create reports

The same report creation experience is available for preview in the Power BI service and in Power BI Desktop.

- [Create reports in the Power BI service with Copilot](copilot-create-report-service.md)
- [Create reports in Power BI Desktop with Copilot](copilot-create-desktop-report.md)

If you need help with writing prompts that get you the report page you want, see [Write Copilot prompts that produce results in Power BI](copilot-prompts-report-pages.md) for guidance.

## Undo a page

After Copilot has generated the report, you can review the page. You have the option to start over by selecting the **Undo** button.  After you select the **Undo** button, Copilot starts over. The content on the page is removed and you start over with topic selection by either generating new topics or selecting the one from the top, when you first started.

## Copilot requirements

- Your tenant admin has to enable the Copilot setting at the tenant level. See the article [Copilot tenant settings (preview)](/fabric/admin/service-admin-portal-copilot).
- Your capacity needs to be in one of the regions listed in this article, [Fabric region availability](/fabric/admin/region-availability).
- If your tenant or capacity is outside the US or France, Copilot is disabled by default unless your Fabric tenant admin enables the [Data sent to Azure OpenAI can be processed outside your tenant's geographic region, compliance boundary, or national cloud instance](/fabric/admin/service-admin-portal-copilot) tenant setting in the Fabric Admin portal.
- Copilot in Microsoft Fabric isn't supported on trial SKUs. Only paid SKUs (F64 or higher, or P1 or higher) are supported.
- If a workspace is assigned to a capacity with Copilot enabled, a free user *can* use the **Create report page** feature.
- If a workspace isn't assigned to a capacity with Copilot enabled, a free user *can't* use the **Create report page** feature. The report must be in a workspace that is compatible with Copilot. The user sees this message:

    "Copilot isn't available in the report. The workspace where this report is saved isn't compatible with Copilot. View workspace requirements."

- In Power BI Desktop, a free user *can* use the **Create report page** feature, as long as the user is contributor, member, or admin of a workspace that is compatible with Copilot.

### Power BI service

To use the narrative visual in Copilot reports and create Copilot reports:

- The workspace has to be running on F64 or Premium capacity, for you to access Copilot for the Power BI service.
- You need either read or write access to the workspace that's on F64 or Premium capacity.
- If you have limited GPU capacity, Copilot may be throttled.

### Power BI Desktop

- You need to have write access to a workspace that is on F64 or Power BI Premium in the Power BI service, where you plan to publish the report.

## Considerations and limitations

We're continuously working to improve the quality of the report pages, including visuals and summaries generated by Copilot. Here are the current limitations. 

- Unlike the Data pane or Visualization pane, you can't resize the Copilot pane. 
- Fabric Copilot experiences in Power BI are preview experiences.  This experience is in public preview. 
- We work continuously to improve the quality of the reports (including visuals) generated by Copilot. We aim to deliver a better experience for when the product reaches general availability.
- AI may generate content that has mistakes. Make sure it's accurate and appropriate before using it.
- You can't tell Copilot which kind of visual to create.
- Copilot can't modify the visuals after it has generated them.
- Copilot can't add filters or set slicers if you specify them in the prompts. For example, if you say: "Create a sales report for the last 30 days." Copilot can't interpret 30 days as a date filter.
- Copilot can't make layout changes. For example, if you tell Copilot to resize the visuals, or to align all the visuals perfectly, it won't work.
- Copilot can't understand complex intent. For example, suppose you frame a prompt like: "Generate a report to show incidents by team, incident type, owner of the incident, and do this for only 30 days." This prompt is complex, and Copilot will probably generate irrelevant visuals.
- Copilot doesn't produce a message for the skills that it doesn't support. For example, if you ask Copilot to edit or add a slicer, it doesn't complete the instruction successfully, as mentioned above. Unfortunately, it *doesn't* give an error message either.
- Read [Update your data model to work well with Copilot](copilot-evaluate-data.md) for more tips.

## Send feedback

We always welcome your feedback about our products. Especially during public preview, your feedback helps us improve the product faster.

## Next steps

- [Update your data model to work well with Copilot](copilot-evaluate-data.md)
- [Create a report with Copilot in the Power BI service](copilot-create-report-service.md)
- [Create a report with Copilot in Power BI Desktop](copilot-create-desktop-report.md)
- [Write Copilot prompts for creating report pages in Power BI](copilot-prompts-report-pages.md)
- [Create a narrative summary visual with Copilot for Power BI](copilot-create-narrative.md)
- [Write Copilot prompts for creating narrative visuals in Power BI](copilot-prompts-narratives.md)
- [Overview of Copilot for Fabric (preview)](/fabric/get-started/copilot-fabric-overview)
- [Frequently asked questions about Copilot for Power BI and Fabric](/fabric/get-started/copilot-faq-fabric)
- [Privacy, security, and responsible use for Copilot](/fabric/get-started/copilot-privacy-security) article in the Fabric documentation 
- [Copilot tenant settings (preview)](/fabric/admin/service-admin-portal-copilot) article in the Fabric documentation 
- [Enhance Q&A with Copilot for Power BI](../natural-language/q-and-a-copilot-enhancements.md)
