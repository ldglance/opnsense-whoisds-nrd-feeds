# WhoisDS Newly Registered Domains Feeds

Public rolling blocklists generated from daily WhoisDS Newly Registered Domains archives.

## Available feeds

| Feed | Rolling window |
|---|---:|
| nrd-3days.txt | 3 days |
| nrd-5days.txt | 5 days |
| nrd-10days.txt | 10 days |
| nrd-15days.txt | 15 days |
| nrd-30days.txt | 30 days |

## Feed location

All feeds are published under the `feeds/` directory.

## Feed behavior

- Contains all valid domains collected from WhoisDS daily archives.
- No local TLD exclusions are applied.
- Includes apex domains and wildcard subdomain entries.
- Duplicate entries are removed.
- Feed coverage depends on available daily archives.
- Coverage information is provided in `feeds/metadata.json`.

## Disclaimer

Newly registered domain feeds can contain legitimate domains.
Use appropriate caution when deploying these lists in production environments.
