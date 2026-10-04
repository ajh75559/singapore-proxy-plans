# singapore proxy: how to get a real Singapore IP pay-as-you-go, and which plan actually fits

Search "singapore proxy" and you'll get two completely different answers in the same results page: a wall of free IP lists, and paid providers selling Singapore residential addresses. Picking between them is the whole decision, because they solve different problems.

If you just need to check how a page renders from Singapore once, a free list is fine. If the thing you're running has to stay up — an account logged in from an SG address, a scraper hitting Shopee or Lazada, an ad-verification job confirming what a Singaporean user actually sees — free lists fall apart in about ten minutes, and you'll spend the rest of the afternoon swapping IPs.

Singapore makes this worse than most countries. It's a city-state of about 5.6 million people, so the pool of genuinely Singaporean addresses is small, and a big share of what shows up on public lists is rented datacenter space in the same few racks.

## Why a free Singapore proxy list usually doesn't survive a real task

HProxy runs a public free-proxy checker and published the numbers for Singapore. At 16:51 UTC on 15 September 2026, they counted 52 live Singapore entries across all anonymity grades, 26 of them "elite". Of those 26, 24 were flagged for recent abuse and 21 were sitting on datacenter ranges — DigitalOcean, Oracle, Tencent Cloud, and similar. The median latency from their test server in Germany was 3,598 ms.

That abuse-flag number is the one that matters. Sites that care about Singapore traffic — marketplaces, local media, banks, ticketing — run IP reputation checks. An address with an abuse flag gets you a CAPTCHA at best and a block at worst, and you'll be back at the list looking for another one.

Free lists also aren't residential in the sense most people mean. They're scraped public servers. Real residential addresses are assigned by an ISP to a household, which is why they pass reputation checks that datacenter ranges don't.

> Unlimited bandwidth and 20M+ IPs sound like the same promise every provider makes. The useful question is whether the specific country you need has real ISP-assigned addresses, and how fast you can replace one that dies.

## Where 9Proxy sits in this

9Proxy is a residential proxy provider with a pool it advertises as 20M+ IPs across 90+ countries, Singapore included. It's IPv4 residential, speaks HTTP, HTTPS and SOCKS5, and lets you target by country, state/region, city and ISP — with postal-code (ZIP) filtering available in the desktop app's proxy filter. The IP-based app runs on Windows, macOS and Linux (the Linux build is CLI-driven), which matters if your Singapore jobs live on a headless box.

Two things about 9Proxy are worth knowing before you look at prices, because they change which plan makes sense:

- **IP-based plans** sell you a fixed number of IPs with unlimited bandwidth. One forwarded IP = one usage. An IP stays alive somewhere between a few hours and roughly 24 hours, and unused IPs never expire — you buy them once and burn them when you need them.
- **GB-based plans** sell traffic instead. You generate as many endpoints as you want from the dashboard, rotate or hold sticky sessions, and only the gigabytes you use are deducted. GB packages carry a 180-day validity, or unlimited validity on Enterprise.

The practical difference for Singapore work: if your job is "log into this account from the same SG address for hours", you want IP-based. If your job is "hit 4,000 SG pages and rotate every request", GB-based costs less because you're not burning a whole IP per session.

👉 See how 9Proxy's Singapore-capable residential plans are priced before you pick a model

### The two models side by side

|  | Residential by IPs | Residential by GB |
| --- | --- | --- |
| Billing unit | Number of IPs, one-time | Total GB, one-time |
| Bandwidth | Unlimited while the IP is active | Capped by purchased GB |
| Validity | IPs never expire until used | 180 days (unlimited on Enterprise) |
| Endpoints | One forwarded IP per usage | Unlimited endpoints, GB is the only limit |
| Rotation | Manual, or auto-rotation on chosen ports | Rotating or sticky by session time |
| Targeting | Country, state, city, ZIP, ISP (in app) | Country, state, city, ISP (in username) |
| Auth | Desktop app + optional proxy auth | Username/password or IP whitelist |
| App required | Yes | No, runs from the dashboard |

If you're on the GB model, targeting is built into the username string — `subaccount-country-sg-sst-15-ssid-job1`, for instance, gives you a Singapore exit held for 15 minutes under that session ID. Different `ssid` values on the same config give you parallel sticky SG IPs.

## Full 9Proxy plan list and current prices

9Proxy raised IP-based and bundle prices on 1 June 2026 and left GB pricing untouched. Everything below is the post-adjustment list, with the per-unit rate so you can compare tiers without doing division in your head. Packages are one-time purchases, not subscriptions.

### IP-based residential (unlimited bandwidth per IP)

| Package | IPs delivered | Per-IP rate | Total | Link |
| --- | --- | --- | --- | --- |
| 100 IPs | 100 | $0.24 | $24 | Get the 100 IP starter pack |
| 500 IPs | 500 | $0.144 | $72 | Buy the 500 IP pack |
| 1,000 IPs + 500 bonus | 1,500 | $0.084 | $126 | Buy 1,000 IPs with 500 free |
| 2,500 IPs | 2,500 | $0.084 | $210 | Buy the 2,500 IP pack |
| 5,000 IPs | 5,000 | $0.072 | $360 | Buy the 5,000 IP pack |
| 15,000 IPs | 15,000 | $0.048 | $720 | Buy the 15,000 IP pack |
| 25,000 IPs | 25,000 | $0.035 | $863 | Buy the 25,000 IP pack |
| 50,000 IPs | 50,000 | $0.029 | $1,438 | Buy the 50,000 IP pack |
| 100,000 IPs (Business) | 100,000 | $0.023 | $2,300 | Buy the 100,000 IP business pack |
| 200,000 IPs (Business) | 200,000 | $0.021 | $4,140 | Buy the 200,000 IP business pack |
| 500,000 IPs (Business) | 500,000 | $0.018 | $8,625 | Buy the 500,000 IP business pack |

### GB-based residential

| Package | Per-GB rate | Total | Validity | Link |
| --- | --- | --- | --- | --- |
| 5 GB | $3.00 | $15 | 180 days | Buy the 5 GB trial-size pack |
| 50 GB + 5 GB bonus | $2.10 | $105 | 180 days | Buy the 50 GB pack with 5 GB free |
| 100 GB | $1.50 | $150 | 180 days | Buy the 100 GB pack |
| 200 GB | $1.00 | $200 | 180 days | Buy the 200 GB pack |
| 1,000 GB | $0.80 | $800 | 180 days | Buy the 1,000 GB pack |
| 2,000 GB | $0.75 | $1,500 | 180 days | Buy the 2,000 GB pack |
| 3,000 GB (Enterprise) | $0.72 | $2,160 | No expiry | Upgrade to the 3,000 GB Enterprise plan |
| 6,000 GB (Enterprise) | $0.70 | $4,200 | No expiry | Upgrade to the 6,000 GB Enterprise plan |
| 10,000 GB (Enterprise) | $0.68 | $6,800 | No expiry | Upgrade to the 10,000 GB Enterprise plan |

Enterprise isn't just a bigger bucket. It adds team mode (1 owner plus up to 5 members), per-member traffic caps, full activity logs, unlimited Share Code creation and shared bandwidth inside the team that doesn't expire.

### Bundles (IPs plus traffic)

| Bundle | Contents | Price | Link |
| --- | --- | --- | --- |
| Starter | 100 IPs + 5 GB | $30 | Buy the Starter bundle |
| Popular | 1,500 IPs + 50 GB | $180 | Buy the Popular bundle |
| Pro | 5,000 IPs + 500 GB | $720 | Buy the Pro bundle |

Bundled IPs don't expire; bundled traffic follows the 180-day window. Prices move, so check the live numbers on the pricing page before committing to a large tier.

## Which plan fits an actual Singapore job

Since almost everyone searching for a Singapore proxy falls into one of a few buckets, here's the honest mapping.

**One-off geo check or a short QA pass on an SG site.** The 5 GB pack at $15 targets Singapore and rotates freely. If you're verifying a checkout flow, a currency display, or how a page looks to a Singaporean visitor, you'll probably use a fraction of it. 👉 Start with the smallest GB pack and see what your job actually burns

**Ad verification, rank tracking, or price monitoring against SG targets.** Rotating GB traffic. A 100 GB or 200 GB pack at $1.00–$1.50/GB handles regular Singapore sweeps without you babysitting IP counts. The "today list" feature reuses IPs that were live in the last 24 hours at no extra cost, which quietly shaves 20–30% off repeat jobs.

**Account work — Singapore-registered profiles, marketplace seller accounts, app sessions.** This is where IP-based plans win, because a sticky session that survives hours beats a rotating one. Start with 100 IPs at $24 and see how many you actually need per account, since the 60-second replacement policy only helps for IPs that die immediately, not ones that die after an hour.

**Agency or team running SG work for several clients.** The Popular bundle (1,500 IPs + 50 GB, $180) exists exactly for this — some jobs need stable SG addresses, others just need traffic. If you're past that, Enterprise GB with team mode avoids buying separate packages for each person.

**Reselling or running platform-level volume.** The 100,000+ IP business tiers get you to $0.023 and below per IP. There's no point looking at these until your monthly SG demand is genuinely in the tens of thousands.

One more cost lever: paying in crypto adds 5% extra IPs on top of the package. 9Proxy accepts cards, USDT, BTC, ETH, LTC, DOGE, Alipay, Apple Pay and Google Pay.

## Getting the Singapore targeting right

Singapore being a city-state changes the usual advice. Country-level targeting is essentially city-level targeting, so don't over-filter: adding a city or ISP constraint to an SG session narrows an already small pool and slows your success rate. Country + ISP is usually enough when you need a specific carrier profile.

For IP-based plans you filter in the app by country, state, city, ZIP or ISP, forward the IP to a port, and the proxy is live on `127.0.0.1:<port>`. Unused IPs sit in your balance indefinitely, so nothing is wasted if a job gets cancelled. The app also supports auto-rotation on selected ports if you want rotating behaviour without moving to the GB model.

For GB plans it's a standard username/password or IP-whitelist setup — no software on the machine, which is the reason people pick it for cloud servers and automation stacks.

👉 Check the current Singapore availability and plan options directly on 9Proxy

## What to keep in mind

Residential proxies rotate. That's the product, not a defect: an SG IP in the pool may live hours or may die in twenty minutes, and no provider fixes that. Treat "unlimited bandwidth" as unlimited data, not unlimited uptime. 9Proxy's stated replacement window covers an IP that fails within the first 60 seconds of delivery — after that, you're consuming a new one.

Independent write-ups are mixed and you should read them as such. iTWire's review called it a solid affordable option for scraping, ad verification and account management, while flagging two practical gripes: the IP-based model requires the desktop app, and free trials depend on promotions and usually have to be requested from support. That same review noted streaming services like Netflix can still detect it — so if your Singapore plan is "watch SG Netflix", a rotating residential pool is the wrong tool and this is not the article for you. A reseller page elsewhere described speeds as moderate rather than fast. And one competitor's blog references a 9Proxy outage while a reseller page notes IPs were later restored — worth knowing that even mid-size residential networks have rough patches, and worth keeping a fallback if you're dependent on one provider for a live Singapore campaign.

## FAQ

**Does 9Proxy have Singapore IPs?**
Yes — Singapore is on its country list, and targeting to Singapore works on both the IP-based app (country, city, ZIP, ISP filters) and the GB-based username string.

**Do I need a monthly subscription?**
No. Both models are one-time balance top-ups. IP-based packages don't expire until the IPs are used; GB packages carry 180 days of validity, and Enterprise GB never expires.

**What's the cheapest way to get one Singapore IP?**
The 100 IP package at $24 is the smallest IP-based tier, which works out to $0.24 per IP. If you only need a few GB of SG traffic rather than persistent addresses, the 5 GB pack at $15 is cheaper overall.

**Can I test before buying?**
9Proxy runs limited trials based on availability, and the trial tends to be granted through support rather than a self-serve button, so ask before you buy a large tier.

**Will an SG residential IP unblock Singapore streaming?**
Not reliably. Residential IPs pass reputation checks well, but streaming platforms fingerprint beyond the IP, and reviewers have reported detection on services like Netflix.

If your Singapore work needs to keep running — same address, repeatable results, no scrambling for a replacement IP — the IP-based tiers are the sane starting point, and $24 for 100 addresses with no expiry is a low-risk way to find out how many your jobs actually consume. 👉 Grab a 9Proxy plan that matches your SG workload and test it on your own targets
