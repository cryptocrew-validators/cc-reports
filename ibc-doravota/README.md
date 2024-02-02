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

## Client substitution

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

- chain_id: `dydx-mainnet-1`
- subject_client: `07-tendermint-15`
- substitute_client: `07-tendermint-19`
```
18c18
<             height: 2581229,
---
>             height: 2600022,
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


### Clients in `active` status:

- chain_id: `injective-1`
- subject_client: `07-tendermint-245`
- substitute_client: `07-tendermint-251`

```
18c18
<             height: 2581229,
---
>             height: 2599734,
```

- chain_id: `akashnet-2`
- subject_client: `07-tendermint-183`
- substitute_client: `07-tendermint-185`

```
18c18
<             height: 2581229,
---
>             height: 2600041
```

- chain_id: `archway-1`
- subject_client: `07-tendermint-34`
- substitute_client: `07-tendermint-72`

```
18c18
<             height: 358086,
---
>             height: 2600089,
```

- chain_id: `pirin-1`
- subject_client: `07-tendermint-14`
- substitute_client: `07-tendermint-15`

```
18c18
<             height: 2581229,
---
>             height: 2600104,
```

- chain_id: `coreum-mainnet-1`
- subject_client: `07-tendermint-12`
- substitute_client: `07-tendermint-42`

```
18c18
<             height: 2581229,
---
>             height: 2600118,
```

- chain_id: `pacific-1`
- subject_client: `07-tendermint-109`
- substitute_client: `07-tendermint-110`

```
18c18
<             height: 2581229,
---
>             height: 2600182,
```

### Proposal

Proposal Title:  
"Substitute IBC light client for doravota"  

Proposal Text:  
"After a hard fork of the doravota chain `vota-ash`, related to a recently discovered issue in [Cosmos-SDK v0.47](https://github.com/cosmos/cosmos-sdk/issues/19321), all IBC lights on counterparty chains have frozen. During the hard fork, only 4 empty blocks were removed and no transactions were invalidated.  

This proposal substitutes the previously used IBC light client for doravota. The passing of this proposal is necessary to unblock IBC channels between the two chains that rely on the subject client."  

Vote text:  
Hi, we're CryptoCrew, and we're behind this proposal. After a recent hard-fork of the DoraFactory chain "doravota", we are assisting the team in restoring IBC functionality with the cosmoshub and other counterparty chains.  

Due to the time-sensitive nature of the process, this proposal was not drafted on the Cosmoshub forum beforehand. Every IBC client-update proposal can be fully verified by validating the proposed client state against a live RPC.  

Please note that during the hard fork state migration on doravota, only 4 empty blocks were removed and no transactions were invalidated. The following difference in the reference is therefore expected.  

> subject client id: 07-tendermint-1191 - last revision: 0 height: 2581229  
host: DD1EBAA0B48F7BDED90919E0910A2A237E1637C163E7C9143204C6F5356F29E0  
reference: 2AF290F2245BD4AD39C72F191E45A26A959E4FB3710D9AA4FBFDECA8136A664D  
<<< substit client id: 07-tendermint-1204 - last revision: 0 height: 2597996  
host: E2197CB826519A6117ED72BD8084AACF0D461DD8A742FC63EFAF56DB5AF7CCA3  
reference: E2197CB826519A6117ED72BD8084AACF0D461DD8A742FC63EFAF56DB5AF7CCA3  
❌ subject client NOT VALID!  
✅ substitute client valid!
----------------------------------  

### Live on-chain proposals

- cosmoshub proposal: https://www.mintscan.io/cosmos/proposals/877
- osmosis proposal: https://www.mintscan.io/osmosis/proposals/722
