# STEKLOVPN PLUS — subscription page

Static subscription page for STEKLOVPN, styled to match the official STEKLOVPN site and Proxy_sait.

## Addresses

- Main page: https://sub-steklo-plus.apruxdomain.lol/
- Main subscription URL: https://sub-steklo-plus.apruxdomain.lol/configs/okeania_auto.txt
- GitHub raw mirror: https://raw.githubusercontent.com/OceaniaVPN/Free_VPN_Sub_Free_vpn123456/main/configs/okeania_auto.txt

## Automatic sync

The workflow at .github/workflows/sync-subscription.yml checks the upstream file every 15 minutes and on manual dispatch. It validates JSON before replacing the hosted copy. If upstream data is unchanged, no commit is created.

Upstream:
https://raw.githubusercontent.com/OceaniaVPN/StekloVPN/refs/heads/main/configs/okeania_auto.txt

## GitHub Pages and DNS

1. In repository Settings → Pages, select Deploy from a branch, branch main, folder / (root), then save.
2. Set the custom domain to sub-steklo-plus.apruxdomain.lol in Pages settings.
3. At the DNS provider, add a CNAME record:
   - Name: sub-steklo-plus
   - Target: oceaniavpn.github.io
4. After GitHub verifies DNS and provisions HTTPS, enable Enforce HTTPS.

The repository root includes CNAME for the custom domain. GitHub Pages and DNS must be configured before the custom domain will serve this repository.
