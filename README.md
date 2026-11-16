# Dedicated Server Pricing: What You'll Pay per Month, Whether It Doubles at Renewal, and Which Cheap Tier Is Enough

Right now, a dedicated server costs anywhere from **€4.99 a month** for a 2-core, 4 GB machine to **€1,055 a month** for a 32-core EPYC with 768 GB of DDR5. Almost everything in that range is explained by cores, memory generation, storage type and port speed. What the price tag doesn't tell you is which of three numbers you're actually looking at: the sticker price, the first-term price, or the renewal price. On some plans the difference between the first two is more than double.

Below is the current pricing across the major providers, the four places where quoted prices mislead, what "unlimited traffic" really means in the terms, and a rule for picking a tier without overbuying. Prices stay in the currency each provider quotes; nothing is converted.

> **Quick pick:** for one production site, a mid-size database, or a game server with a few dozen players, the 6-core / 32 GB NVMe class is usually the right size, and it costs roughly **€34 to €59 a month** effective once you account for commitment terms and first-year discounts. Anything at 32 cores and 128 GB or more starts around **€359 to €395 a month**. 👉 [Check Vultr's current bare metal configurations and monthly rates](https://bit.ly/VuLtr) to line its published plans up against these bands before you sign a term with anyone.

## What does a dedicated server cost per month right now?

The table below is pulled from provider pricing pages, with the exact configuration each price buys. Read the last column before the price column, because several of these rates only exist on a contract.

| Provider and plan | CPU and cores | RAM and storage | Price | Commitment and notes |
| --- | --- | --- | --- | --- |
| Scaleway Start-2-S-SSD | Intel C2350, 2C/2T, 1.7 GHz | 4 GB / 120 GB SSD | €4.99/mo | No commitment shown on the listing |
| Scaleway Start-9-M | Ryzen 5 PRO 3600, 6C/12T, 3.6 GHz | 32 GB / 2×1 TB NVMe | €33.99/mo | Requires 36-month commitment |
| Scaleway Pro-6-S | Xeon E3 1240v6, 4C/8T, 3.7 GHz | 64 GB / 2×500 GB SSD | €46.54/mo | Requires 12-month commitment |
| Namecheap Xeon E-2236 | 6C/12T, 3.4 GHz | 32 GB DDR4 ECC / 2×480 GB SSD | $37.33/mo first year (list $87.88) | 58% off first year |
| Namecheap Xeon E-2236 | 6C/12T, 3.3 GHz | 64 GB DDR4 ECC / 2×960 GB SSD | $58.79/mo first year (list $98.88) | 41% off first year |
| Contabo AMD Ryzen 12 Cores | Ryzen 9 7900, 12×3.70 GHz | 64 GB / 1 TB NVMe | €109.65/mo for first 12 months (list €149.00) | Out of stock at time of checking |
| Contabo AMD Turin 32 Cores | EPYC 9355P, 32×3.55 GHz | 128 GB / 2×1 TB NVMe | €359.10/mo for first 12 months (list €399.00) | 10 Gbit/s port optional |
| netcup RS 4000 G12.5 | EPYC 9645, 12 dedicated cores (virtualised) | 32 GB / 512 GB NVMe | €77.83/mo excl. VAT (€89.50 incl. 19%) | 12-month contract |
| HOSTKEY bm.v4-epyc-promo-10g | EPYC 9354, 32C | 192 GB DDR5 / 2×1 TB NVMe | €395/mo | 10 Gbps, 50 TB, VAT excluded |
| HOSTKEY bm.v4-epyc3 | EPYC 9354, 32C | 768 GB DDR5 / 2×3.84 TB NVMe | €1,055/mo | 1 Gbps, 50 TB, VAT excluded |

Two things jump out. First, the same core count covers a huge spread: a 6-core machine is €33.99 at the bottom and $58.79 at the top, and neither is a like-for-like comparison because one is a 3.6 GHz Zen 2 and the other an E-2236. Second, the €1,055 machine is not a "better" version of the €395 machine for most workloads. It has 768 GB of RAM because it's built for in-memory databases and heavy virtualisation, and you pay for memory you will never touch if you're hosting a web app.

## Where the price tag misleads

**A first-year discount is a loan, not a price.** Namecheap lists the 32 GB Xeon E-2236 at $37.33/mo against a list price of $87.88/mo, a 58% first-year discount. Do the arithmetic on a two-year horizon and the second year costs about **2.35 times** what the first year did: roughly $448 for year one, then about $1,055 a year from then on. Contabo runs the same pattern with a softer slope, €109.65 a month for the first 12 months against €149.00 after. Budget at the list price and treat the discount as a first-year rebate.

**Some prices only exist if you sign for years.** Scaleway's €33.99 for a 6-core, 32 GB NVMe Ryzen is tagged "with 36 months commitment" right in the price field; the same page quotes €46.54 for a 4-core/64 GB box on a 12-month commitment, and other configurations carry 36-month tags as well. Over three years that €33.99 plan is a €1,223.64 commitment. If your workload might move to a different shape in a year, a short commitment at a higher monthly rate is often cheaper than breaking a long one.

**Tax treatment changes the ranking between providers.** netcup shows €12.93 excluding VAT and €14.87 including 19% German VAT side by side for its entry plan, HOSTKEY marks its table "VAT excl.", and Contabo's displayed rate already includes applicable taxes for a 12-month subscription. Comparing a VAT-exclusive number against a VAT-inclusive one can shift a decision by a fifth. Check which basis you're looking at before you declare one provider cheaper.

**"Dedicated" doesn't always mean the whole machine.** netcup sells its root servers on a page titled dedicated servers, and states plainly in the body copy that "our root servers are not classic bare metal servers" — you get dedicated cores, RAM and storage on a virtualisation platform, not exclusive possession of the hardware. Scaleway, by contrast, describes Dedibox as a physical server reserved entirely for one user with hardware IPMI/KVM access. Both are legitimate products at their prices. They are not the same thing, and a search for dedicated server pricing will surface both.

| What the tag says | What it can mean | Question to ask |
| --- | --- | --- |
| "First 12 months" or "1st year" | Renewal returns to a much higher list price | What is the rate in month 13? |
| "With 36 months commitment" | Price is conditional on a multi-year term | What's the month-to-month rate? |
| "VAT excl." vs "incl. 19% VAT" | 15% to 25% swing in what you actually pay | Is this the number I'm invoiced? |
| "Dedicated server" | Full physical machine or dedicated slices | Do I get IPMI/KVM on the hardware? |

## What does "unlimited traffic" actually limit?

Read the fair-use clause, not the traffic number, and watch the port speed rather than the monthly volume. Contabo advertises unlimited traffic with no setup fee, then qualifies it in the footnote: incoming traffic is unmetered, but if usage is "exceptionally high or disruptive", Contabo reserves the right to throttle servers at its own discretion. HOSTKEY is more concrete, stating that servers on a 1 Gbps port "cannot use more than 70% of the allocated bandwidth for more than 3 hours a day". Scaleway takes the opposite commercial position and advertises predictable flat monthly pricing with no hidden bandwidth or egress fees.

The practical check takes two minutes. Find the fair-use paragraph and look for a percentage of port capacity and a time window, because that combination is what actually caps you. A 1 Gbps port running at 70% for three hours a day still moves tens of terabytes a month, which is plenty for most sites and nowhere near enough for a video origin or a backup target. If your workload is sustained throughput, price a 10 Gbps port and a committed traffic plan instead of trusting the word "unlimited".

## Which tier do you actually need?

Match the machine to the bottleneck, not to the biggest number in the table.

- **Serving a brochure site, a small API, or a dev environment.** Two to four cores and 4 to 16 GB is enough. The €4.99 to €20 range exists for this, and a VPS at the same price would be a reasonable substitute, so don't pay for bare metal unless you need the whole machine.
- **One production web app with a database on the same box.** Six cores and 32 GB with NVMe storage is the sweet spot. You're choosing between roughly €33.99 on a 36-month term, $37.33 in the first year at list $87.88, and €58.79 in the first year at list $98.88. Compare the renewal figures and the commitment length, not the headline.
- **Multiple services, virtualisation, CI or rendering.** You need 24 to 32 cores and 128 GB or more. This is the €289 to €399 band: netcup's RS 16000 G12.5 at €289.46 excl. VAT, Contabo's 32-core EPYC 9355P at €359.10 for the first year, HOSTKEY's 32-core EPYC 9354 with 192 GB DDR5 and a 10 Gbps port at €395.
- **In-memory databases or dense virtualisation.** Only here does a 768 GB machine at €1,055 a month make sense. If you can't name the dataset that needs to sit in RAM, this tier is not for you.

Vultr publishes its bare metal line with configurations and current rates on its own pricing page, which is the cleanest place to run this comparison against a single provider rather than stitching numbers together from five of them. 👉 [See Vultr's full bare metal plan list and current pricing](https://bit.ly/VuLtr).

## Stock and provisioning belong in your migration plan

Availability is an unadvertised cost. At the time of checking, two of the four Contabo configurations shown on its dedicated server page were marked out of stock, including the €109.65 Ryzen 12-core. Several Namecheap listings carried an "Only 1 in stock!" flag, which means the configuration you priced may not be the configuration you can order tomorrow. HOSTKEY delivers preconfigured servers immediately but quotes one day to several days for custom builds. netcup says its root servers are ready in minutes, which follows from them being virtualised.

If you're migrating a live service, order the new machine before you announce a cutover date, and keep the old one running until the new one has been through a full traffic cycle.

## FAQ

**How much more does a dedicated server cost than a VPS?**
At the entry end, not much. A 2-core, 4 GB dedicated box at €4.99 sits in the same range as a mid-size VPS. The gap opens at 32 GB of RAM and above, where dedicated hardware typically costs several times a comparably sized VPS because you're paying for the whole machine and the hardware access that comes with it.

**Why do two providers charge three times as much for the same core count?**
CPU generation, memory type, storage type, port speed and whether IPMI/KVM access is included account for most of it. A 6-core Xeon E-2236 with SATA SSDs and a 6-core Ryzen 5 PRO 3600 with NVMe are not equivalent machines, even though both are "6 cores".

**Does paying annually save money?**
It can. HOSTKEY discounts prepayment by 3% for three months, 6% for six months and 12% for twelve. Scaleway's headline prices on several plans are tied to 12 or 36-month commitments. Compare the annual total against the monthly rate times twelve, and check what happens if you cancel early.

**Is tax included in the price I see?**
Depends on the provider. netcup, HOSTKEY and Contabo each handle it differently, as shown above. Assume nothing and check the invoice basis.

**Can I cancel whenever I want?**
Check the minimum term first. Contabo's shortest initial term is one month, with subsequent terms matching the first and four weeks' notice on postpaid accounts. Scaleway's lower prices require 12 or 36 months. netcup sells on a 12-month contract with a 30-day money-back guarantee.

## Before you order

Pick by the constraint that actually binds you. If budget is the constraint and the workload is light, the €4.99 to €20 tier is genuinely sufficient and anything more is waste. If one production app with a database is the constraint, target 6 cores and 32 GB of NVMe and compare renewal prices rather than first-year ones. If virtualisation or CI is the constraint, go straight to 24 to 32 cores and 128 GB, and price the port speed alongside the CPU.

Two numbers to confirm before you enter payment details, on any provider: the rate that applies after the introductory period ends, and the minimum term you're committing to. Those two determine what you'll have paid by this time next year, and neither usually appears in the headline.

👉 [Compare Vultr's current bare metal plans, rates and billing terms](https://bit.ly/VuLtr) against the bands above, then check the same two numbers there.
