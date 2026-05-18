---
description: Learn how to monitor questionnaire responses and analyse results in Dastra.
---

# Monitor questionnaires

## Response dashboard

From the **"View questionnaires"** tab, select a questionnaire template to access its response dashboard. It provides four views:

* **Responses**: list of all responses with their status (pending, published, overdue), score and linked object
* **Detailed board**: side-by-side comparison of all responses by category and score — useful for benchmarking across entities or processing activities
* **Stats**: aggregated statistics across all responses for that template
* **Details**: configuration and metadata of the questionnaire

## Individual response reporting

Opening a response gives access to a detailed reporting view:

* **Status timeline**: progression from "Waiting for respondents" → "Started" → "Pending validation" → "Published"
* **Score**: total score out of the maximum points
* **Completion**: number of questions answered out of the total
* **Response time**: how long the respondent took to complete the questionnaire
* **Red flags**: answers automatically flagged as requiring attention based on the template configuration
* **Result analysis**: automatic analysis blocks generated from the responses (compliance level, risk assessment, etc.)
* **Scoring by categories**: visualised as a radar chart or bar chart, broken down by questionnaire section

## AI analysis (beta)

From a response's reporting view, trigger an **AI analysis** to get:

* An overall compliance or risk score
* A written review summarising key findings
* A breakdown by analysis criteria (completeness, legal basis, security measures, etc.)
* Suggested tasks to address identified gaps

{% hint style="warning" %}
The AI analysis is a beta feature. Results should be interpreted with caution and reviewed by a qualified professional.
{% endhint %}

## Validating and publishing a response

Once you have reviewed a response, click **"Review and validate the questionnaire"** to move it to "Published" status. This action is available to questionnaire owners.

{% hint style="info" %}
If you cannot validate a response, check that the respondent has clicked the **"Finalize"** button. Without this step, the response remains in "Pending validation".
{% endhint %}

## Generating an action plan

From a response's reporting view, click **"Generate an action plan"** to automatically create tasks based on the answers provided. Tasks are suggested according to the template's configuration and added directly to Dastra's task management module.
