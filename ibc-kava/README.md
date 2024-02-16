# CryptoCrew IBC-KAVA

## Channel List

| Source Chain         | Source Channel   | Source Port        | Destination Chain     | Destination Channel   | Destination Port    | CC Relayer    |
|----------------------|------------------|--------------------|-----------------------|-----------------------|---------------------|---------------|
| `kava_2222-10`     | `channel-0`      | `transfer`         | `cosmoshub-4`       | `channel-277`         | `transfer`          |     ✅      |
| `kava_2222-10`     | `channel-1`      | `transfer`         | `osmosis-1`         | `channel-143`         | `transfer`          |     ✅      |
| `kava_2222-10`     | `channel-5`      | `transfer`         | `akashnet-2`        | `channel-37`          | `transfer`          |     ✅      |
| `kava_2222-10`     | `channel-82`     | `transfer`         | `exchain-66`        | `channel-45`          | `transfer`          |             |
| `kava_2222-10`     | `channel-87`     | `transfer`         | `canto_7700-1`      | `channel-13`          | `transfer`          |     ✅      |
| `kava_2222-10`     | `channel-116`    | `transfer`         | `kaiyo-1`           | `channel-95`          | `transfer`          |     ✅      |
| `kava_2222-10`     | `channel-117`    | `transfer`         | `evmos_9001-2`      | `channel-83`          | `transfer`          |     ✅      |
| `kava_2222-10`     | `channel-119`    | `transfer`         | `umee-1`            | `channel-98`          | `transfer`          |             |
| `kava_2222-10`     | `channel-120`    | `transfer`         | `migaloo-1`         | `channel-48`          | `transfer`          |     ✅      |
| `kava_2222-10`     | `channel-122`    | `transfer`         | `injective-1`       | `channel-143`         | `transfer`          |     ✅      |
| `kava_2222-10`     | `channel-124`    | `transfer`         | `xstaxy-1`          | `channel-7`           | `transfer`          |             |
| `kava_2222-10`     | `channel-128`    | `transfer`         | `ixo-5`             | `channel-25`          | `transfer`          |             |
| `kava_2222-10`     | `channel-129`    | `transfer`         | `phoenix-1`         | `channel-216`         | `transfer`          |     ✅      |
| `kava_2222-10`     | `channel-132`    | `transfer`         | `pacific-1`         | `channel-18`          | `transfer`          |     ✅      |
| `kava_2222-10`     | `channel-133`    | `transfer`         | `agoric-3`          | `channel-63`          | `transfer`          |     ✅      |
| `kava_2222-10`     | `channel-134`    | `transfer`         | `core-1`            | `channel-129`         | `transfer`          | `ibc-persistence` |
| `kava_2222-10`     | `channel-135`    | `transfer`         | `haqq_11235-1`      | `channel-6`           | `transfer`          |             |
| `kava_2222-10`     | `channel-136`    | `transfer`         | `neutron-1`         | `channel-36`          | `transfer`          | `ibc-neutron` |
| `kava_2222-10`     | `channel-137`    | `transfer`         | `dydx-mainnet-1`    | `channel-7`           | `transfer`          |     ✅      |
| `kava_2222-10`     | `channel-139`    | `transfer`         | `noble-1`           | `channel-37`          | `transfer`          |     ✅      |
| `kava_2222-10`     | `channel-140`    | `transfer`         | `celestia`          | `channel-13`          | `transfer`          |     ✅      |
| `kava_2222-10`     | `channel-142`    | `transfer`         | `coreum-mainnet-1`  | `channel-18`          | `transfer`          |             |
| `kava_2222-10`     | `channel-144`    | `transfer`         | `dymension_1100-1`  | `channel-3`           | `transfer`          | `ibc-dymension` |

Total active counterparty chains: 14

## Relayer Accounts
- `kava_2222-10`
```
kava - kava18hx3fcqrvynx9vvpvyv5qym82xz4suw5vn80f8
```
- `osmosis-1`
```
kava - osmo18hx3fcqrvynx9vvpvyv5qym82xz4suw5caqzfj
```
- `akashnet-2`
```
kava - akash18hx3fcqrvynx9vvpvyv5qym82xz4suw5aa74x6
```
- `agoric-3`
```
kava - agoric18hx3fcqrvynx9vvpvyv5qym82xz4suw5zm3d0k
```
- `cosmoshub-4`
```
kava - cosmos18hx3fcqrvynx9vvpvyv5qym82xz4suw5sxnjlq
```
- `evmos_9001-2`
```
kava - evmos1qz5humuak45aj67hmy4at5hykfsvc8453dxyl7
```
- `kaiyo-1`
```
kava - kujira18hx3fcqrvynx9vvpvyv5qym82xz4suw5pw32j2
```
- `phoenix-1`
```
kava - terra18hx3fcqrvynx9vvpvyv5qym82xz4suw5kzfjaq
```
- `canto_7700-1`
```
kava - canto1qz5humuak45aj67hmy4at5hykfsvc845p6k637
```
- `migaloo-1`
```
kava - migaloo18hx3fcqrvynx9vvpvyv5qym82xz4suw5aj6g2w
```
- `injective-1`
```
kava - inj10hvldghaqvsedplt3utxffs34ylss5w8chwgfp
```
- `pacific-1`
```
kava - sei1yvejj22t78s2vfk7slty2d7fs5lkc8rn78qyra
```
- `dydx-mainnet-1`
```
kava - dydx18hx3fcqrvynx9vvpvyv5qym82xz4suw5elaklh
```
- `noble-1`
```
kava - noble18hx3fcqrvynx9vvpvyv5qym82xz4suw5c9x68w
```
- `celestia`
```
kava - celestia18hx3fcqrvynx9vvpvyv5qym82xz4suw5pvzz9d
```

## Chain Registry PRs
- [Add ibc injective-kava](https://github.com/cosmos/chain-registry/pull/2558)
- [Add ibc cronos-kava](https://github.com/cosmos/chain-registry/pull/2668)
- [Add Kava USDt to assetlists](https://github.com/cosmos/chain-registry/pull/2712)
- [Add ibc kava-sei](https://github.com/cosmos/chain-registry/pull/2921)
