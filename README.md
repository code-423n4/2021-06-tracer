


## ⭐️ Tracer: Contest prep
Under "Contest scope information" below, include the following:

- [ ] Name of each contract and:
  - [ ] lines of code in each
  - [ ] external contracts called in each 
  - [ ] libraries used in each 
- [ ] Describe any novel or unique curve logic or mathematical models implemented in the contracts
- [ ] Does the token conform to the ERC-20 standard? In what specific ways does it differ?
- [ ] Describe anything else that adds any special logic that makes your approach unique
- [ ] Identify any areas of specific concern in reviewing the code
- [ ] Add all of the code to this repo that you want reviewed
- [ ] Make sure your code is thoroughly commented using the [NatSpec format](https://docs.soliditylang.org/en/v0.5.10/natspec-format.html#natspec-format).
- [ ] Modify the bottom of this `README.md` file to describe how your code is supposed to work with links to any relevent documentation and any other criteria/details that the C4 Wardens should keep in mind when reviewing
- [ ] Please have final versions of contracts and documentation added/updated in this repo **no less than 8 hours prior to contest start time.**
- [ ] Ensure that you have access to the _findings_ repo where issues will be submitted. 
- [ ] **Create a PR to this repo with the above changes.**

### Provide the following info to the C4 team in the private sponsor channel we set up for you in Discord:
- [ ] Your logo (URL or add file to this repo)
- [ ] Your primary Twitter handle
- [ ] Any other Twitter handles we can/should tag in (e.g. organizers' personal accounts, etc.)
- [ ] Your Discord URI
- [ ] Your website
- [ ] Optional: Do you have any quirks, recurring themes, iconic tweets, community "secret handshake" stuff we could work in? How do your people recognize each other, for example? 

### [ ] Delete this checklist and all text above the line below when you're ready.

---

# Tracer contest details
- $80,000 USDC main award pot
- Join [C4 Discord](https://discord.gg/EY5dvm3evD) to register
- Submit findings [using the C4 form](https://code423n4.com/2021-06-tracer-contest/submit)
- [Read our guidelines for more details](https://code423n4.com/compete)
- Starts June 24 00:00 UTC
- Ends June 30 23:59 UTC

This repo will be made public before the start of the contest. (C4 delete this line when made public)

# Tracer Contest Scope
## Contracts in Scope
### Core Contracts
- `Insurance.sol`
  - 232 LOC
  - External contracts: `TracerPerpetualSwaps.sol`
  - Libraries: `LibMath.sol`, `LibInsurance.sol`, `LibBalances.sol`
- `InsurancePoolToken.sol`
  - 19 LOC
  - External contracts: None
  - Libraries: None
- `Liquidation.sol`
  - 473 LOC
  - External contracts: `Pricing.sol`, `TracerPerpetualSwaps.sol`, `Insurance.sol`, `GasOracle.sol`
  - Libraries: `LibMath.sol`, `LibLiquidation.sol`, `LibBalances.sol`, `LibPerpetuals.sol`
- `Pricing.sol`
  - 273 LOC
  - External contracts: `TracerPerpetualSwaps.sol`, `Insurance.sol`, `Oracle.sol`
  - Libraries: `LibMath.sol`, `LibPrices.sol`
- `TracerPerpetualsFactory.sol`
  - 473 LOC
  - External contracts: `PerpsDeployerV1.sol` (not in scope), `LiquidationDeployerV1.sol` (not in scope), `PricingDeployerV1.sol` (not in scope),  `InsuranceDeployerV1.sol` (not in scope)
  - Libraries:
- `TracerPerpetualSwaps.sol`
  - 599 LOC
  - External contracts: `Pricing.sol`, `Insurance.sol`, `Liquidation.sol`, `GasOracle.sol`
  - Libraries: `LibMath.sol`, `LibPrices.sol`, `LibBalances.sol`, `LibPerpetuals.sol`, `LibSafetyWithdraw.sol`
- `ChainlinkOracleAdapter.sol`
  - 66 LOC
  - External contracts: `IChainlinkOracle.sol` (out of scope)
  - Libraries: `LibMath.sol`
- `GasOracle.sol`
  - 68 LOC
  - External contracts: `IChainlinkOracle.sol` (out of scope)
  - Libraries: `LibMath.sol`
### Library Contracts
- `LibBalances`
- `LibInsurance`
- `LibLiquidation`
- `LibMaths.sol`
- `LibPerpetuals.sol`
- `LibPrices.sol`
- `SafetyWithdraw.sol`
## Novel Maths
While there is no novel maths present, an understanding of the Tracer perpetual swaps maths and mechanisms will be helpful. You can learn more from our [perpetual swaps whitepaper](https://tracer.finance/media/whitepapers/perp-swaps/Tracer_Perpetual_Swaps.pdf).

## Tokens
All tokens used within the Tracer perpetual swaps system are assumed to conform to the ERC20 standard.