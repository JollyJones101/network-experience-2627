# Platformarchitectuur

## Context

Alle groepen werken op de gedeelde Proxmox-productienode **Smith**. De opleiding beheert de fysieke host, hypervisor, storage, uplinks en globale netwerkdiensten. Een groep beheert alleen workloads binnen de toegewezen pool.

```text
Gebruikers / campus / eventueel internet
                  │
        goedgekeurde netwerkdiensten
                  │
                  ▼
          Proxmox-node Smith
        ┌─────────┼─────────┐
        ▼         ▼         ▼
     pool G1   pool G2   pool G…
      VM's      VM's      VM's
```

## Verantwoordelijkheidsgrens

| Laag | Opleiding | Studentengroep |
|---|---|---|
| Fysieke host, Proxmox en storage | beheer, capaciteit, updates | geen wijzigingsrechten |
| Bridges, VLANs, routing en perimeter | ontwerp en goedkeuring | vereisten documenteren en aanvragen |
| Proxmox-pool en ACL | toewijzen en auditen | eigen VM's beheren |
| Gast-OS | noodstop bij risico | installatie, hardening, updates |
| Applicatie en data | kaders en toezicht | volledige lifecycle |
| Back-upvoorziening | platform en beleid | eigen data selecteren en restore testen |
| DNS/reverse proxy/certificaten | gedeelde dienst of goedkeuring | aanvraag, validatie en documentatie |

## Geen impliciete infrastructuur

De exacte beschikbare VLANs, firewall, VPN, reverse proxy, DNS, back-up en identity provider worden door de docent ingevuld. Een project mag niet aannemen dat een dienst bestaat omdat die in een voorbeeldarchitectuur voorkomt.

## Productieprincipes

- één storing in een groepsproject mag andere groepen niet beïnvloeden;
- resources krijgen een maximum en worden gemeten;
- beheerinterfaces zijn niet publiek;
- netwerktoegang is standaard beperkt;
- elke tijdelijke VM heeft eigenaar, doel en verwijderdatum;
- niet-reproduceerbare data heeft een herstelpad;
- gedeelde changes zijn vooraf goedgekeurd.
