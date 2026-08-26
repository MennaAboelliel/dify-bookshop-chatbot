# Korashi Books — Dify FAQ Chatbot

A simple AI-powered FAQ chatbot for **Korashi Books**, a fictional independent bookshop in Downtown Cairo, Egypt.

The chatbot was built using **Dify Cloud Sandbox**, **OpenAI GPT-5**, and a **Knowledge Base (RAG)** containing the shop's FAQ document.

## Live Demo

**Public Dify Chatbot:**
https://udify.app/chat/hqPP0fVV8ErwpLUr

The application is publicly accessible without requiring users to log in.

---

## Project Overview

Korashi Books receives common customer questions about opening hours, location, shipping, returns, payment methods, book languages, special orders, and contact information.

The goal of this project was to build a working FAQ assistant that:

* Answers customer questions using information from the shop's FAQ.
* Provides concise and friendly responses.
* Avoids making up information.
* Politely declines questions that are outside the available knowledge base.
* Can be accessed through a public web link.

---

## Technology Stack

| Component           | Technology                |
| ------------------- | ------------------------- |
| Platform            | Dify Cloud Sandbox        |
| App Type            | Dify Chatbot              |
| LLM Provider        | OpenAI                    |
| Model               | GPT-5                     |
| Knowledge Retrieval | Dify Knowledge Base (RAG) |
| Knowledge File      | `faq.md`                  |
| Cost                | $0 / Free Tier            |

No custom code, Docker, GPU, or self-hosted infrastructure is required.

---

## Knowledge Base

The chatbot uses a single FAQ document:

**`faq.md`**

The FAQ contains 10 customer topics:

1. Opening hours
2. Store location
3. Shipping policy
4. Return policy
5. Payment methods
6. English and Arabic book availability
7. Special orders
8. Contact channels
9. Events
10. Gift cards and gift wrapping

The knowledge base is attached to the chatbot through Dify's **Context / Knowledge** configuration.

The chatbot is instructed to use the FAQ as the source of truth for factual shop information.

---

## System Prompt

The complete system prompt used by the chatbot is available in:

**`system_prompt.md`**

The prompt defines:

* The chatbot persona.
* The allowed scope.
* Grounding requirements.
* Fallback behavior.
* Response style.
* Rules against fabricating information.

The chatbot must not invent shop policies, prices, opening hours, shipping costs, or services.

---

## Example Questions

The chatbot was tested using questions such as:

### Opening Hours

**Question:**

> What time do you close on Friday?

**Expected behavior:**
The chatbot explains that Korashi Books is closed on Fridays.

### Shipping

**Question:**

> Do you ship to Alexandria?

**Expected behavior:**
The chatbot explains that Alexandria is covered by Bosta courier and that shipping costs 60 EGP with an estimated delivery time of 2–4 business days.

### Returns

**Question:**

> What's your return policy?

**Expected behavior:**
The chatbot explains the 14-day return/exchange policy and the applicable conditions.

### Language Availability

**Question:**

> Do you have books in English?

**Expected behavior:**
The chatbot explains that approximately 40% of the stock is in English and describes the available categories.

---

## Out-of-Scope / Unknown Questions

The chatbot was also tested with a question that was not covered by the FAQ:

> Can you customize a leather book cover for me?

Instead of inventing a service or price, the chatbot correctly responded that it did not have that information and directed the customer to contact Korashi Books.

This behavior satisfies the grounding and fallback requirements.

---

## Testing

The public chatbot was tested outside the Dify editor using the published web application.

Three FAQ questions were tested successfully:

* Opening hours
* Shipping to Alexandria
* Return policy

The chatbot returned correct answers based on the FAQ.

The public application was also tested with an unknown service question and correctly avoided fabricating an answer.

---

## Screenshots

The project includes screenshots documenting the chatbot setup and testing process.

```text
screenshots/
├── 01_app_setup.png
├── 02_knowledge_attached.png
├── 03_conversation_1.png
├── 04_conversation_2.png
└── 05_conversation_3.png
```

### Screenshot 01 — Chatbot Setup

Shows the Korashi Books Helper chatbot running in Dify's preview panel.

### Screenshot 02 — Knowledge Base

Shows the FAQ knowledge base attached to the chatbot.

### Screenshots 03–05 — Public Conversations

Show the published chatbot answering three FAQ questions correctly.

---

## How to Recreate

A reviewer can recreate the chatbot using the following steps:

1. Create a free account on Dify Cloud.
2. Create a new **Chatbot** application.
3. Connect an OpenAI model provider.
4. Select **GPT-5**.
5. Create a Knowledge Base.
6. Upload `faq.md`.
7. Use the default chunking/indexing settings.
8. Attach the Knowledge Base to the chatbot's Context.
9. Copy the system prompt from `system_prompt.md` into the chatbot instructions.
10. Publish the application.
11. Open the generated public web application URL.
12. Test the FAQ questions and an unknown question.

---

## Project Structure

```text
dify-bookshop-chatbot/
│
├── README.md
├── faq.md
├── system_prompt.md
│
└── screenshots/
    ├── 01_app_setup.png
    ├── 02_knowledge_attached.png
    ├── 03_conversation_1.png
    ├── 04_conversation_2.png
    └── 05_conversation_3.png
```

---

## Responsible AI & Privacy

Korashi Books is a fictional shop created for demonstration purposes.

The project does not use real customer data or private customer information.

The chatbot is designed to:

* Ground factual responses in the provided FAQ.
* Avoid hallucinating unknown shop information.
* Stay within the defined bookshop-related scope.
* Provide a clear fallback when information is unavailable.

---

## Cost

**Total project cost: $0**

The project uses:

* Dify Cloud Sandbox / free tier.
* OpenAI model access configured for the project.
* No paid infrastructure.
* No custom server.
* No GPU.
* No Docker or local installation.

---

## Project Status

**Completed**

The chatbot has been created, connected to the FAQ Knowledge Base, tested, and published as a public Dify web application.

**Live application:**
https://udify.app/chat/hqPP0fVV8ErwpLUr
