# Conversational Agent Workflow

<<<<<<< HEAD
This document describes how the n8n workflow uses a dedicated AI agent to gather requirements, produce WordPress content, and manage customer feedback.

1. **Lead Capture** – Customers fill out a form or call a voice line that hits the `Incoming Webhook` node.
2. **Transcription** – Voice audio is sent to the `Speech To Text` node, which returns a transcript.
3. **Requirement Summary** – The transcript is passed to the `Summarize Requirements` node (OpenAI) to extract key points and generate clarifying questions.
4. **Staging Site** – The workflow then creates a staging site on WP Engine via API.
5. **Content Generation** – AI generates page copy and image prompts.
6. **Upload** – Generated content is posted to the WordPress site.
7. **Notification** – The customer receives an email with the staging URL for review.
8. **Feedback Loop** – Further feedback can be submitted to the same webhook, repeating the process until approval.

Customize this flow by adding additional nodes—for example, Stripe payment collection, PDF proposal generation, or ongoing maintenance checks.

=======
This document describes the n8n workflow that automates the end‑to‑end creation of a WordPress site using WP Engine. Customers interact with a dedicated AI agent for requirements gathering and feedback.

1. **Lead Capture** – Customers submit a form or leave a voice message that triggers the `Incoming Webhook` node.
2. **Transcription** – Audio is sent through the `Speech To Text` node to obtain a transcript.
3. **Requirement Summary** – The transcript is summarized by the `Summarize Requirements` node (OpenAI) and clarifying questions are generated.
4. **Project Plan** – An additional `Generate Project Plan` node produces a milestone outline and cost estimate which is emailed to the customer via the `Send Proposal` node.
5. **Approval & Payment** – The workflow waits for customer approval, then creates a Stripe checkout session for the initial deposit.
6. **Staging Site** – After payment the `Create Staging Site` node provisions a new environment on WP Engine.
7. **AI Content Generation** – The `Generate Content` node creates copy and image prompts which are uploaded with the `Upload to WordPress` node.
8. **Prototype Review** – An email notification provides the staging URL. The workflow waits for feedback which is summarized by the `Summarize Feedback` node and applied via `Update WordPress`.
9. **Final Invoice & Deployment** – Once the customer is satisfied a final Stripe invoice is generated. The site is deployed to production and the customer receives a final notification.

Import the workflow from `workflows/automated-agency-v2.json` in n8n to experiment with this automated process. Adjust the nodes and prompts to suit your specific services and style.
>>>>>>> 0tbjbg-codex/design-ai-powered-automated-creative-agency-workflow
