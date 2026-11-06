# Horizon 32HL733H — MB110 Titanium firmware update

Documentație și arhiva firmware folosită pentru repararea afișării Netflix pe un Horizon 32HL733H. Test efectuat pe 5 noiembrie 2026: actualizare de la **V.2.21.19.0** la **V.2.35.36.0**, urmată de confirmarea versiunii și test Netflix reușit.

**[Descarcă firmware-ul din Releases](https://github.com/sorinnuta/horizon-32hl733h-mb110-update/releases/tag/v2.35.36.0)**

## Configurația testată

| Componentă | Identificare |
| --- | --- |
| TV | Horizon 32HL733H |
| Platformă | MB110 |
| UI Name | titanium |
| Mboot inițial | MB110-048 |
| Build inițial | 2016-11-14 11:46:20 |
| Profil panou | `315_VESWNDLN14_2D_WXG_D_N_F0_V_110_221127_217762` |
| PQ | `PQTool_MB110R2_OEM_WXGA_202484` |

Modelul comercial singur nu stabilește compatibilitatea. Pachetul nu este prezentat ca update universal pentru Horizon, MB97, MB110S sau alte interfețe. O instalare nepotrivită ori întreruperea alimentării poate bloca televizorul. Nu avem o validare independentă a semnăturii producătorului sau a tuturor componentelor actualizate.

## Conținutul release-ului

- `17MB110.titaniumV.2.35.36.0.zip`: arhiva originală, cu numele normalizat pentru descărcare, fără modificarea conținutului.
- `SHA256SUMS`: amprenta arhivei și a binarului din interior.

ZIP-ul conține numai `upgrade_mb110.bin`. Hash-urile sunt și în [SHA256SUMS](SHA256SUMS). Verificarea SHA-256 confirmă identitatea fișierului, nu compatibilitatea cu aparatul sau autenticitatea producătorului.

```bash
sha256sum 17MB110.titaniumV.2.35.36.0.zip
```

Instalarea folosită a fost prin **MENU → 1505**, cu binarul dezarhivat în rădăcina unui stick FAT32. Înainte de încercare, identifică placa și interfața din meniul service și salvează configurația originală. Exporturile de profiluri/PQ/identitate prin USB nu sunt un backup integral al bootloaderului și sistemului. Nu întrerupe alimentarea și nu scoate USB-ul în timpul actualizării.

## Proveniență

Pachet descărcat de proprietarul televizorului din [postarea #6 a tehnicianului yokoono51 pe Elektroda](https://www.elektroda.pl/rtvforum/topic4114275.html#21497427). Acolo este publicat drept `17MB110 titaniumV.2.35.36.0.zip` (107.61 MB), pentru MB110 Titanium. Publicarea originală privește un alt model de televizor; rezultatul pe Horizon este documentat aici separat.

Firmware-ul este material terț și nu este creat de autorul acestui repository. Nu a fost identificată în arhivă o licență de redistribuire și nu i se atribuie aici o licență nouă. Acest proiect nu este afiliat Horizon, Vestel sau Netflix. Pentru o problemă de atribuire ori o solicitare a titularului drepturilor, poate fi deschis un issue.

Nu sunt publicate exporturile aparatului: credențiale, HDCP, adrese MAC, profiluri originale sau alte date de identitate.
