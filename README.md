# RackNerd NVMe VPS: Which Plans Are Actually NVMe, What They Cost, and Which One Fits Your Workload (Full Plan Table)

RackNerd's NVMe line is the Ryzen series. The $10–$15/year specials that circulate every Black Friday belong to a different product: Intel Xeon boxes on RAID-10 SATA SSD. If NVMe is the reason you're here, your two cheapest doors in are the 512 MB plan at **$26.99/year** and the 1.2 GB Ryzen 7950X annual special at **$18.88/year** — and if you're putting a real site on it, neither is the plan you actually want.

Below are all ten plans currently orderable on the Ryzen/NVMe side, what separates the 3900X nodes from the 7950X nodes, the per-year math nobody puts on the plan page, and the four restrictions that decide whether this host is right for you at all.

> **Quick picks.** Cheapest usable box: 512 MB at $26.99/year (VPN, DNS, monitoring, a Linux sandbox). Best value if the promo is still stocked: 1.2 GB Ryzen 7950X at $18.88/year, which is fewer dollars per year than the 512 MB. Default for WordPress or a small app: 4 GB at $24.59/month, or the 4 GB 7950X annual at $55.88 while it lasts.
>
> 👉 [Check current Ryzen NVMe plan availability and cart pricing](https://bit.ly/RacKnerd)

## Which RackNerd lineup is the NVMe one

Two product families sit side by side on the same account system, and they are not interchangeable. The standard KVM VPS runs Intel Xeon with RAID-10 SATA SSD. The Ryzen VPS line runs AMD Ryzen with pure NVMe in a RAID-protected array. RackNerd's own FAQ makes the pitch on both fronts: one Ryzen core does the work of multiple Xeon cores in most workloads, and the storage array is built to keep up with that CPU rather than bottleneck it.

That second claim is the one worth pricing out, because it's the difference between a page that renders instantly and one that pauses on every database query:

| Spec | SATA SSD | NVMe SSD | Gen4 NVMe |
| --- | --- | --- | --- |
| Sequential read | ~550 MB/s | ~3,500 MB/s | ~7,000 MB/s |
| Sequential write | ~520 MB/s | ~3,000 MB/s | ~5,500 MB/s |
| Random IOPS | ~90,000 | ~500,000 | ~1,000,000 |
| Latency | ~100 μs | ~20 μs | ~10 μs |

Manufacturer-class numbers, not a benchmark of any single RackNerd node, so treat them as the ceiling rather than a promise. Real-world results land lower; more on that in the benchmark section.

## RackNerd NVMe VPS plans and prices

The full Ryzen Linux NVMe lineup, seven plans, all with a real 1 Gbps port, one dedicated IPv4, full root access and the SolusVM-based control panel:

| Plan | vCPU | NVMe | Bandwidth | Price & term | Order |
| --- | --- | --- | --- | --- | --- |
| 512 MB | 1 vCore | 10 GB | 500 GB | **$26.99/year** (annual only) | [512 MB annual plan](https://my.racknerd.com/aff.php?aff=11397&pid=500) |
| 1 GB | 1 vCore | 15 GB | 1 TB | $17.99/month | [1 GB plan](https://my.racknerd.com/aff.php?aff=11397&pid=501) |
| 2 GB | 2 vCores | 20 GB | 2 TB | $20.59/month | [2 GB plan](https://my.racknerd.com/aff.php?aff=11397&pid=502) |
| 4 GB | 2 vCores | 30 GB | 3 TB | $24.59/month | [4 GB plan](https://my.racknerd.com/aff.php?aff=11397&pid=503) |
| 6 GB | 3 vCores | 45 GB | 4 TB | $27.59/month | [6 GB plan](https://my.racknerd.com/aff.php?aff=11397&pid=504) |
| 8 GB | 3 vCores | 75 GB | 5 TB | $36.59/month | [8 GB plan](https://my.racknerd.com/aff.php?aff=11397&pid=505) |
| 12 GB | 4 vCores | 90 GB | 6 TB | $55.99/month | [12 GB plan](https://my.racknerd.com/aff.php?aff=11397&pid=506) |

Only the 512 MB tier is annual-only. The other six can be billed monthly, quarterly, semi-annually or annually, and longer cycles lock the rate for the term.

Separately, RackNerd published three Ryzen 7950X annual specials with DDR5 memory and Gen4 NVMe. These come from the official announcement, which states plainly that if the order link still works, the promotion is still live:

| Plan | vCPU | Gen4 NVMe | Bandwidth | Price & term | Order |
| --- | --- | --- | --- | --- | --- |
| 1.2 GB | 1 vCore | 25 GB | 2,500 GB | **$18.88/year** | [1.2 GB 7950X annual](https://my.racknerd.com/aff.php?aff=11397&pid=830) |
| 2.5 GB | 2 vCores | 38 GB | 4,000 GB | $32.98/year | [2.5 GB 7950X annual](https://my.racknerd.com/aff.php?aff=11397&pid=831) |
| 4 GB | 2 vCores | 65 GB | 6,000 GB | $55.88/year | [4 GB 7950X annual](https://my.racknerd.com/aff.php?aff=11397&pid=832) |

Two things to keep in mind. First, the standard page on RackNerd's site currently serves FAQ content rather than a live price table, so the numbers above are what the order pages show, and the cart total is the only figure that binds. Second, annual specials are stock-limited and rotate by datacenter; a plan showing as orderable today can vanish from your preferred location next week.

## Ryzen 3900X vs 7950X: what you can and can't choose

Both processors appear in the Ryzen lineup. The 7950X machines pair DDR5 memory with PCIe Gen4 NVMe; the 3900X machines run DDR4. RackNerd's promotional material describes the two coexisting rather than the newer chip replacing the older one, and the company's own announcement confirms 7950X nodes in San Jose specifically.

You don't get to pick. The node your order lands on decides, and that isn't exposed in the cart. What you can do is read the plan description on the order page, which names the processor on the 7950X specials.

Does the gap matter for a small site? The 7950X wins on single-thread clock speed, and single-thread speed is what makes a WordPress admin panel or a Node service feel responsive — a PHP-FPM pool of 4–8 workers is bound by how fast each worker finishes, not by how many cores the host has. For a Minecraft server or a Discord bot, same story. For a static site behind a CDN, either chip is fine and you should buy on price.

## What a year actually costs

Per-month list prices hide the biggest spread in this lineup.

The 512 MB annual plan works out to **$2.25/month equivalent**. The 1.2 GB 7950X special works out to **$1.57/month** — cheaper per year than the smaller plan, with 2.4× the RAM, 2.5× the storage and five times the bandwidth. If that special is in stock at checkout, the 512 MB plan only makes sense for someone who needs it in a datacenter where the promo isn't offered.

The bigger spread is between the monthly and annual 4 GB options. The standard 4 GB plan at $24.59/month costs **$295 over a year**. The 4 GB 7950X annual special is **$55.88 for the same twelve months**, with 65 GB of Gen4 storage instead of 30 GB and DDR5 instead of DDR4. That's roughly two months of the monthly plan for a full year of a better-specified machine. The catch is that the annual plan is a promotion with limited stock, while the monthly plan is simply the standing catalog price.

👉 [Order the 4 GB Ryzen 7950X annual plan at $55.88/year](https://my.racknerd.com/aff.php?aff=11397&pid=832)

And the one that changes how you should buy: **RackNerd does not offer refunds or a money-back guarantee.** That's stated in their knowledgebase, not buried. Prepaying a year on an eight-core plan you've never logged into is the expensive way to find out the network path to your users is mediocre. Test on the cheapest plan that proves the point, then move up.

## Picking a plan by what you're running

**512 MB / $26.99 per year.** A WireGuard endpoint, a secondary DNS server, an uptime probe, a jump box, a place to learn Linux. RackNerd's own guides warn against WordPress on this tier and they're right — you'll spend the year fighting the OOM killer. It's also the cheapest possible way to verify the NVMe claims yourself before trusting anyone's review, including this one.

**1 GB vs 2 GB.** The difference is the second vCore, not the RAM. One core handles a low-traffic site; a second core is what keeps requests from queuing when a cron job or a backup runs alongside normal traffic. $17.99 to $20.59 buys you that.

**2 GB to 4 GB.** A $4/month step that doubles RAM and adds 10 GB of storage. This is the plan most people running a WordPress site, a small Rails or Django app, or a Docker host with three or four containers should land on.

**6 GB and up.** The 6 GB adds a third vCore and 45 GB, which matters once you're running a busy database next to the app. The 8 GB tier's 75 GB of storage is the point where you stop checking `df -h` weekly. The 12 GB plan is for consolidating several small workloads onto one box.

None of these are for sustained CPU-heavy compute. If you're rendering video or running long batch jobs, a shared vCore slice is the wrong purchase at any price.

## Limits you find out after ordering

**No control panel.** This is raw Linux with root. No cPanel, no Plesk, no managed WordPress. If you want a panel, install a free one yourself or budget for a license elsewhere.

**Ticket support only, 24/7.** No live chat. Fine for "my node isn't booting," less fine if you want someone to debug your Nginx config.

**Upgrades go one direction.** You can move up a tier at any time; it takes about a minute of downtime for the reboot. Downgrading means cancelling and buying the smaller plan fresh.

**Provisioning is genuinely instant.** Credentials, IP and control panel login arrive by email within minutes. Reinstalling a different distribution later is a few clicks in the panel.

**IPv6 is available on request.** RackNerd's FAQ confirms up to 100 free IPv6 addresses in Los Angeles DC-02 via support ticket after ordering.

**Datacenter choice matters more than the plan.** Ryzen NVMe stock appears across Los Angeles, San Jose, Seattle, Dallas, Chicago, Utah, New York, New Jersey, Ashburn, Atlanta, Amsterdam and Strasbourg, but not every plan is in every location. Pick the location closest to your users, not to you: Los Angeles or San Jose for Asian traffic, Amsterdam or Strasbourg for Europe, New York or Ashburn for the US East Coast.

👉 [Start with the $26.99/year 512 MB plan and test the network before committing](https://my.racknerd.com/aff.php?aff=11397&pid=500)

## Independent performance numbers

VPSBenchmarks ran a full trial on RackNerd's Ryzen 2 vCore / 4 GB plan in December 2025. Their results: **Web Performance grade B**, **Disk I/O grade C**, provisioning in **1 minute 50 seconds**, and the hardware confirmed as an AMD Ryzen 9 7950X at 4.5 GHz on the newer Los Angeles/San Jose nodes.

Read that honestly. Grade B on web serving means response times are solid for application hosting. Grade C on disk I/O means the NVMe doesn't hit marketing peak in a shared slice — which is normal for virtualized storage, and the reason the earlier spec table should be read as a ceiling. Both grades together describe a box that's quick at serving pages and merely adequate at hammering the disk. If your workload is a page cache and a database that fits in RAM, that profile is fine. If it's continuous large writes, look at dedicated hardware.

## FAQ

**Can I run Windows on these plans?** No. Windows is a separate product line on the Ryzen NVMe backbone, listed from $27.59/month with the license included. The Linux Ryzen plans ship Linux images only.

**Is the $18.88/year plan still available?** RackNerd's announcement says the promotion is live as long as the order link works. If the cart loads the plan with that price, it's available; if it errors or shows a different total, it's gone for that location.

**Can I change the OS later?** Yes, any time, from the control panel, including switching distributions.

**Can I get more IPv6 addresses?** In Los Angeles DC-02, up to 100 free, via a ticket after your order.

**Which datacenter should I pick?** The one nearest your audience. Los Angeles DC-02 is the safe default if you're unsure — it's the IPv6-enabled location and has the better path to Asia.

**How do I pay?** Card, PayPal, Alipay, and cryptocurrency.

## How to decide

Match the plan to the job and stop there:

- A VPN endpoint, DNS resolver, monitor or learning box → **512 MB at $26.99/year**.
- One small site with light traffic → **2 GB at $20.59/month**, or the **1.2 GB 7950X at $18.88/year** if it's stocked where you need it.
- WordPress, a small app, or a Docker host → **4 GB**: $24.59/month, or **$55.88/year** on the 7950X special while it exists.
- A database next to the app, or several containers → **6 GB and up**.

Before you check out, confirm two things: the datacenter dropdown has your location for that specific plan, and the annual total in the cart matches what you expected. There's no refund waiting on the other side if it doesn't.

👉 [See the current RackNerd Ryzen NVMe plans and cart prices](https://bit.ly/RacKnerd)
