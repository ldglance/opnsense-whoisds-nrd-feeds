# WhoisDS Newly Registered Domain Feeds

Public rolling blocklists generated from daily WhoisDS Newly Registered Domain (NRD) archives.

## Available feeds

| Feed | Rolling window | Raw download |
|---|---:|---|
| NRD 3-day | 3 calendar days | [feeds/nrd-3days.txt](https://raw.githubusercontent.com/ldglance/opnsense-whoisds-nrd-feeds/main/feeds/nrd-3days.txt) |
| NRD 5-day | 5 calendar days | [feeds/nrd-5days.txt](https://raw.githubusercontent.com/ldglance/opnsense-whoisds-nrd-feeds/main/feeds/nrd-5days.txt) |
| NRD 10-day | 10 calendar days | [feeds/nrd-10days.txt](https://raw.githubusercontent.com/ldglance/opnsense-whoisds-nrd-feeds/main/feeds/nrd-10days.txt) |
| NRD 15-day | 15 calendar days | [feeds/nrd-15days.txt](https://raw.githubusercontent.com/ldglance/opnsense-whoisds-nrd-feeds/main/feeds/nrd-15days.txt) |
| NRD 30-day | 30 calendar days | [feeds/nrd-30days.txt](https://raw.githubusercontent.com/ldglance/opnsense-whoisds-nrd-feeds/main/feeds/nrd-30days.txt) |

Coverage and source-date information: [feeds/metadata.json](https://raw.githubusercontent.com/ldglance/opnsense-whoisds-nrd-feeds/main/feeds/metadata.json).

## Feed format

Each line is a domain entry. Every included domain is published as both its apex and a wildcard entry (for example, `example.com` and `*.example.com`). Entries are normalized, deduplicated, and sorted.

**No local firewall TLD or suffix exclusions are applied.** These feeds preserve all valid domains in the collected source archives; each consumer can apply its own policy.

A rolling feed is generated using the archives available for its calendar window. During initial population or after missing source dates, a feed may contain fewer than its requested number of days. Check `metadata.json` for `available_days`, `missing_dates`, and `complete` before relying on a particular window.

## Source and caution

Source data: [WhoisDS Newly Registered Domains](https://www.whoisds.com/newly-registered-domains).

Newly registered domains are not automatically malicious. These lists can contain legitimate domains and may cause false positives. Review the data and test policies before using a feed to block user traffic. This repository is an independent community project and is not affiliated with or endorsed by WhoisDS or OPNsense.
