## Compound Asset Listing


## Introduction

In collaboration with Compound, OpenZeppelin has developed a structured procedure for listing assets. This method, intended to address the security risks of Compound, derives from a comprehensive review of past asset listing proposals, community discussions, and processes adopted by other protocols. The resulting process includes a detailed checklist for security risk assessment and a sequential guide for asset listing proposals.

Users looking to implement this process must initially refer to the Process Guide, which outlines secure asset listing management from beginning to end. Gauntlet offers a complimentary Market Risk Assessment Framework within this process. The checklist is a tool for sharing necessary information with the community, marking the first step in the Asset Listing Process. An understanding of the risks is crucial, as it helps to comprehend the logic behind the checklist, process, and potential issues in integration.

The primary aim was to develop a preliminary procedure for the community to follow while securely listing assets. Feedback and improvements from the community are welcomed and encouraged. An initial objective was to list main exploration results and summarize known risks of the Compound protocol. A Risks document was produced, focusing on risks related to interaction with external assets. This document serves as a guideline for anyone evaluating new asset listings, detailing each risk category and possible mitigation through existing designs.

Post risk analysis, it was recognized that the specific risks associated with an asset must be taken into account during its listing. Hence, a checklist of queries and information requests was created for use during the asset listing process. This checklist aims to address all concerns specific to each asset and its integration. Before proposing an asset listing, the proposer must review this checklist and provide the requested information for a community check on potential integration issues. The final part of this process involves reviewing the risks, completing the checklist, and following other intermediate steps.

This effort intends to establish a secure and structured asset listing process, adaptable to community feedback and enhancements over time. Suggested improvements for the future include automated integrations for mandatory checklist completion, auto-completion of the checklist to ease proposal submission, modifications to the checklist based on community needs, improvements in tooling, formal processes for community member roles in checklist verification, and creation of a scoring framework.

    


---
## Evaluation





##### Why do we need the Compound Asset Listing Process?  
     
- [ ]  To increase the value of assets over time
- [x]  To address the security risks of Compound and ensure a secure and structured asset listing process
- [ ]  To decrease the value of assets over time
- [ ]  To buy assets for fun





##### What is the purpose of the checklist in the Compound Asset Listing Process?  
     
- [x]  To address all concerns specific to each asset and its integration
- [ ]  To increase the value of assets over time
- [ ]  To decrease the value of assets over time
- [ ]  To buy assets for fun

    


---
## Process

### Process for New Asset Listing on Compoundv3

<div align="center">
  <img style="max-height:400px;margin-bottom:30px" src="https://d31h13bdjwgzxs.cloudfront.net/academy/compound-eth-1/Guide/compound_asset_listing_compound/1689953114048_new_asset_listing_process.png"/>
</div>


The first step in the new asset listing process on Compoundv3 is the submission of a request for asset listing. A new market proposer must review the Checklist and provide as much requested information as possible in a forum post titled "Add market: {ASSET SYMBOL}" in the "New Markets" category of the Compound forum.

Following the request, the next stage is the community analysis which comprises of verification, risk analysis, and tooling and simulations. Community member(s) oversee the review of the provided information, ensuring its correctness and completeness. The community also evaluates the market risks of the asset using available data, potentially utilizing a scoring system. Gauntlet supplies a market risk assessment framework for this stage. Finally, community member(s) execute the available test suite and simulations against the contracts deployed on the target network.

The process advances to the finalization of deployment once the community analysis is complete. Here, the promoter is required to deploy any auxiliary contracts such as a price feed modifier and share the deployed contract addresses in the same forum post. A formal on-chain proposal is then drafted, including necessary parameters and explaining the reasoning behind each proposed parameter value.

Optionally, the proposal undergoes an audit. This step is taken if the community requests a review by security auditors, which can be performed by OpenZeppelin or a third party hired by the proposal author.

Following the audit, the on-chain proposal is submitted for voting. If the proposal fails, the forum post is updated with the results and provides a platform for follow-up discussions.

The final stage of the process takes place post-launch. Parameters such as the collateral factor are adjusted to safe levels and the reserve factor is set to align with other assets. Additionally, optional borrow limits can be set.


See [this](https://github.com/OpenZeppelin/compound-assets-listing/blob/master/Process.md) link for the full details of the process: https://github.com/OpenZeppelin/compound-assets-listing/blob/master/Process.md 

    


---
## Evaluation





##### What is the next stage after the submission of a request for asset listing?  
     
- [ ]  Verification of the provided information
- [ ]  Deployment of auxiliary contracts
- [x]  Community analysis
- [ ]  Adjustment of parameters post-launch





##### What is the final stage of the asset listing process?  
     
- [ ]  Verification of the provided information
- [ ]  Deployment of auxiliary contracts
- [ ]  Submission of a formal on-chain proposal
- [x]  Adjustment of parameters post-launch

    


---
## Checklist

The Compound Asset Listing Checklist provides a thorough framework for anyone proposing a new asset listing. First, general information about the token asset, including the name, project description, potential benefits to the Compound community, and pertinent resources such as websites and social media links, must be provided. Information about the proposer, their relationship with the token, and any social channel metrics are also required.

Next, a detailed Market Risk Assessment is necessary. This involves submitting the token's market cap, its historical volatility, the largest exchanges where it is listed, and any major smart contract balances. Information about the token's total supply and emission schedule is also needed. It's important to note that Gauntlet, a simulation platform for building financial models of blockchain protocols and applications, will pull live data for their market risk assessment after the checklist is submitted.

Thirdly, the decentralization aspect of the asset needs to be considered. Information about the asset's distribution among token holders, privileged roles in the token contract, and whether the asset is pausable or has a blacklist or whitelist should be provided.

The fourth section delves into smart contract risks, considering the asset's codebase, on-chain activity, and overall security posture. The proposer must provide information about audits, active bug bounty programs, and emergency contacts, as well as any additional security tools used in development.

The fifth section explores the token's multi-chain strategy and contract behavior. Information about whether the token will include implementations on other networks, how it deviates from a standard ERC20 implementation, and its unique features should be provided.

Finally, the price feed behavior, upgradability, and initial requirements need to be assessed. This includes the frequency of price updates, the entity responsible for these updates, and the threshold for price change that triggers an update. Additionally, information about the token's upgradability, who is authorized to upgrade it, and the upgradeability design should be presented. A few initial requirements include setting the collateral factor to 0 and establishing a supply cap if necessary.

Community members should review all the information provided carefully before approving a new asset. Verification of the information, assessment of new contracts, evaluation of documentation quality, and review of the token test suite or integration simulations results are all vital parts of the community check. All proposals must be first posted in the Compound forum New Markets category, and each proposal should relate solely to the listing of one token.

See [this](https://github.com/OpenZeppelin/compound-assets-listing/blob/master/Checklist.md) link for the full checklist: https://github.com/OpenZeppelin/compound-assets-listing/blob/master/Checklist.md

    


---
## Evaluation





##### What information is required in the first section of the Compound Asset Listing Checklist?  
     
- [x]  Information about the token's market cap and historical volatility
- [ ]  Information about the token's distribution among token holders
- [ ]  KYC Information of all the token token owners
- [ ]  Information about the all the protocols using the token





##### What is the purpose of the Market Risk Assessment section in the Compound Asset Listing Checklist?  
     
- [ ]  To assess the token's distribution among token holders
- [ ]  To evaluate the token's codebase and overall security posture
- [x]  To analyze the token's market cap, historical volatility, and major smart contract balances
- [ ]  To explore the token's multi-chain strategy and contract behavior

    


---
## Risks

## Protocol Risks
The protocol risks in the Compound asset listing involve multiple factors that are explained below

### Codebase vulnerability
The smart contract contains potential bugs that could be exploited. To address this concern, the Compound team has thoroughly tested the codebase and subjected it to multiple rounds of audits.

Failures in external integrations: Compound currently relies on Chainlink oracles to obtain price data. Any manipulations or inaccuracies in these oracles could result in price manipulations, which are discussed further in the market risk section.

### Governance Risks
Governance risks involve problems like wrong governance actions or governance attacks. An example of the former is the execution of a proposal containing harmful transactions, such as a large-scale COMP distribution issue. To circumvent this, OpenZeppelin's relationship with Compound has been established to prevent proposals that could undermine the protocol.

In the case of governance attacks, there's a potential risk of large quantities of COMP being concentrated through loans or purchases in a few wallets, which could threaten the governance system. However, this is currently considered an unrealistic risk due to the lack of concrete examples.

### Market Risks
The market risks, extensively analysed in Gauntlet's report, involve price manipulation, insolvency risk, non-incentivized liquidations, and a cascading effect of liquidations. If price manipulation occurs in a low liquidity market, it could lead to the liquidation of honest borrowers. Insolvency risk refers to a situation where the protocol's liabilities surpass its funds. A significant price crash could render liquidations unprofitable, leading to a dearth of incentivized liquidators. The cascade effect refers to a deflationary spiral caused by liquidations triggering more liquidations. To mitigate this, proposal #49 has been suggested.

### Network Risks
With Compound smart contracts deployed on various networks, each having unique dynamics, security models, and asset pools, network risks become a consideration. By venturing into these networks, Compound assumes risks related to network design, evm compatibility, bridge security, and native vs bridged asset dynamics, among others.


## Asset-Specific Risks
Asset-specific risks must be dealt with in a structured manner. OpenZeppelin suggests a checklist for topics to be reviewed when onboarding new assets. This checklist is complemented by a comprehensive process for listing new assets.

### Compatibility
This involves checking how extra asset features could potentially interfere with the ERC20 functions involved in Compound integration. Also, the degree of deviation of an asset from the ERC20 standard could affect the protocol's fundamental assumptions on how ERC20 tokens behave.

### Compliance
An asset's level of decentralization needs to be considered since a highly centralized asset could lead to unexpected minting and failed transfers due to blacklisting features. Additionally, like all smart contracts, assets may contain bugs that could be exploited, potentially causing issues with Compound. Therefore, identifying these bugs and studying their implications becomes critical.

Lastly, it's crucial to note the specific interactions between Compound and external asset contracts. Various protocol contracts interact with ERC20 tokens, including cTokens, and relative functions interacting in Comet, CometRewards, BaseBulker, MainnetBulker, and GovernorBravoDelegate.

### External Token interactions

Compoun interacts with external asset contracts including ERC20 tokens through various functions. Comet, an integral part of the system, employs functions like `doTransferIn` and `doTransferOut`, relying on the `transferFrom` and `transfer` functions of the ERC20 tokens, respectively. The `doTransferIn` function is used by other Comet functions like `supply`, `supplyTo`, `supplyFrom`, and `buyCollateral`, whereas `doTransferOut` is called upon by functions like `withdraw`, `withdrawTo`, `withdrawFrom`, `withdrawReserves`, and `buyCollateral`. Another function, `approveThis`, enables the governor to approve any token within the system. Additionally, `getPackedAssetInternal` and `getCollateralReserves` utilize ERC20 functions to verify asset integrity and manage reserves. These interactions ensure seamless transactions within the Compound protocol.

Other components like `CometRewards` and `BaseBulker` also engage with external contracts. CometRewards uses `doTransferOut` for token transfers, and `setRewardConfig` to establish reward schemes. BaseBulker, on the other hand, employs `sweepToken` for asset removal by an admin, and `doTransferIn` to facilitate token transfers from a user. MainnetBulker, a special case that lends out ETH against different collaterals, also employs `doTransferIn` and `doTransferOut`, specifically for the tokens steth and wsteth. Lastly, the GovernorBravoDelegate manages voting using `castVoteInternal` and cancellation of proposals with the cancel function. All these interactions demonstrate a robust and flexible system architecture that allows for diverse asset management and protocol governance within Compound.

See [this](https://github.com/OpenZeppelin/compound-assets-listing/blob/master/Risks.md) link for full details: https://github.com/OpenZeppelin/compound-assets-listing/blob/master/Risks.md

    


---
## Evaluation





##### What are the risks associated with market risks?  
     
- [ ]  Codebase vulnerability, governance risks, network risks, and asset-specific risks
- [ ]  Compliance risks, governance risks, network risks, and asset-specific risks
- [ ]  Codebase vulnerability, governance risks, and network risks
- [x]  Price manipulation, insolvency risk, non-incentivized liquidations, and a cascading effect of liquidations

    

