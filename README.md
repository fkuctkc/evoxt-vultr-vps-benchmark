# Evoxt vs Vultr: which cheap VPS is faster per dollar, which one holds up under load, and what you actually pay each month (full plan table, overage and refund rules)

At matched prices, Evoxt's machines return better web and single-core results than Vultr's equivalents. vpsbenchmarks graded Evoxt VM-1 (1 core, 2 GB, $5.99/month) **B for web performance** against **E** for Vultr's Regular 2 GB at $10.00, and Evoxt VM-4 (4 cores, 8 GB, $23.99) **B** against **D** for Vultr High Performance 4 GB at $24.00.

Vultr's case rests on other things: 32+ data center regions, hourly billing with a monthly cap, and better stability grades in two of the three price pairs below. What follows is the full Evoxt plan list with current prices, the grade-by-grade matchups, what a month actually costs once transfer caps and billing cycles are counted, which Japan location to pick, and the workloads where Evoxt is the wrong buy.

> **Quick pick:** most people comparing these two should start with Evoxt VM-1 at $5.99/month: 1 core, 2 GB RAM, 20 GB NVMe, weekly offsite backup included, and a 14-day money-back window on new accounts. It is the cheapest plan here that runs a database-backed site without swapping. 👉 [check VM-1 pricing and deploy](https://console.evoxt.com/deploy.php?aff=1168&plan=VM-1)

## Every Evoxt plan, with prices as listed on the pricing page

| Plan | vCPU / RAM | NVMe | Transfer / month | Price / month | Order |
| --- | --- | --- | --- | --- | --- |
| VM-0.5 | 1 core / 512 MB | 5 GB | 250 GB | $2.99 | [deploy VM-0.5](https://console.evoxt.com/deploy.php?aff=1168&plan=VM-0.5) |
| VM-0.75 | 1 core / 1 GB | 10 GB | 250 GB | $4.99 | [deploy VM-0.75](https://console.evoxt.com/deploy.php?aff=1168&plan=VM-0.75) |
| VM-1 | 1 core / 2 GB | 20 GB | 500 GB | $5.99 | [deploy VM-1](https://console.evoxt.com/deploy.php?aff=1168&plan=VM-1) |
| VM-1.5 | 2 cores / 2 GB | 20 GB | 500 GB | $6.95 | [deploy VM-1.5](https://console.evoxt.com/deploy.php?aff=1168&plan=VM-1.5) |
| VM-2 | 2 cores / 4 GB | 30 GB | 1 TB | $11.99 | [deploy VM-2](https://console.evoxt.com/deploy.php?aff=1168&plan=VM-2) |
| VM-3 | 4 cores / 4 GB | 30 GB | 1 TB | $14.99 | [deploy VM-3](https://console.evoxt.com/deploy.php?aff=1168&plan=VM-3) |
| VM-4 | 4 cores / 8 GB | 60 GB | 2 TB | $23.99 | [deploy VM-4](https://console.evoxt.com/deploy.php?aff=1168&plan=VM-4) |
| VM-6 | 8 cores / 8 GB | 60 GB | 2 TB | $29.99 | [deploy VM-6](https://console.evoxt.com/deploy.php?aff=1168&plan=VM-6) |
| VM-8 | 8 cores / 16 GB | 80 GB | 3 TB | $47.99 | [deploy VM-8](https://console.evoxt.com/deploy.php?aff=1168&plan=VM-8) |
| VM-12 | 16 cores / 16 GB | 80 GB | 3 TB | $60.95 | [deploy VM-12](https://console.evoxt.com/deploy.php?aff=1168&plan=VM-12) |
| VM-16 | 16 cores / 32 GB | 100 GB | 5 TB | $95.99 | [deploy VM-16](https://console.evoxt.com/deploy.php?aff=1168&plan=VM-16) |

Three details in that table matter more than the headline prices:

**Transfer depends on the network you pick.** The pricing page shows one monthly figure per plan, and it matches the Premium-network column in third-party plan tables. On the Standard network the entry plans list roughly double (500 GB on VM-0.5, 1 TB on VM-1), and Premium Plus lists the least; Premium Plus on VM-0.5 also costs more, at $3.49. Your checkout shows the allowance for the tier you select, so read it before paying.

**Billing is monthly to triennial.** Evoxt bills monthly, quarterly, semi-annually, annually, biennially or triennially, and you can top up account credit for future invoices. There is no hourly option anywhere in the lineup.

**Every plan includes the same extras:** KVM on AMD EPYC, IPv6, VNC console access, a documented API, and automatic weekly offsite backup at no extra cost. Evoxt advertises a 99.99% uptime SLA and automated deployment that finishes in about 2.5 minutes. An extra IPv4 address is $3/month, and a paid backup plan is sold as an upgrade inside the control panel.

## The head-to-head grades, and what they do and don't tell you

vpsbenchmarks grades each plan A (best) through F. These are the three natural price pairs, using each plan's most recent trial:

| Plan (trial date) | Web perf | Raw CPU | Stability | Disk IO | Network |
| --- | --- | --- | --- | --- | --- |
| Evoxt VM-1 $5.99 (Feb 2026) | B | E | C | B | D |
| Vultr Regular 2 GB $10.00 (Jan 2026) | E | F | C | C | D |
| Evoxt VM-2 $11.99 (Aug 2026) | C | D | E | B | C |
| Vultr High Performance 2 GB $12.00 (Sep 2025) | D | F | D | D | E |
| Vultr High Frequency 2 GB $12.00 (Jul 2026) | D | F | D | C | C |
| Evoxt VM-4 $23.99 (Nov 2025) | B | B | D | B | D |
| Vultr High Performance 4 GB $24.00 (Jun 2025) | D | D | C | C | C |

Read the web and CPU rows first. Evoxt takes web performance in all three pairs and raw CPU in two of three. At $23.99, VM-4 posts B/B on web and raw CPU, which is the strongest combination on that page. Vultr's dedicated-CPU tiers at $28 and $30 graded C/E and C/E on the same two columns.

Stability runs the other way. Evoxt VM-2's E is the worst grade in the set, and VM-4's D still trails Vultr High Performance 4 GB's C. If your workload punishes restarts and jitter more than slow pages, that column should decide your purchase.

Two caveats on how much weight to give this. Each row is a single trial of a single instance, and the trial dates span from September 2025 to August 2026, so a VM tested nine months earlier competed against different neighbors on different hardware. Treat the grades as a directional signal about tiers and price points, not as a promise about the node you get.

On disk, the standardized grades and user sentiment disagree. vpsbenchmarks rates Evoxt's disk B on VM-1, VM-2 and VM-4, ahead of the Vultr plans in those pairs. A Reddit r/VPS user described Evoxt as the fastest VPS they had tested at that price while calling disk I/O its weakest point. Both can be true: fio-style sequential and mixed tests look fine, and individuals running small random reads on a busy node have a worse time.

## What the monthly bill really looks like

**Going over the transfer cap.** Vultr charges $0.01/GB on most regions, which is easy to budget for. Evoxt's policy is less clear from the outside: one third-party writeup describes throttling after the cap rather than a bill, another cites an overage rate of about $12/TB on the Premium network. Size the plan so you never test it, and confirm the policy in the console before you move real traffic onto a $2.99 box.

**Starting and stopping.** Vultr bills hourly against a monthly cap (672 hours for most compute instances), so a box you create at noon and destroy at midnight costs 12 hours. Evoxt sells by the month at minimum. If you spin up test environments weekly, that difference is worth more than the price gap.

**Longer terms.** A 12-month term has been reported at 10% off, which would put VM-1 near $65 for the year instead of $71.88 paid monthly. The discount is applied at checkout, so verify the number there rather than trusting any article, this one included.

**The exit.** New accounts get a 14-day money-back guarantee. There are scattered reports of friction when requesting it, so keep the request inside the window and in writing. That window is the cheapest way to test whether a node's disk and network behave for your workload: 👉 [start VM-1 on a monthly term](https://console.evoxt.com/deploy.php?aff=1168&plan=VM-1) and benchmark it in the first week.

## Tokyo or Osaka, and where Vultr's footprint wins

Evoxt runs 16 regions, with two in Japan. Tokyo sits on the Standard network and peers through multiple Tier-1 carriers plus BBIX. Osaka is the Premium tier, with Softbank as primary transit, which is the route budget buyers pick when traffic heads toward mainland China. Measured latency from East Asia to Tokyo lands around 50 to 80 ms, degrading toward 160 ms at Japanese evening peak; Osaka holds up better under load with a lower p95 tail, which matters more than the average for anything interactive.

Vultr covers more ground: 32+ regions including Singapore, Tokyo, Seoul, Mumbai and Sydney. If your users are in Seoul, Mumbai or Australia, Vultr's local region beats a Japan-only deployment on latency every time.

The rule that follows: users concentrated in Japan or mainland China, pick Osaka Premium and accept the tighter transfer allowance (500 GB on VM-1 instead of 1 TB). Users spread across Asia or sitting in a city Evoxt doesn't cover, pick Vultr. Bandwidth-heavy workloads with no China angle belong on Evoxt's Standard network, where the allowance is largest for the same money. 👉 [deploy an Osaka Premium VM](https://console.evoxt.com/deploy.php?aff=1168&plan=VM-1) if the China route is the reason you're here.

## When Evoxt is the wrong call

Skip it if any of these describe you:

- **You need hourly billing** for CI runners, staging environments or short-lived test boxes. Evoxt has no hourly option, full stop.
- **You need DDoS protection built in.** VPSBenchmarks' feature table lists native DDoS protection as missing for Evoxt. Anything that attracts attacks needs a third-party layer in front.
- **You need support inside four hours.** Ticket response is reported in the 4 to 8 hour range, and there is no live chat at this price tier. Fine for a hobby project or a side project with no customers; uncomfortable for anything with an SLA in front of paying users.
- **Your workload is random-read heavy.** Database servers doing lots of small reads are the case Evoxt's own users complain about, whatever the standardized disk grade says.
- **Uptime grade E bothers you.** VM-2's stability grade is the weakest number in the whole comparison, and there are isolated reports of a fresh VM with 100% packet loss and of a UK buyer invoiced for five servers after ordering one. Those are single voices, not a pattern, but they fit the risk profile of a small provider.

Also temper the marketing: Evoxt advertises up to 6.0 GHz+ per core, and that is not guaranteed on every node. Older hardware runs at 3.5 GHz and up. The single-core advantage is real at the price, but you are buying a chance at the fastest node, not a contract for one.

## Before you pay: five things to confirm

1. **Network tier at checkout.** Standard, Premium or Premium Plus changes both your transfer allowance and, on VM-0.5, the price.
2. **RAM against your stack.** 512 MB and 1 GB plans run a static site, a VPN endpoint or a tiny API. A WordPress install with plugins wants 2 GB (VM-1). MySQL plus an app plus a build process wants VM-2 or VM-4.
3. **Billing cycle.** With no hourly billing, a mistaken configuration costs at least a month. The 14-day refund covers that if you act inside it.
4. **Support expectations.** Open a ticket with a real question before migrating anything with customers on it.
5. **Backups.** Weekly offsite backup is included, but it is weekly. Keep your own copy of anything you cannot rebuild.

## The decision, in one pass

- One small site, VPN, game server or single-threaded API, users in Asia: **Evoxt VM-1 at $5.99** (VM-0.75 at $4.99 if 1 GB genuinely covers it).
- Same, but traffic is heavy and latency to China is irrelevant: **VM-1 or VM-2 on the Standard network** for the larger allowance.
- 4 cores and 8 GB with the best raw CPU score in this comparison: **VM-4 at $23.99**.
- Many regions, hourly lifecycles, dedicated-CPU tiers, or a city Evoxt doesn't cover: **Vultr**.
- 16 cores and 32 GB on a budget: **VM-16 at $95.99**, which has no direct equivalent in the price pairs above.

👉 [see all Evoxt plans and current prices](https://bit.ly/EvoXt)

## FAQ

**Can I get a refund?** New accounts have a 14-day money-back guarantee. Request it in writing inside the window; reports of friction exist but are not the norm.

**Does Evoxt take cryptocurrency?** Yes. Cards, PayPal, Bitcoin, Litecoin, Ethereum and USDT on Tron are all listed, and the Chinese-language site also mentions Alipay.

**Tokyo or Osaka for China traffic?** Osaka, on the Premium network, where Softbank is the primary transit. Tokyo's Standard network peers through Tier-1 carriers and BBIX, which suits Japan and general East Asia traffic. Osaka gives you less transfer for the same price.

**What happens if I exceed the transfer cap?** Reports conflict between throttling and a per-TB overage charge, so treat the cap as a hard ceiling and check the order form for your tier.

**Is there hourly billing?** No. The shortest cycle is one month, up to three years.
