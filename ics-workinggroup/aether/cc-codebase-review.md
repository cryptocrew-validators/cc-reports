# ICS Code Review
**Chain:** Aether  
**Repository:** https://github.com/aetherevm/aether  
**Commit:** https://github.com/aetherevm/aether/tree/8f0386f8cd8f34cdeb3bd956ffce6e1f50c769a3

## Relevant Dependencies:

- **Cosmos SDK: [v0.47.4](https://github.com/cosmos/cosmos-sdk/releases/tag/v0.47.4)**
- **ibc-go: [v7.2.0](https://github.com/cosmos/ibc-go/releases/tag/v7.2.0)**
- **interchain-security: [v3.1.0](https://github.com/cosmos/interchain-security/releases/tag/v3.1.0)**

The support for this version of the Cosmos SDK will only consist of bug fixes in the future. 

The support for this ibc-go version will end on March 17th, 2024. No more security updates or bug fixes will be released afterwards. 

For now, all of these dependencies are still supported and no major bugs are known to affect them.

## CCV Implementation:

The consumer module as well as consumer keeper and consumer types are implemented correctly.

The consumer keeper is pre-initialized as a Non-Zero Keeper to statisfy the requirements of the IBC Keeper: 
https://github.com/aetherevm/aether/blob/8f0386f8cd8f34cdeb3bd956ffce6e1f50c769a3/app/app.go#L523

The Consumer Keeper is then later correctly re-initialized:
 https://github.com/aetherevm/aether/blob/8f0386f8cd8f34cdeb3bd956ffce6e1f50c769a3/app/app.go#L573

An IBC Route for the consumer module is also added to the IBC Router.  
Evidence and Slashing are correctly handled as well.

The order of Begin- and End-Blockers as well as the order of Genesis Initialization is legitimate.

**Additional Note:**   
Aether removes the fee-pool from a list of blocked addresses in order for the consumer-chain to be able to send tokens to the provider-chain:
https://github.com/aetherevm/aether/blob/8f0386f8cd8f34cdeb3bd956ffce6e1f50c769a3/app/app.go#L459

## Summary:
The implementation of Cross Chain Validation has been handled well and no apparant code issues have been found during this review.  
***Note: The scope of this code review was to only assess parts of the code relevant to Cross Chain Validation.***

## Suggestions:
Given that the support for ibc-go v7.2.0 is ending on March 17th, the team should consider upgrading to a newer version before than.






