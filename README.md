# Korashi Books — Dify FAQ Chatbot

A simple AI-powered FAQ chatbot for **Korashi Books**, a fictional independent bookshop in Downtown Cairo, Egypt.

The chatbot was built using **Dify Cloud Sandbox**, **OpenAI GPT-5**, and a **Knowledge Base (RAG)** containing the shop's FAQ.

---

## Live Demo

**Public Dify Chatbot:**
https://udify.app/chat/hqPP0fVV8ErwpLUr

The application is publicly accessible through the Dify web app.

---

## Project Overview

Korashi Books is a small independent bookshop specializing in English and Arabic fiction, poetry, and local history titles.

The chatbot is designed to answer common customer questions that would normally be received through Instagram and WhatsApp, including questions about opening hours, location, shipping, returns, payment methods, book languages, special orders, events, gift cards, and contact information.

The main goal is to provide a simple, reliable FAQ assistant that answers from a controlled knowledge base instead of inventing shop information.

---

## Objectives

This project demonstrates how to build and publish a working AI FAQ chatbot without custom application code.

The chatbot:

* Uses a Dify Chatbot application.
* Uses a Knowledge Base containing the shop FAQ.
* Uses OpenAI GPT-5 as the language model.
* Provides concise and friendly customer-service responses.
* Grounds factual answers in the FAQ.
* Avoids fabricating unknown information.
* Provides a fallback when the requested information is not available.
* Is published as a public web application.

---

## Technology Stack

| Component           | Technology                |
| ------------------- | ------------------------- |
| Platform            | Dify Cloud Sandbox        |
| Application Type    | Chatbot                   |
| LLM Provider        | OpenAI                    |
| Model               | GPT-5                     |
| Knowledge Retrieval | Dify Knowledge Base / RAG |
| Knowledge File      | `faq.md`                  |
| Cost                | $0                        |

No custom backend, Python code, Docker, GPU, or self-hosted infrastructure is used.

---

# Knowledge Base

The chatbot uses the following knowledge-base document:

**`faq.md`**

The FAQ contains 10 topics:

1. Opening hours
2. Store location
3. Shipping policy
4. Return policy
5. Payment methods
6. English and Arabic book availability
7. Special orders
8. Contact channels
9. Events
10. Gift wrapping and gift cards

The FAQ was uploaded to Dify as a Knowledge Base and connected to the chatbot through its Context / Knowledge configuration.

The chatbot is instructed to use the FAQ as the source of truth for factual information about the shop.

---

# Full FAQ

## Korashi Books — Frequently Asked Questions

Korashi Books is a small independent bookshop in Cairo, Egypt, specializing in English and Arabic fiction, poetry, and local history titles. This document answers the questions our customers ask us most often on Instagram and WhatsApp.

### 1. What are your opening hours?

We're open Saturday to Thursday, 10:00 AM – 9:00 PM. We're closed on Fridays. During Ramadan, hours shift to 8:00 PM – 1:00 AM to accommodate evening shoppers — we'll post updated hours on our Instagram each year.

### 2. Where are you located?

We're on 26th of July Street, Downtown Cairo, two minutes' walk from Tahrir Square metro station. Look for the green awning with the owl logo.

### 3. Do you ship outside Cairo?

Yes. We ship anywhere in Egypt via Bosta courier:

* Cairo & Giza: 1–2 business days, flat fee of 40 EGP.
* Alexandria, Delta cities: 2–4 business days, flat fee of 60 EGP.
* Upper Egypt & Red Sea governorates: 3–6 business days, flat fee of 80 EGP.

We currently do not ship internationally, but we're working on it.

### 4. What is your return policy?

You can return or exchange any book within 14 days of purchase, as long as it's unused and in its original condition.

Bring your receipt (a photo of your order confirmation is fine).

Refunds are issued to the original payment method within 5 business days.

Sale items are final and cannot be returned.

### 5. What payment methods do you accept?

**In-store:** cash, Visa/Mastercard, and Meeza cards.

**Online/delivery orders:** cash on delivery, InstaPay, or Vodafone Cash.

We do not currently accept international cards for online orders.

### 6. Do you have books in English?

Yes — about 40% of our stock is in English, covering fiction, poetry, and non-fiction.

We also carry Arabic literature, translated classics, and a small children's book section in both languages.

### 7. Can you special-order a book you don't have in stock?

Absolutely.

Message us the title and author on Instagram or WhatsApp and we'll check availability with our suppliers.

Special orders usually arrive within 7–10 business days and require a 50% deposit, which is fully refundable if the book doesn't arrive within 3 weeks.

### 8. How can I contact you?

* **Instagram:** @korashibooks — fastest response, usually within a few hours
* **WhatsApp:** +20 100 000 0000
* **Email:** [hello@korashibooks.example](mailto:hello@korashibooks.example)
* **In person:** 26th of July Street, Downtown Cairo, during opening hours

### 9. Do you host any events?

Yes, we hold a monthly poetry reading night on the last Thursday of each month, and occasional author signings — announced on our Instagram a week in advance.

Entry is free; seating is first-come, first-served.

### 10. Do you offer gift wrapping or gift cards?

We offer free gift wrapping in-store on request.

Gift cards are available in-store only, in denominations of 100, 200, and 500 EGP, and never expire.

This FAQ reflects the policies of Korashi Books, a fictional independent bookshop created for demonstration purposes.

---

# Full System Prompt

The following system prompt is used by the Korashi Books Helper chatbot:

> **System Prompt — Korashi Books Helper**
>
> You are the Korashi Books Helper, a friendly customer service assistant for Korashi Books, a small independent bookshop in Downtown Cairo, Egypt.
>
> ## Persona
>
> Warm, concise, and helpful — like a knowledgeable staff member texting a customer back on Instagram or WhatsApp.
>
> Keep answers short (2–4 sentences) unless the customer asks for detail.
>
> You may use a light, friendly tone and the occasional relevant emoji (📚, 🚚), but don't overdo it.
>
> ## Scope
>
> Only answer questions about Korashi Books: opening hours, location, shipping, returns, payment methods, book stock/languages, special orders, events, gift cards, and how to contact the shop.
>
> Base every factual answer strictly on the information provided in the knowledge base (the shop's FAQ). Do not use outside/general knowledge to answer questions about the shop's policies, hours, prices, or services.
>
> If a customer asks something unrelated to the bookshop (e.g. general trivia, coding help, other businesses), politely explain that you can only help with questions about Korashi Books.
>
> ## Fallback rule
>
> If the answer is not contained in the knowledge base, say so honestly. Do not guess, estimate, or invent details (no made-up prices, hours, or policies).
>
> In that case, respond with something like:
>
> "I don't have that information on hand — please reach out to us directly on Instagram (@korashibooks) or WhatsApp (+20 100 000 0000) and we'll help you out!"
>
> ## Style rules
>
> Never fabricate shipping costs, return windows, hours, or contact details that aren't in the knowledge base.
>
> If a question is ambiguous, ask a brief clarifying question rather than guessing.

---

# Example Questions and Expected Answers

## Opening Hours

**Question:**

> What time do you close on Friday?

**Expected answer:**

Korashi Books is closed on Fridays.

---

## Shipping

**Question:**

> Do you ship to Alexandria?

**Expected answer:**

Yes. Alexandria is covered by Bosta courier, with a flat shipping fee of 60 EGP and an estimated delivery time of 2–4 business days.

---

## Return Policy

**Question:**

> What's your return policy?

**Expected answer:**

Books can be returned or exchanged within 14 days if unused and in their original condition. Refunds are issued to the original payment method within 5 business days, while sale items are final sale.

---

## English Books

**Question:**

> Do you have books in English?

**Expected answer:**

Yes. About 40% of the shop's stock is in English, including fiction, poetry, and non-fiction.

---

# Grounding and Fallback Test

The chatbot was tested with a question that is not covered by the FAQ:

> Can you customize a leather book cover for me?

The chatbot did not invent a service or price. Instead, it explained that the information was not available and directed the customer to contact the shop.

This demonstrates the required fallback behavior:

* No fabricated information.
* No invented prices.
* No invented policies.
* Clear escalation to the shop's contact channels.

---

# Public Application Testing

The published Dify web application was tested outside the Dify editor.

Three FAQ questions were tested successfully:

1. **What time do you close on Friday?**
2. **Do you ship to Alexandria?**
3. **What's your return policy?**

The chatbot returned answers consistent with the information contained in the FAQ.

An additional unknown question about custom leather book covers was tested and the chatbot correctly declined to guess.

---

# Screenshots

The repository contains screenshots documenting the application setup, knowledge-base configuration, and public chatbot testing.

```text
screenshots/
├── 01_app_setup.png
├── 02_knowledge_attached.png
├── 03_conversation_1.png
├── 04_conversation_2.png
└── 05_conversation_3.png
```

### `01_app_setup.png`

Shows the Korashi Books Helper chatbot running in Dify's preview panel.

### `02_knowledge_attached.png`

Shows the FAQ Knowledge Base connected to the chatbot.

### `03_conversation_1.png`

Shows the public chatbot answering the opening-hours question.

### `04_conversation_2.png`

Shows the public chatbot answering the shipping question.

### `05_conversation_3.png`

Shows the public chatbot answering the return-policy question.

---

# How to Recreate the Chatbot

A reviewer can recreate the chatbot using the following process:

1. Create a free account on Dify Cloud.
2. Create a new **Chatbot** application.
3. Connect the OpenAI model provider.
4. Select **GPT-5**.
5. Create a new Knowledge Base.
6. Upload `faq.md`.
7. Accept the default chunking/indexing settings.
8. Wait for the Knowledge Base indexing to finish.
9. Attach the Knowledge Base to the chatbot Context.
10. Copy the system prompt from `system_prompt.md` into the chatbot instructions.
11. Save and publish the chatbot.
12. Open the generated public web application URL.
13. Test the FAQ questions.
14. Test an unknown question to confirm the fallback behavior.

---

# Project Structure

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

# Privacy and Responsible AI

Korashi Books is a fictional independent bookshop created for demonstration purposes.

No real customer information or private personal data is used in this project.

The chatbot is designed to:

* Ground factual responses in the provided FAQ.
* Avoid hallucinating unknown shop information.
* Stay within the defined bookshop-related scope.
* Clearly state when information is unavailable.
* Direct customers to the shop's contact channels when necessary.

---

# Cost

**Total project cost: $0**

The project uses the Dify Cloud Sandbox and a configured OpenAI model provider without paid infrastructure or custom hosting.

No GPU, Docker, custom server, or local installation is required.

---

# Acceptance Criteria

| Requirement                        | Status     |
| ---------------------------------- | ---------- |
| Dify Chatbot created               | ✅ Complete |
| OpenAI model connected             | ✅ Complete |
| FAQ Knowledge Base created         | ✅ Complete |
| 8+ FAQ topics included             | ✅ Complete |
| Knowledge Base attached to chatbot | ✅ Complete |
| System prompt configured           | ✅ Complete |
| Public web app published           | ✅ Complete |
| Public URL available               | ✅ Complete |
| 3 FAQ questions tested             | ✅ Complete |
| Unknown question fallback tested   | ✅ Complete |
| GitHub documentation               | ✅ Complete |
| Screenshots included               | ✅ Complete |
| No custom code required            | ✅ Complete |
| Fictional/public-safe shop data    | ✅ Complete |

---

# Final Result

The Korashi Books Helper is a working public FAQ chatbot built with Dify Cloud, OpenAI GPT-5, and a controlled FAQ Knowledge Base.

**Live application:**
https://udify.app/chat/hqPP0fVV8ErwpLUr

**Repository:**
https://github.com/MennaAboelliel/dify-bookshop-chatbot
