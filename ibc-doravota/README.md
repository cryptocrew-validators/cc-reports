# IBC-DORAVOTA

## Relayer Accounts
| address                                   | chain     | 24.01.2024 | denom |
|-------------------------------------------|-----------|------------|-------|
| osmo1t59rf5hjnf5erlgnkk24gj8a43lp9djclujs5d | osmosis   | 200        | OSMO  |
| cosmos1t59rf5hjnf5erlgnkk24gj8a43lp9djch8pqzl | cosmoshub | 50         | ATOM  |
| nolus1t59rf5hjnf5erlgnkk24gj8a43lp9djcph3lq6 | nolus     | 500        | NLS   |
| akash1t59rf5hjnf5erlgnkk24gj8a43lp9djc6uv8m9  | akash     | 100        | AKT   |
| inj1kdn77tjqntzf8r2szvjn62t8787jthzx6zcq7d  | inective  | 15         | INJ   |
| archway1t59rf5hjnf5erlgnkk24gj8a43lp9djczvaygg | archway   | 250        | ARCH  |
| sei1t59rf5hjnf5erlgnkk24gj8a43lp9djc6tsky7   | sei       | 300        | SEI   |
| dydx1t59rf5hjnf5erlgnkk24gj8a43lp9djc770yzg  | dydx      | 200        | USDC  |
| core1t59rf5hjnf5erlgnkk24gj8a43lp9djcyfem9y  | coreum    | 110        | CORE  |

## Action items:
- [x] Create substitution clients after vota-ash hardfork on osmosis and cosmoshub
- [ ] Create client update proposals on osmosis and cosmoshub

### Client substitution

- chain_id: `osmosis-1`
- subject_client: `07-tendermint-2959`
- substitute_client: `07-tendermint-3083`
```
18c18
<             height: 2581229,
---
>             height: 2596982,
90,95c90
<         frozen_height: Some(
<             Height {
<                 revision: 0,
<                 height: 1,
<             },
<         ),
---
>         frozen_height: None,
```

- chain_id: `cosmoshub-4`
- subject_client: `07-tendermint-1191`
- substitute_client: `07-tendermint-1204`
```
18c18
<             height: 2581229,
---
>             height: 2597075,
90,95c90
<         frozen_height: Some(
<             Height {
<                 revision: 0,
<                 height: 1,
<             },
<         ),
---
>         frozen_height: None,
```

Proposal Title:  
"Substitute IBC light client for doravota"  

Proposal Text:  
"After a hard fork of the doravota chain `vota-ash`, related to a recently discovered issue in [Cosmos-SDK v0.47](https://github.com/cosmos/cosmos-sdk/issues/19321), all IBC lights on counterparty chains have frozen. During the hard fork, only 4 empty blocks were removed and no transactions were invalidated.  

This proposal substitutes the previously used IBC light client for doravota. The passing of this proposal is necessary to unblock IBC channels between the two chains that rely on the subject client."
