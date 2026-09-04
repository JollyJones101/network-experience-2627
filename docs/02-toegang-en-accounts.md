# Toegang en accounts

## Accounts

De docent deelt de initiële toegangsmethoden mee. Noteer in jullie documentatie alleen niet-gevoelige informatie.

| Systeem | Toegang | Opmerking |
|---|---|---|
| Bestaande VPN | `<DOOR_DOCENT>` | Verplichte route voor beheer |
| OPNsense | `<DOOR_DOCENT/INDIEN_NODIG>` | Alleen binnen toegewezen beheerrechten |
| Proxmox-cluster | `<DOOR_DOCENT>` | Beperkte groepsscope |
| Reverse proxy | `<AANVRAAGPROCEDURE>` | Onboarding, geen herinstallatie |
| Bitwarden | `<GROEPSVAULT>` | Secrets buiten GitHub |

## Waar mag je inloggen?

Toegestaan:

- OPNsense van je eigen groep;
- Proxmox-nodes van je eigen groep;
- VM's en containers van je eigen groep;
- services die je zelf beheert.

Niet toegestaan:

- doos-Proxmox;
- fysieke Proxmoxcluster;
- omgevingen van andere groepen;
- netwerken buiten de opdracht.

## Secrets

Nooit in GitHub:

- wachtwoorden;
- tokens;
- private keys;
- certificaatsleutels;
- recovery codes;
- exports met secrets.

Gebruik placeholders:

```text
<SECRET_IN_BITWARDEN>
<GROUP_VAULT_ITEM>
```

## Adminacties loggen

Log betekenisvolle adminacties via:

- issue;
- commit;
- change request;
- changelog-entry;
- relevante documentatie.

Bij verloren toegang: maak een supportticket met context, impact, reeds geteste stappen en gevraagde hulp.
