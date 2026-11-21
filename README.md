# STEKLOVPN PLUS — subscription page

Static subscription page for STEKLOVPN, styled to match the official STEKLOVPN site and Proxy_sait.

## Addresses

- Main page: https://sub-steklo-pluse.apruxdomain.shop/
- Main subscription URL: https://sub-steklo-pluse.apruxdomain.shop/configs/okeania_auto.txt
- GitHub raw mirror: https://raw.githubusercontent.com/OceaniaVPN/Free_VPN_Sub_Free_vpn123456/main/configs/okeania_auto.txt

## Automatic synchronization

The workflow at .github/workflows/sync-subscription.yml runs every 15 minutes and on manual dispatch. It:
- Downloads and validates the JSON subscription from the StekloVPN source repository.
- Reads `data-season` from the official STEKLOVPN page source (`STEKLOVPN-Site/public/index.html`) and publishes it as `season.json`.
- Publishes the feed and season.json to this repository only when values change.

The page reads season.json; it does not calculate the season from the visitor's device date.

## GitHub Pages and DNS

1. In repository Settings → Pages, select Deploy from a branch, branch main, folder / (root), then save.
2. Set the custom domain to sub-steklo-pluse.apruxdomain.shop in the Pages settings.
3. At the DNS provider, add a CNAME record:
   - Name: sub-steklo-pluse
   - Target: oceaniavpn.github.io
4. After GitHub verifies DNS and provisions HTTPS, enable Enforce HTTPS.

The repository root includes CNAME for the custom domain. GitHub Pages and DNS must be configured before the custom domain will serve this repository.
