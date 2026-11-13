# VPS hosting providers: what a $2 entry plan really costs, how many sites fit on 2 GB, and which tier to buy (plan comparison plus the fees that show up after checkout)

Entry-level VPS plans from the providers compared below start between roughly $2 and $5 a month. The same market is usually quoted at $20 to $100 a month once you look at the configurations people actually run production sites on. Both figures are accurate. They describe different machines and, more often than not, different billing terms.

So the useful question isn't "who is cheapest." It's which of those two numbers you'll actually be paying in month 13, and what the plan includes at that price. Below are the billing periods behind the headline prices, RAM-to-site ratios you can size against, the fees that surface after checkout, and one risk that no uptime badge covers.

> **If you want the short version:** most readers with a handful of low-traffic sites need a 2 GB / 1 vCPU plan and nothing above it. Check the live plan list and the renewal rate before you pay, since promotional terms differ by provider and by billing cycle. 👉 [See JustHost's current VPS plans and listed prices](https://justhost.asia/?ref=196392).

## Why the same market quotes $2 and $100

PCMag puts typical VPS hosting at $20 to $100 per month, with shared hosting usually under $10 and dedicated servers at $100 and up. A separate roundup of cheap VPS plans lists entry tiers starting at $2 a month. Neither is wrong.

The $2 plans are real products: a single vCPU, 1 GB of RAM, a small SSD slice, and a bandwidth allowance that suits a test box or a low-traffic site. The $20 to $100 band describes 4 GB to 16 GB of RAM with several cores, which is what a small agency, a WooCommerce store, or a reseller actually rents.

Plan your purchase against the second number. Budgeting against the first is how people end up migrating three months in.

## Verified plan data across the market

Prices below are as published by each provider or by a roundup updated in late 2026. Currencies are mixed because the providers list them that way. No provider in this table is affiliated with this article.

| Provider | Entry configuration | Listed price and billing period | What adds cost later |
| --- | --- | --- | --- |
| Liquid Web | Cloud VPS, 1 vCPU / 2 GB / 60 GB SSD / 2 TB, from $11/mo ($0.015/hr); top CPU tier 16 vCPU / 32 GB / 400 GB / 8 TB at $392/mo | Monthly, hourly billing available | cPanel is billed separately |
| IONOS | 1–24 GB RAM, 10–640 GB SSD, unlimited traffic up to 1 Gbit/s | $2–$90/mo | Backups are a paid add-on; limited data center choice |
| Hostinger | Entry 1 vCPU / 4 GB / 50 GB NVMe | $4.99–$19.99/mo, first 24 months | Self-managed only, no Windows VPS plans |
| Hostwinds | Entry 1 CPU / 1 GB / 30 GB / 1 TB transfer, up to 96 GB RAM on top tiers | $4.99–$431.24/mo, first billing cycle | 3-day refund window; SSL not included on the base plan |
| DigitalOcean | 512 MiB–256 GiB RAM, 10 GiB–4,690 GiB SSD | $4–$2,096/mo | No refunds |
| GoDaddy | 1–4 vCPU, 2–16 GB RAM, 40–200 GB SSD | $8.99–$44.99/mo for the first three years | Refund terms vary by product |
| Hetzner Cloud | NVMe storage, AMD EPYC | From €4.35/mo | Regions in Germany, Finland, and the US |
| Netcup | 2 vCore / 2 GB / 64 GB SSD | From €3.35/mo | Popular in Europe; check region before ordering |
| Vultr | Small SSD instances upward | From $2.50/mo | Configuration-dependent pricing |

Two things to notice. First, Liquid Web's own table bottoms out at $11/mo for a 2 GB machine, while the cheapest plans in the wider market sit near $2. That gap is the difference between a managed-adjacent cloud platform and a bare unmanaged slice. Second, four of the nine rows carry a billing period in the price cell. That's the next section.

## The headline price is a billing term, not a rate

Scan the "price" column of any VPS comparison and you'll find three different things wearing the same label:

- **GoDaddy:** $8.99–$44.99/mo *for the first three years*
- **Hostinger:** $4.99–$19.99/mo *for the first 24 months*
- **Hostwinds:** $4.99–$431.24/mo *during the first billing cycle*

A first billing cycle can mean one month. Hostinger's two-year term at $4.99 works out to $119.76 for the full 24 months, and the rate you pay in month 25 is a separate number that the comparison table doesn't show. GoDaddy's quote locks a discounted rate for 36 months; after that, the listing price applies.

Do this before you pay:

1. Multiply the promotional rate by the promotional term to get the real first-term outlay.
2. Ask, in writing, what the rate is in the first month after the term ends.
3. Multiply that second rate by 12 to get your steady-state annual cost.

If a provider won't state the post-term rate in writing, treat the promotional price as a one-off and budget at the market's $20–$100 band instead. That's the number your project has to survive.

## Managed or unmanaged changes who fixes things at 2 a.m.

PCMag draws the line cleanly. With unmanaged hosting, you manage the server, perform maintenance, and handle security; the provider only hosts your data. You get full control and a lower fee, and you own every patch, firewall rule, and broken PHP upgrade. With managed hosting, the provider takes those responsibilities, you trade away some control, and the subscription is notably higher.

Hostinger's entire VPS range is self-managed. Liquid Web charges extra for cPanel on top of the plan. Neither detail appears in a headline price.

Pick unmanaged only if you can answer yes to all of these: you're comfortable on a Linux command line, you can configure a firewall and TLS, and you have a plan for patching. If any answer is no, the higher managed fee is cheaper than the outage.

## Every VPS sits on one physical server

VPS hosting runs on a single physical server partitioned into isolated virtual machines. Performance is stable until the host machine has a problem, and HostAdvice's own comparison concedes the consequence: a VPS "may experience downtime if the physical server fails." Scaling is manual too. Need more RAM, and you file an upgrade rather than watching it happen.

Cloud hosting distributes across multiple servers, scales automatically, and bills by usage. It costs more per unit and its pricing is harder to predict.

Translate that into a decision: if four hours of downtime would cost you more than the monthly hosting bill, either buy a plan with genuine failover or split across two machines. A 99.9% uptime guarantee on a single-server VPS is a promise about the network, not about the chassis.

## How much RAM for how many sites

Rough working numbers, assuming caching and a sane plugin load:

- **1–2 GB RAM / 1 core:** about 5–10 lightweight sites
- **4–8 GB RAM / 2–4 cores:** roughly 20–50 sites
- **8 GB+ with multiple cores:** 50+ sites

On traffic, the usual threshold for leaving shared hosting is around 90,000 monthly visits. Below that, a well-cached shared plan often holds up and a VPS is overhead you don't need yet. Above it, or if you need root access, custom PHP modules, or a staging environment, the move pays for itself.

Add two other triggers: you need to install software shared hosting blocks, or your traffic spikes hard enough that a noisy neighbour on a shared box would take you down.

## The fees that appear after checkout

- **Control panel licences.** cPanel on Liquid Web is an additional charge. On budget plans it can rival the plan itself.
- **Backups.** IONOS charges for them. GoDaddy bundles seven days of automated snapshots, which is not the same as off-site retention.
- **SSL.** Hostwinds' base plan doesn't include a certificate; Let's Encrypt covers most cases, but check before assuming.
- **Refund windows.** Hostwinds gives you three days. DigitalOcean gives you none. Hostinger offers a 30-day money-back guarantee. Read this line before you click buy, because it's the only exit you get.
- **Free tiers.** Kamatera's 30-day trial is worth up to $100 in cloud resources, and Mikr.us offers a permanently free 256 MB / 3 GB micro VPS. Both are fine for testing. Free plans cap CPU, storage, throughput, and support response, so production workloads still need a paid tier.

## Where JustHost fits

JustHost's plan names, RAM and CPU allotments, billing periods, and renewal rates belong in the checks above, not in a slogan. Pull up the live list, note the entry configuration against the 5–10 sites per 2 GB rule, confirm whether the price shown is monthly or an annualised figure, and check whether a control panel is included or billed separately. Five minutes on those four points tells you more than any ranking.

👉 [Check JustHost's live plan list and current pricing](https://justhost.asia/?ref=196392) before you compare it against the table above.

## FAQ

**Can a 2 GB VPS really host 5–10 sites?**
Yes, for lightweight sites with caching in place. Ten WordPress installs with heavy plugins and no page cache will exhaust 2 GB quickly. Start with the sites you have, watch memory for two weeks, and upgrade when swap usage climbs.

**Do cheap VPS plans include a control panel?**
Often not. Some providers bill cPanel separately, and on a $5 plan the licence can cost more than the server. If you don't need a GUI, a free panel or plain SSH does the job.

**How long do I have to cancel?**
It varies from three days to 30 days, and at least one major provider offers no refunds at all. Confirm the window for your specific plan, not the provider's general policy.

**When should I move off shared hosting?**
Around 90,000 monthly visits, or earlier if you need root access, custom modules, or a staging environment.

## Choosing your tier

Match the plan to what you're hosting, not to the discount:

- One site, under 20,000 visits a month, no server skills → stay on shared hosting or buy managed. A cheap unmanaged VPS will cost you more in evenings than it saves.
- 5–10 light sites, comfortable with SSH → a 2 GB / 1 vCPU plan.
- 20–50 sites or a store with real concurrency → 4–8 GB with 2–4 cores.
- Downtime measured in revenue → cloud with failover, or two smaller machines.

Before you pay, confirm three things: the data center region closest to your visitors, whether a control panel licence is included, and the exact refund window written in your order confirmation. Then check the post-promotional rate one more time. 👉 [Start with JustHost's current plans and prices](https://justhost.asia/?ref=196392).
