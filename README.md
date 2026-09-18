# gohighlevel conversation ai cost: what you actually pay per message, per sub-account, and when a dedicated AI setter is cheaper

Most people searching for the cost of GoHighLevel's conversation AI are trying to answer one question: *what lands on my card at the end of the month?* The unhelpful answer is "it depends." The useful answer is that there are three separate bills stacked on top of each other, and only one of them is the AI.

HighLevel's own help docs split it cleanly: the agency subscription, the AI Employee plan per location, and the phone system. Conversation AI sits in the middle layer, and that middle layer changed shape — it used to be a flat per-message charge, and it now runs on token billing unless you buy an unlimited plan. That shift is the source of most of the confusion in agency Facebook groups and on r/gohighlevel.

Here's how the numbers actually work, and where a dedicated AI setter like CloseBot starts to look cheaper than the native option.

## The three bills behind "conversation AI cost"

**1. Your HighLevel subscription.** Starter is $97/month, Unlimited is $297/month, Agency Pro is $497/month. Starter caps you at 3 sub-accounts; Unlimited and Pro remove that cap. This bill exists whether you use AI or not.

**2. The AI layer, billed per enabled location.** Three options, all documented in HighLevel's AI pricing article:

| Option | Monthly cost | Conversation AI allowance |
| --- | --- | --- |
| Pay-Per-Use | $0 (no subscription fee) | Billed at token cost |
| AI Employee Growth | $50/month per location | 1,000 agent responses, then pay-per-use rates |
| AI Employee Unlimited | $97/month per location | Unlimited, subject to fair use |

**3. Phone system charges.** These survive every AI plan. HighLevel says it plainly: unlimited Voice AI does not mean free phone service. Text and call charges are billed separately.

Two extra details that catch people out. Agent Studio is *not* included in any subscription tier — it stays pay-per-use across Pay-Per-Use, Growth, and Unlimited. And rebilling AI Employee usage to your clients requires the $497/month agency plan, so if you're on Starter or Unlimited and planned to pass AI costs through with a markup, that plan is the price of admission.

## What Conversation AI actually costs on pay-per-use

Token billing is where the "hidden costs" threads come from. HighLevel bills input tokens (customer messages, history, instructions, knowledge base content) and output tokens (the AI's replies) separately, using the model you selected.

Current published rates per 1M tokens:

| Model | Input | Output |
| --- | --- | --- |
| GPT-5 | $1.25 | $10.00 |
| GPT-5 Mini | $0.25 | $2.00 |
| GPT-4.1 | $2.00 | $8.00 |
| GPT-4.1 Mini | $0.40 | $1.60 |

HighLevel's own worked example: a conversation using 100,000 input tokens and 25,000 output tokens on GPT-5 costs **$0.375** ($0.125 input + $0.25 output).

That single number is the most useful thing on the page, because you can multiply it. If a location handles roughly 1,000 conversations a month at that size, you're looking at somewhere near $375 — which is comfortably more than the $97 unlimited plan. Run the same math on GPT-5 Mini with short replies and the per-conversation cost drops by roughly an order of magnitude, and pay-per-use becomes the cheaper choice.

That is the whole decision in one sentence: **long conversations and big knowledge bases push you to a subscription; short, repetitive chats stay cheap on tokens.**

### Where Growth and Unlimited break even

Growth at $50/month includes 1,000 agent responses. At HighLevel's example cost of $0.375 per conversation, 1,000 responses would cost about $375 on pay-per-use. Growth pays for itself well before you hit the included allowance if your conversations look anything like that example.

Unlimited at $97/month makes sense when you'd otherwise cross 1,000 responses and keep going — or when you want Voice AI bundled in. Growth includes 100 Voice AI minutes across inbound, outbound, and widget use combined; Unlimited covers Voice AI subject to fair use.

Two caveats attached to "unlimited." First, fair use is written into the terms: HighLevel reserves the right to throttle, limit, or require an upgrade if usage is deemed excessive. Second, the block-or-continue behaviour depends on the location's AI Usage Limit settings. If you set **Block AI at the limit**, usage stops at the configured ceiling. If you set **Keep AI running, just notify**, overages keep billing. Choose deliberately, because the default decides whether you get a surprise invoice.

## The part that scales badly: per-location pricing

The subscription is per enabled location. Five client accounts on Unlimited is $485/month, before phone charges and before the agency plan that lets you rebill it. Twenty accounts is $1,940/month.

CloseBot published a case study of a 102-sub-account agency where the equivalent HighLevel AI Employee Unlimited cost would have been $9,894/month. Treat that as a vendor's own example rather than neutral research — but the arithmetic is checkable: $97 × 102.

The same case study puts CloseBot's total at $809/month for that account, including $148 in message costs and roughly $255 in OpenAI token spend. That's the structural difference between the two products: HighLevel charges per location, CloseBot charges per message plus one flat platform fee regardless of how many sub-accounts you connect.

## CloseBot's plans, and what each one actually costs

CloseBot is the AI setter built to live inside a CRM rather than replace one. It connects natively to HighLevel, HubSpot, and LeadConnector, takes over the text channels in that inbox, and runs objective-based agents built with a drag-and-drop builder. It's the app I'm linking to here, so let's go through the current plans as published.

| Plan | What you get | Price | Billing | Buy |
| --- | --- | --- | --- | --- |
| Free | 100 messages/month, 1 agent, 1 user seat, 1 MB knowledge storage, unlimited account connections | $0 | Always free | [Start free with 100 messages a month](https://app.closebot.com/register?fpr=li87) |
| Core (Business) | Messages included in the base price, 15+ templates, human support, $5 per extra seat, storage add-ons, extra agents | From $64/month for the 500-message tier; $53/month equivalent on annual billing ($640/year) | Monthly or annual | [See the Business plan tiers](https://app.closebot.com/settings?tab=subscription&plan=business&toggle=monthly&fpr=li87) |
| Agency | Unlimited account connections, white-label client portal, rebill all costs, client seats, agency wallets via your own Stripe | $397/month flat, plus $0.012 per message you can mark up | Monthly | [Check the Agency plan and rebilling setup](https://app.closebot.com/settings?tab=subscription&plan=agency&toggle=monthly&fpr=li87) |
| Growth | HIPAA compliance, quarterly audits, 99.99% priority uptime, priority support, 50+ templates, custom volume | Custom quote | Custom | [Ask about Growth, SLAs and compliance](https://app.closebot.com/a?fpr=li87) |

A few honest notes on that table.

**Message volume is the dial.** The Business side of the plans page runs on a slider from 100 messages up through 500, 1K, 2K, 5K, 20K, 50K and 100K+. Message costs are baked into the price rather than metered on top, and the per-message effective rate drops as you raise the ceiling. Go over your ceiling and you pay a 2x overage rate drawn from a wallet — which is why the wallet top-up setting is worth configuring before launch, not after.

**Annual billing drops the entry price** from $64 to $53/month on the Business tier, billed as $640/year, and unlocks the larger template library.

**One disagreement in the documentation you should know about.** The plans page FAQ currently states agencies are billed a flat $0.012 per message. CloseBot's help centre article on agency plans still describes $0.006 per message. Either the help doc is stale or the rate moved. Confirm the number on the subscription screen before you build a client pricing model on it.

**There's no bring-your-own-key option.** CloseBot runs the models on its own accounts and explains this as a security decision, so your model spend is folded into what you pay them rather than billed by OpenAI or Anthropic directly. That's the opposite of the older V2 docs that told you to supply your own API keys, and it means one fewer variable in your margin math.

**No refunds.** Free plan under 100 messages a month, seven days of trial on any paid plan, then no money back. Month-to-month, cancel anytime.

## The cost comparison nobody puts on one line

Putting both products side by side for a realistic small agency — five client accounts, roughly 2,000 AI messages a month:

| Line item | HighLevel AI Employee Unlimited | CloseBot + HighLevel |
| --- | --- | --- |
| Platform | $297/month (Unlimited, needed for rebilling at cost) | $297/month (same) |
| AI layer | $97 × 5 locations = $485/month | $397/month Agency plan |
| Message/token costs | Included, subject to fair use | $0.012/message, rebillable (about $24 at 2,000 messages) |
| Model tokens | Included | Folded into the plan |
| Rough monthly total | $782 before phone charges | $718 before phone charges |

The gap is small at five accounts. It widens fast. At twenty accounts the HighLevel AI line alone is $1,940/month, while CloseBot's platform fee stays at $397 and you pay per message. That's the whole reason CloseBot leads its comparison content with per-sub-account math.

The trade-off is real in the other direction too. CloseBot doesn't do voice. HighLevel's AI Employee includes Voice AI, which CloseBot does not attempt to replace. If your offer is a phone agent that answers inbound calls, this comparison doesn't apply to you.

## What third-party reviewers and users actually say

CloseBot's own marketing claims are large: over 1 million booked appointments, around 150,000 messages a day, 99.99% uptime, and more than 1,000 agencies on the platform. Those are vendor numbers, not audited ones.

Independent material is thinner but consistent in direction. On G2, one reviewer describes CloseBot's conversation quality as "far superior to GoHighLevel's native AI," and another says that compared to HighLevel's native AI — which they describe as often returning incorrect responses and fumbling appointments — CloseBot is "a huge improvement." A third-party review published in August 2026 makes the same architectural point I'd make: CloseBot is CRM-native, so if you don't already run a CRM, you're buying two products instead of one, and roughly $97/month of that bundle goes to HighLevel Starter rather than to the AI itself.

There's also a quality-versus-price split worth stating plainly. In a comparison posted by an agency owner, the summary was that GoHighLevel wins on raw price for straightforward support-style conversations, while CloseBot handles complex sales flows and routing better. That matches the pricing shape: HighLevel sells you capacity per location, CloseBot sells you per-message usage plus a platform fee, and the two only land in the same ballpark once you're running several client accounts with real conversation volume.

## How to decide, based on the numbers rather than the demo

- **One location, straightforward conversations.** Pay-per-use with a cheaper model is genuinely the cheapest option. Watch the token bill for a month before committing to anything per-location.
- **Two or three busy locations with long sales conversations.** Growth at $50 per location usually beats token billing once you pass a few hundred substantial conversations.
- **Five or more client accounts, and you want a consistent per-client price.** The per-location AI fee is the thing that eats your margin. This is where a platform fee plus rebillable per-message cost becomes worth the extra integration work — check the CloseBot Agency plan and compare it against your actual sub-account count.
- **You sell inbound voice.** Stay on HighLevel's AI Employee. CloseBot doesn't cover it, and phone system charges apply either way.
- **You need a flat, all-in monthly number with nothing underneath it.** Neither product gives you that. Both meter something: HighLevel meters locations and tokens, CloseBot meters messages and seats.

If you want to test the second option without spending anything, the free tier is 100 messages a month with one agent and unlimited account connections — enough to build a real agent and see whether its conversation style holds up against the native option on your own leads. 👉 [Build your first agent on the free plan](https://app.closebot.com/register?fpr=li87)

## FAQ

**Is GoHighLevel's conversation AI included in the $97 subscription?**
No. The $97 is the HighLevel Starter platform fee. Conversation AI is either billed at token cost on pay-per-use, or covered by an AI Employee plan at $50/month (Growth) or $97/month (Unlimited) per enabled location.

**What does a single conversation AI message cost?**
On pay-per-use, HighLevel doesn't charge a flat per-message rate anymore — it charges for input and output tokens. Their published example works out to $0.375 for a conversation using 100,000 input and 25,000 output tokens on GPT-5. Shorter exchanges on cheaper models cost a fraction of that.

**Do Voice AI minutes still cost extra on the Unlimited plan?**
The AI portion is covered subject to fair use, but phone system charges are separate and still apply to every call. That's why an unlimited-plan location can still show phone-related charges.

**Can I rebill conversation AI costs to clients?**
HighLevel requires the $497/month agency plan to rebill AI Employee usage. CloseBot takes the opposite approach: its Agency plan is built around rebilling, with client wallets funded through your own Stripe account and markup you set yourself.

**Is CloseBot cheaper than HighLevel's conversation AI?**
It depends entirely on your sub-account count and message volume. At one or two locations, HighLevel is usually cheaper. Past four or five accounts, the per-location fee usually overtakes a flat platform fee plus per-message billing — run your own numbers with your real message volume before deciding, and confirm the current agency per-message rate in the app, since the documentation currently lists two different figures.
