# racknerd cheap vps: current KVM deals from $11.29/year, how to pick the right plan, and the renewal and refund rules worth knowing first

RackNerd's cheapest KVM VPS is $11.29/year right now — 1 GB RAM, 1 vCPU, 24 GB SSD storage, 2 TB of monthly transfer, and a dedicated IPv4 address. That works out to about 94 cents a month, and unlike most intro pricing in hosting, it renews at the same promotional rate instead of jumping several times higher in year two.

The trade-offs are real: everything is unmanaged, support is ticket-only, and promotional annual plans can't be refunded. None of that matters if you're comfortable running your own server. This guide covers every plan currently on the table, what the specs actually get you in day-to-day use, and a few checkout rules you'll want to know before paying.

> **If you just want the answer:** the **1 GB plan at $11.29/year** handles VPNs, DNS resolvers, bots, uptime monitors, and small sites fine. If you're running Docker containers or a small database, step up to the **3.5 GB plan at $32.49/year** — 2 cores, 65 GB SSD, and 7 TB of transfer make it the best value in the lineup. 👉 [Check RackNerd's current cheap VPS deals](https://bit.ly/my-rn)

## What RackNerd's cheap VPS deals cost right now

Five KVM plans make up the current holiday promotion, running from $11.29 to $59.99 per year. RackNerd rotates these deals around holidays and sells them primarily through deal links, so treat the order page as the source of truth for the live price — but the tiers below have been stable across the current sale cycle.

| Plan | RAM / vCPU | SSD | Monthly transfer | Price | Order |
| --- | --- | --- | --- | --- | --- |
| 1 GB KVM | 1 GB / 1 core | 24 GB | 2 TB | **$11.29/yr** | [ Order the 1 GB plan](https://my.racknerd.com/cart.php?a=add&pid=903&aff=16470) |
| 2 GB KVM | 2 GB / 1 core | 40 GB | 3.5 TB | **$18.29/yr** | [ Order the 2 GB plan](https://my.racknerd.com/cart.php?a=add&pid=904&aff=16470) |
| 3.5 GB KVM | 3.5 GB / 2 cores | 65 GB | 7 TB | **$32.49/yr** | [ Order the 3.5 GB plan](https://my.racknerd.com/cart.php?a=add&pid=905&aff=16470) |
| 4 GB KVM | 4 GB / 3 cores | 105 GB | 9 TB | **$43.88/yr** | [ Order the 4 GB plan](https://my.racknerd.com/cart.php?a=add&pid=906&aff=16470) |
| 6 GB KVM | 6 GB / 4 cores | 140 GB | 12 TB | **$59.99/yr** | [ Order the 6 GB plan](https://my.racknerd.com/cart.php?a=add&pid=907&aff=16470) |

Every plan in the table includes the same baseline: KVM virtualization, RAID-10 SSD storage, a 1 Gbps network port, one dedicated IPv4, full root access, DDoS protection, a free Clientexec license, and near-instant deployment through a SolusVM control panel.

One thing that confuses first-time buyers: the entry plan on RackNerd's main website is a 512 MB KVM server at $26.99/year. That's more than double the price of the 1 GB deal above, with half the RAM. The main-site lineup exists mostly for people who want month-to-month billing:

| Plan | RAM / vCPU | SSD | Transfer | Price | Order |
| --- | --- | --- | --- | --- | --- |
| 512 MB KVM | 512 MB / 1 core | 30 GB | 500 GB | $26.99/yr | [ Order the 512 MB plan](https://my.racknerd.com/cart.php?a=add&pid=1&aff=16470) |
| 1 GB KVM | 1 GB / 2 cores | 50 GB | 1 TB | $17.99/mo | [ Order the 1 GB monthly plan](https://my.racknerd.com/cart.php?a=add&pid=20&aff=16470) |
| 2 GB KVM | 2 GB / 3 cores | 75 GB | 2 TB | $20.59/mo | [ Order the 2 GB monthly plan](https://my.racknerd.com/cart.php?a=add&pid=21&aff=16470) |
| 4 GB KVM | 4 GB / 4 cores | 130 GB | 3 TB | $24.59/mo | [ Order the 4 GB monthly plan](https://my.racknerd.com/cart.php?a=add&pid=22&aff=16470) |
| 6 GB KVM | 6 GB / 5 cores | 170 GB | 4 TB | $27.59/mo | [ Order the 6 GB monthly plan](https://my.racknerd.com/cart.php?a=add&pid=23&aff=16470) |
| 8 GB KVM | 8 GB / 6 cores | 220 GB | 5 TB | $36.59/mo | [ Order the 8 GB monthly plan](https://my.racknerd.com/cart.php?a=add&pid=24&aff=16470) |

As a rule: if annual billing works for you, ignore the main-site list prices entirely. The deals live in the promotional tiers.

## Are $11-a-year servers actually usable?

Yes — for light workloads. The reason matters: RackNerd uses full KVM virtualization on every plan, so you get a genuinely isolated environment where your allocated RAM is yours, and you can run Docker, custom kernels, or mount a custom ISO. Plenty of budget hosts cut costs with OpenVZ containers, which share the host kernel and block most of that. RackNerd hasn't.

Independent testing of a 2 GB Los Angeles plan over six months recorded 99.95% uptime, a 198 ms time-to-first-byte, around 420 MB/s sequential disk speed, and roughly 940 Mbps of real throughput on the gigabit port. For a server costing under $20 a year, those numbers are respectable.

The caveat is CPU. These are shared-core nodes packed for economics, so a noisy neighbor can affect you under load, and sustained heavy CPU consumption runs against the spirit — and sometimes the letter — of the acceptable use policy. A VPN endpoint, DNS resolver, cron jobs, or a small website fits fine. A video encoding box doesn't.

Also keep your own backups. Promo plans are non-refundable, so if a disk dies or you misconfigure something, recovery is on you.

## The renewal math, and why RackNerd breaks the usual pattern

Promotional plans renew at the same promotional price you originally paid. This is the single most important thing to understand about RackNerd's pricing, because the rest of the budget hosting industry works the opposite way: cheap first year, expensive renewal.

Over three years, the 1 GB plan costs $33.87 total. The 3.5 GB plan costs $97.47 total, or about $2.71 a month. There's no second-year trap to model because the rate is locked.

Here's how the 2 GB tier compares against the big clouds:

| Provider | 2 GB plan price | Annual cost | vCPU | SSD | Transfer |
| --- | --- | --- | --- | --- | --- |
| RackNerd (promo) | $18.29/year | $18.29 | 1 | 40 GB | 3.5 TB |
| DigitalOcean | $18/mo | $216 | 1 | 50 GB | 3 TB |
| Vultr | $15/mo | $180 | 1 | 50 GB | 3 TB |
| Linode (Akamai) | $14/mo | $168 | 1 | 50 GB | 2 TB |

The gap is roughly ten times. To be fair about what that money buys elsewhere: DigitalOcean, Vultr, and Linode offer hourly billing, managed databases, load balancers, block storage, and polished APIs. If you need any of those platform features, they're worth paying for. If you just need a server with root access, the difference is hard to ignore — a comparable spec on DigitalOcean runs about $72 a year against RackNerd's $11.29.

## The fine print to check before you order

A few rules that don't show up in the marketing but should shape how you buy:

1. **Promotional annual plans are non-refundable.** RackNerd offers a 99.9% uptime SLA, but if you change your mind a week in, the money stays. Decide before you click.
2. **Flash deals sell out.** The best pricing tends to appear around holidays, and popular tiers sell out quickly. Once purchased, the plan stays available and renews at the locked rate.
3. **Promo codes exist, but only one works per order.** Codes like MYPHPNOTES (30% off VPS orders) and WIN-30OFF (30% off Windows VPS) have circulated recently, and 15OFFDEDI takes 15% off dedicated servers. On annual KVM billing, the sale price is usually already better than what a code gets you — codes matter most for monthly billing, Windows, and bare metal. Verify the code at checkout before assuming anything.
4. **IPv6 is free if you ask.** Up to 100 IPv6 addresses are available at the Los Angeles and France (Strasbourg) locations — open a support ticket after ordering.
5. **OS reinstall is self-service.** Through SolusVM you can reinstall to a different Linux distribution anytime without a ticket. Upgrading to a higher plan works too, with a brief reboot.
6. **No migration help, no hand-holding.** Support is ticket-based and runs 24/7, with reported response times ranging from under half an hour to a day. Simple issues get fixed fast; OS-level problems are yours.

If that list reads fine to you, the current deals are live: 👉 [lock in the 1 GB plan at $11.29/year](https://my.racknerd.com/cart.php?a=add&pid=903&aff=16470)

## Where should your VPS live?

You choose the datacenter at order time, and it's worth 30 seconds of thought because you can't easily change it later. RackNerd operates roughly 20 locations across North America, Europe, and Asia — Los Angeles (two facilities), San Jose, Seattle, Dallas, Chicago, Atlanta, Ashburn, New York, Toronto, Amsterdam, London, Frankfurt, Singapore, and more.

The short version: pick the location closest to your users. Los Angeles DC-02 and San Jose are the popular picks for US West Coast, and the Los Angeles Asia-optimized option or Singapore work well if you're serving users in Asia. Amsterdam, London, or Frankfurt make sense for European audiences. All locations run on the same 1 Gbps port standard.

## Who shouldn't buy a RackNerd cheap VPS

Being honest about the fit saves everyone time:

- **You need managed hosting, cPanel, or automatic updates.** RackNerd does none of this. If you want someone else to patch the server, look at managed hosts.
- **You need block storage, S3-compatible object storage, load balancers, or managed databases.** The big clouds sell these; RackNerd sells raw servers.
- **You're running mission-critical production for a business.** The uptime record is good and the 99.9% SLA exists, but there's no phone line and no dedicated support team for emergencies.
- **You need premium network routes into China.** BandwagonHost specializes in CN2 GIA routes; RackNerd runs standard routing.
- **Your workload needs sustained heavy CPU.** RackNerd does bare metal if you need it — an Intel Xeon E3-1240 v3 with 32 GB RAM starts at $64.95/month, up to a dual Xeon with 256 GB RAM at $209/month, all with unmetered 1 Gbps.
- **You need Windows.** It's available as a separate product line (AMD Ryzen 3900X with NVMe storage, full RDP access), just with its own pricing.

## RackNerd cheap VPS FAQ

**Is an $11/year VPS actually usable?**
Yes, for light workloads. VPNs, DNS resolvers, bots, monitoring probes, staging environments, and small websites all run comfortably on the 1 GB plan. Don't expect dedicated-core performance, and keep backups since budget plans are non-refundable.

**Does the promo price go up at renewal?**
No. RackNerd's promotional annual plans renew at the same promotional price you paid, which is unusual for the budget hosting market and the main reason the deals hold their value long-term.

**Can I get a refund if I change my mind?**
Not on promotional annual plans. Monthly standard plans offer more flexibility if you're unsure about the commitment.

**Is RackNerd a legitimate company?**
Yes. It was founded in 2019 by industry veteran Dustin B. Cisneros, is headquartered in Los Angeles, operates its own infrastructure across roughly 20 locations, has been named to the Inc. 5000, and has been a fixture of the LowEndBox deal ecosystem since launch.

**Do promo codes stack with sale prices?**
No — only one code works per order, and the annual holiday sale pricing on KVM plans is typically the better deal. Codes deliver the most value on monthly billing, Windows VPS, and dedicated servers.

## Picking your plan

- VPN, DNS resolver, bot, or uptime monitor → the **1 GB plan at $11.29/year** is enough
- Staging server or validating a side project → the **2 GB plan at $18.29/year**
- Docker plus a small database plus a website → the **3.5 GB plan at $32.49/year**, the sweet spot in the lineup — 👉 [order the 3.5 GB plan here](https://my.racknerd.com/cart.php?a=add&pid=905&aff=16470)
- Several services on one box → the **6 GB plan at $59.99/year**
- You refuse annual billing → the standard monthly lineup above

Before you check out, do three things: pick the datacenter closest to your users, set up an off-site backup routine (RackNerd gives you the tools, not the policy), and confirm the live price on the order page since these deals rotate. If all that lines up, 👉 [browse all of RackNerd's current VPS deals](https://bit.ly/my-rn) and grab the tier that matches your workload.
