# proxy price: how per-GB rates really work, where hidden costs hide, and which plan fits your traffic

Type "proxy price" into Google and you get a wall of numbers: $0.49/GB, $1/GB, $5.88/GB, "$0.018 per IP". They look comparable. Most of them aren't, because they're answering four different questions at once — what you pay per gigabyte, per IP, per month, or per successful request.

So before any plan comparison is useful, the unit has to be fixed. Here's how the pricing actually breaks down, what tends to inflate a bill after checkout, and where a provider like DataImpulse sits in that picture — including every tier it currently sells, not just the $1 headline.

## The four ways proxy providers charge you

Almost every vendor's pricing page is one of these four models wearing a different font.

- **Per GB of bandwidth.** You buy traffic and it drains as data moves through the proxy. Standard for residential and mobile pools, where the value is IP quality rather than a fixed endpoint.
- **Per IP or per port, per month.** You rent a specific address or a set number of concurrent ports. Common for datacenter and static ISP proxies, where stability matters more than volume.
- **Monthly subscription.** A recurring bundle of traffic or IPs, usually cheaper per unit at higher tiers — and usually with a minimum you pay whether you use it or not.
- **Pay-as-you-go balance.** You top up and burn it down. No recurring commitment. The model that makes sense for spiky workloads, and the one DataImpulse uses across all four of its proxy types.

The model matters as much as the rate. A $1/GB pay-as-you-go plan and a $0.80/GB subscription plan are not the same offer if you only run heavy crawls three weeks a quarter — the subscription's unused gigabytes evaporate at the end of the cycle, and you paid for them anyway.

## What each proxy type roughly costs

Fair 2026 ranges, drawn from published rates across the market:

| Proxy type | Typical billing | Rough fair range | Main cost driver |
| --- | --- | --- | --- |
| Residential | Per GB | ~$1–8/GB | Clean, ethically sourced consumer IPs |
| Datacenter | Per GB or per IP/month | ~$0.50–3/GB; a few $/IP/month | Speed and volume, weak IP reputation |
| Mobile (4G/5G) | Per GB or per IP/month | ~$2–15/GB | Carrier NAT makes these the hardest to block |
| Static ISP | Per IP/month | ~$1.50–5/IP/month | A permanent, dedicated residential-grade address |
| Managed scraper / SERP APIs | Per request | ~$0.30–12 per 1,000 requests | You're renting someone else's scraping stack |

Two things fall out of that table. First, datacenter proxies are cheap because they're abundant and easy to detect; paying residential or mobile rates for a target that doesn't check IP reputation is money thrown away. Second, the spread inside a single category is enormous — a $1/GB provider and an $8/GB provider both call themselves "residential."

## The number that actually decides your bill

Here's the part most pricing pages skip: cost per gigabyte is not cost per result.

A cheap pool with a 92% success rate costs you more per completed request than a pricier pool at 99.5%, because failed requests still burn traffic — plus the retries eat wall-clock time and engineering attention. Ban rate and latency compound the same way.

DataImpulse publishes a 99.51% success rate and rates 4.8/5 on G2. Third-party testing is more mixed but broadly consistent with a mid-tier network. An editorial review from ProxyLook put Google SERP success around 99.74%, Amazon around 98.4%, and Cloudflare-fronted targets near 93.1%, with P50 latency around 740 ms and a ban rate near 1.1%. A benchmark published by Shifter — a competitor, so weigh it accordingly — counted roughly 172,900 live IPs across five countries versus 306,400 on its own network, with median response times between 430 and 501 ms.

Read together: fine for retail, e-commerce, SERP and price-monitoring work; a step behind the premium networks on the hardest social platforms. That's the honest picture, and it's why the "$1/GB" number should be treated as a starting point for your own measurement, not a verdict.

## Hidden costs that don't show up in the $/GB figure

This is where a good-looking rate turns into a bad invoice. Watch for five things:

1. **Minimum spend.** Some enterprise vendors list attractive per-GB rates behind a $500–$1,000/month entry commitment. You're not buying a gigabyte, you're buying a contract.
2. **Traffic expiry.** If unused gigabytes reset monthly, your effective price is your *paid* price, not your *used* price. Two months of light usage can double the real cost.
3. **Targeting surcharges.** Country-level targeting is usually included. State, city, ZIP and ASN filters often aren't. On standard residential at DataImpulse, advanced filtering is billed at double the standard rate, while datacenter plans list state/city/ZIP/ASN as included features. Country targeting carries no premium.
4. **KYC and sales calls.** Some providers won't let you buy 1 GB without a business verification step. That's a real cost if you wanted to test this afternoon.
5. **Trial-pool versus paid-pool quality.** A recurring complaint in forums: the free or cheap trial performs better than the pool you're paying for. The defense is to run a small *paid* test against your own targets before scaling.

DataImpulse skirts three of those. There's no sales gate and no subscription, country targeting is in the base rate, and purchased traffic doesn't expire — buy 50 GB and use 10 this week and 40 over the next month. The minimum is $5, and there's no free tier: access starts with a paid intro pack. According to HostAdvice's review, intro plans carry a 7-day money-back guarantee for card payments provided you've used less than 80% of the traffic, and crypto purchases are non-refundable.

If you want to test the model on your own targets before committing to a volume tier, 👉 [start with DataImpulse's $5 / 5 GB intro pack here](https://bit.ly/dataimPulse) — that's the smallest legitimate entry point in the category.

## Every DataImpulse tier, including the ones nobody writes about

Four product lines, all pay-as-you-go, all with non-expiring traffic and no subscription. Prices are as published on the site.

| Plan | Proxy type | What you get | Effective rate | Billing | Purchase |
| --- | --- | --- | --- | --- | --- |
| Intro | Residential | 5 GB | $1.00/GB | Pay-as-you-go | [Get the 5 GB intro pack](https://bit.ly/dataimPulse) |
| Basic | Residential | 50 GB | $1.00/GB | Pay-as-you-go | [Buy the 50 GB residential pack](https://bit.ly/dataimPulse) |
| Advanced | Residential | 1 TB | $0.80/GB | Pay-as-you-go | [Compare residential volume tiers](https://bit.ly/dataimPulse) |
| Custom | Residential | 5 TB+ | from ~$0.70/GB | Volume agreement | [Talk to DataImpulse about 5 TB+ volume](https://bit.ly/dataimPulse) |
| Starter | Datacenter | 10 GB | $0.50/GB | Pay-as-you-go | [Buy datacenter traffic from $0.50/GB](https://bit.ly/dataimPulse) |
| Mid | Datacenter | 100 GB | $0.50/GB | Pay-as-you-go | [Take the 100 GB datacenter pack](https://bit.ly/dataimPulse) |
| Bulk | Datacenter | 1 TB | $0.45/GB | Pay-as-you-go | [Check the 1 TB datacenter tier](https://bit.ly/dataimPulse) |
| Custom | Datacenter | 5 TB+ | from $2,250 | Volume agreement | [Request a datacenter volume quote](https://bit.ly/dataimPulse) |
| Starter | Mobile | 2.5 GB | $2.00/GB | Pay-as-you-go | [Buy mobile traffic from $2/GB](https://bit.ly/dataimPulse) |
| Mid | Mobile | 25 GB | $2.00/GB | Pay-as-you-go | [Take the 25 GB mobile pack](https://bit.ly/dataimPulse) |
| Bulk | Mobile | 1 TB | $1.60/GB | Pay-as-you-go | [Check the 1 TB mobile tier](https://bit.ly/dataimPulse) |
| Custom | Mobile | 5 TB+ | from $8,000 | Volume agreement | [Request a mobile volume quote](https://bit.ly/dataimPulse) |
| Starter | Premium residential | 1 GB | $5.00/GB | Pay-as-you-go | [Try premium residential from $5](https://dataimpulse.com/premium-residential-proxies/?aff=86938) |
| Mid | Premium residential | 10 GB | $5.00/GB | Pay-as-you-go | [Check premium residential plans](https://dataimpulse.com/premium-residential-proxies/?aff=86938) |
| Custom | Premium residential | 5 TB+ | from $20,000 | Volume agreement | [Request a premium residential quote](https://bit.ly/dataimPulse) |

A few notes the table doesn't show. The 20% volume discount on mobile and premium residential only kicks in at the 1 TB+ tier — below that, those two lines are flat-rate. The default residential rate stays exactly $1.00/GB whether you buy 5 GB or 800 GB, which is unusual in a market that normally penalizes small buyers. And premium residential adds a dedicated account manager and all targeting options without surcharge.

## How that stacks up against published competitor rates

Residential entry pricing, as listed by each provider:

| Provider | Published residential rate | Model |
| --- | --- | --- |
| DataImpulse | $1.00/GB ($0.80/GB at 1 TB) | Pay-as-you-go, no minimum |
| Evomi | ~$0.49/GB | Pay-as-you-go |
| SOAX | ~$2.00/GB on a $1,600 business plan (800 GB) | Subscription |
| Oxylabs | ~$2.50/GB at the 1 TB tier | Tiered / sales |
| Decodo | ~$4.00/GB | Pay-as-you-go |
| Bright Data | ~$5.88/GB listed | Tiered, enterprise minimums |
| IPRoyal | ~$7.00/GB | Pay-as-you-go |

Evomi undercuts DataImpulse on the sticker, and reviews of it flag reliability as the trade-off — one budget-provider roundup described frequent outages and connection issues, which is exactly the cost-per-result problem described earlier. SOAX and Oxylabs look closer once you're at volume but require a larger commitment to get there. Bright Data and IPRoyal land higher on the entry tiers.

Two catches worth stating plainly. First, there's no public coupon code for DataImpulse that we could verify — the discount structure *is* the volume tier ($0.80/GB at 1 TB, ~$0.70/GB at 5 TB for residential). Treat any "exclusive code" page promising more with suspicion. Second, the numbers above move; verify on the vendor's own pricing page before you budget.

## Which tier should you actually buy?

Match the plan to your monthly traffic, not to your ambition.

**Under 5 GB a month.** The $5 intro pack. Non-expiring traffic means a light month doesn't waste the balance, so this doubles as a paid test of the pool on your real targets. 👉 [Grab the intro pack and run your own benchmark](https://bit.ly/dataimPulse).

**5–50 GB a month.** Residential Basic at $50/50 GB if your targets defend themselves; the $5/10 GB datacenter starter if they don't. Route each job to the cheapest lane where it works — paying residential rates for a target that never blocks datacenter IPs is the most common budget mistake in this category.

**50–500 GB a mon
