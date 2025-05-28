# Conversational Agent Workflow

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

