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

## Expired client state:
host_chain: `vota-ash`
reference_chain: `archway-1`
client_id: `07-tendermint-10`
```
ERROR ThreadId(66) send_messages_and_wait_commit{chain=vota-ash tracking_id=ft-transfer}:send_tx_with_account_sequence_retry{chain=vota-ash account.sequence=4}:estimate_gas: failed to simulate tx. propagating error to caller: gRPC call `send_tx_simulate` failed with status: status: Unknown, message: "failed to execute message; message index: 0: cannot send packet using client (07-tendermint-10) with status Expired: client state is not active [cosmos/ibc-go/v7@v7.3.0/modules/core/04-channel/keeper/packet.go:75] With gas wanted: '18446744073709551615' and gas used: '75896' ", details: [], metadata: MetadataMap { headers: {"content-type": "application/grpc", "x-cosmos-block-height": "2465374"} }
ERROR ThreadId(66) send_messages_and_wait_commit{chain=vota-ash tracking_id=ft-transfer}:send_tx_with_account_sequence_retry{chain=vota-ash account.sequence=4}: gas estimation failed or encountered another unrecoverable error error=gRPC call `send_tx_simulate` failed with status: status: Unknown, message: "failed to execute message; message index: 0: cannot send packet using client (07-tendermint-10) with status Expired: client state is not active [cosmos/ibc-go/v7@v7.3.0/modules/core/04-channel/keeper/packet.go:75] With gas wanted: '18446744073709551615' and gas used: '75896' ", details: [], metadata: MetadataMap { headers: {"content-type": "application/grpc", "x-cosmos-block-height": "2465374"} }
ERROR transfer error: failed while submitting the Transfer message to chain vota-ash: gRPC call `send_tx_simulate` failed with status: status: Unknown, message: "failed to execute message; message index: 0: cannot send packet using client (07-tendermint-10) with status Expired: client state is not active [cosmos/ibc-go/v7@v7.3.0/modules/core/04-channel/keeper/packet.go:75] With gas wanted: '18446744073709551615' and gas used: '75896' ", details: [], metadata: MetadataMap { headers: {"content-type": "application/grpc", "x-cosmos-block-height": "2465374"} }
```

## Action items:
[] Debug Sei client creation issue
[] Create substitution client for `archway-1`
[] Pass client substitution proposal on `vota-ash`
