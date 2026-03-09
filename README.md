# Balancer Recovery Dashboard

Live dashboard tracking recovered funds from the Balancer V2 Composable Stable Pool exploit on November 3, 2025.

## What it tracks

- **Whitehat Recovered Funds** ($4.67M at exploit prices) — assets rescued by external whitehats across Ethereum, Base, Polygon, and Arbitrum
- **Metastable Pools Rescue** ($4.11M) — internal rescue operation with Certora targeting CSPv5 pools on Ethereum, Optimism, and Arbitrum
- **Live % Claimed** — fetched at page load from GitHub CSVs + on-chain multisig balances
- **Live token prices** — via CoinGecko API
- **Wallet claim checker** — search if your address is eligible

## Excluded from scope

- StakeWise recovery ($21.8M osETH/osGNO) — handled separately
- Gnosis Chain frozen assets ($7.1M) — returned via hard fork
- Hypernative-paused pools ($19.4M)

## Data Sources

- On-chain DAO multisig balances (Etherscan, Arbiscan, Basescan, Polygonscan, Optimistic Etherscan)
- [BIP-892: Distribution of Rescued Funds](https://forum.balancer.fi/t/bip-892-distribution-of-rescued-funds-from-balancer-v2-november-3rd-2025-attacks/6883)
- [User shares repository](https://github.com/maxyz-xyz/balancer-upscale-exploit-shares)
- [Recovered_funds.xlsx](./Recovered_funds.xlsx) spreadsheet
- CoinGecko API for live prices

## How to deploy

This is a single `index.html` file. No build step required.

### GitHub Pages (recommended)

1. Create a new repo (or use an existing one)
2. Upload `index.html` to the repo root
3. Go to **Settings → Pages → Source → Deploy from a branch → main / root**
4. Your dashboard will be live at `https://yourusername.github.io/reponame/`

### Any static host

Just upload `index.html` to any web server — Vercel, Netlify, IPFS, or even open it locally in a browser.

## Claim your funds

Visit [balancer.fi/portfolio](https://balancer.fi/portfolio) to claim. No KYC required — just connect the wallet that held BPT at the snapshot block and sign a message.

## References

- [BIP-892](https://forum.balancer.fi/t/bip-892-distribution-of-rescued-funds-from-balancer-v2-november-3rd-2025-attacks/6883)
- [BIP-908](https://forum.balancer.fi/t/bip-908-bounty-for-information-and-recovery-of-stolen-funds/6958)
- [BIP-726: SEAL Safe Harbor](https://forum.balancer.fi/t/bip-726-adopt-the-seal-safe-harbor-agreement/6087)
- [Post-Mortem](https://medium.com/balancer-protocol/nov-3-exploit-post-mortem-51dcbeb6b020)
