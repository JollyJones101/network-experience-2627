# VPN

Elke groep voorziet VPN-toegang tot de interne beheeromgeving.

## Keuze

VPN draait bij voorkeur op OPNsense. WireGuard is aanbevolen. OpenVPN mag indien gemotiveerd.

## Verwachtingen

- VPN-type documenteren;
- adresrange documenteren;
- toegelaten routes bepalen;
- firewallregels beperken tot wat nodig is;
- gebruikers of peers beheren;
- toegang kunnen intrekken;
- risico's benoemen;
- testbewijs toevoegen.

## Minimaal testen

- Proxmox webinterface bereikbaar via VPN;
- webshare bereikbaar via VPN of juiste route;
- n8n bereikbaar indien van toepassing;
- monitoring of interne testservice bereikbaar;
- ongewenste toegang geblokkeerd.

Gebruik [templates/vpn-test-template.md](templates/vpn-test-template.md).

