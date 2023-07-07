
# Index Update contest details

- Join [Sherlock Discord](https://discord.gg/MABEWyASkp)
- Submit findings using the issue page in your private contest repo (label issues as med or high)
- [Read for more details](https://docs.sherlock.xyz/audits/watsons)

# Q&A

### Q: On what chains are the smart contracts going to be deployed?
Mainnet, Polygon, Optimism, Arbitrum, Avalanche
___

### Q: Which ERC20 tokens do you expect will interact with the smart contracts? 
Any
___

### Q: Which ERC721 tokens do you expect will interact with the smart contracts? 
None
___

### Q: Which ERC777 tokens do you expect will interact with the smart contracts? 
None
___

### Q: Are there any FEE-ON-TRANSFER tokens interacting with the smart contracts?

No
___

### Q: Are there any REBASING tokens interacting with the smart contracts?

No
___

### Q: Are the admins of the protocols your contracts integrate with (if any) TRUSTED or RESTRICTED?
TRUSTED
___

### Q: Is the admin/owner of the protocol/contracts TRUSTED or RESTRICTED?
TRUSTED
___

### Q: Are there any additional protocol roles? If yes, please explain in detail:
SetToken Manager
- Whitelisted to manage Modules on the SetToken
- Whitelisted to rebalance the SetToken
- Able to collect streaming fees of SetToken when the rebalance does not lock

SetToken Holders
- Able to mint/redeem for underlying collateral of SetToken when the rebalance does not lock

Rebalance Bidders
- Able to execute token exchanges according to the price configured by the SetToken Manager
- Should not be able to decay the SetToken Net-Asset-Value according to this price. with any combination of actions (bids, mints, or redeems)
___

### Q: Is the code/contract expected to comply with any EIPs? Are there specific assumptions around adhering to those EIPs that Watsons should be aware of?
No
___

### Q: Please list any known issues/acceptable risks that should not result in a valid finding.
No

___

### Q: Please provide links to previous audits (if any).
Last Sherlock Audit https://github.com/sherlock-audit/2023-05-Index-judging

BasicIssuanceModule:
- OpenZeppelin: https://blog.openzeppelin.com/set-protocol-audit/
- ABDK: https://1162024285-files.gitbook.io/~/files/v0/b/gitbook-x-prod.appspot.com/o/spaces%2F-MJY-enmfAw5ra2s-8QX%2Fuploads%2FQApRQYHEn7GrBqHJWT8a%2FABDK%20Set%20Protocol%20v2%20Audits.pdf?alt=media&token=ac08addf-4371-411f-b0e0-17b042ac7f84
___

### Q: Are there any off-chain mechanisms or off-chain procedures for the protocol (keeper bots, input validation expectations, etc)?
No
___

### Q: In case of external protocol integrations, are the risks of external contracts pausing or executing an emergency withdrawal acceptable? If not, Watsons will submit issues related to these situations that can harm your protocol's functionality.
Acceptable
___



# Audit scope


[index-protocol @ 663e64efaa95df2247afa8926d4cfb42948f54fe](https://github.com/IndexCoop/index-protocol/tree/663e64efaa95df2247afa8926d4cfb42948f54fe)
- [index-protocol/contracts/protocol/integration/auction-price/BoundedStepwiseExponentialPriceAdapter.sol](index-protocol/contracts/protocol/integration/auction-price/BoundedStepwiseExponentialPriceAdapter.sol)
- [index-protocol/contracts/protocol/integration/auction-price/BoundedStepwiseLinearPriceAdapter.sol](index-protocol/contracts/protocol/integration/auction-price/BoundedStepwiseLinearPriceAdapter.sol)
- [index-protocol/contracts/protocol/integration/auction-price/BoundedStepwiseLogarithmicPriceAdapter.sol](index-protocol/contracts/protocol/integration/auction-price/BoundedStepwiseLogarithmicPriceAdapter.sol)
- [index-protocol/contracts/protocol/integration/auction-price/ConstantPriceAdapter.sol](index-protocol/contracts/protocol/integration/auction-price/ConstantPriceAdapter.sol)


