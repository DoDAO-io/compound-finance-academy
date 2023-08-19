## Pause Gaurdian


## Introduction

## What is Pause Guardian?
Pause Guardian is a safeguard mechanism within the Comptroller contract in many DeFi protocols. It's an address empowered to disable selected protocol functions such as Mint, Borrow, Transfer, and Liquidate, particularly in response to an unforeseen vulnerability or crisis situation. 

Pause Guardian serves as an important risk management tool designed to preserve the integrity of the ecosystem during critical situations. This layer of protection ensures the system's stability and reduces the potential for loss during sudden market volatility or when the system faces unanticipated bugs or exploits.

The role of the Pause Guardian is to pause certain functionalities within the protocol when triggered by certain predefined conditions. This includes situations like when a stablecoin depegs significantly, an invalid price feed is received, or when a potential contract bug is detected. The purpose of this temporary pause is to prevent further detrimental actions until the situation can be fully assessed and remediated. It's a safety mechanism that bolsters the resilience of the protocol, safeguarding the investments of users within the ecosystem.

This critical role of the Pause Guardian is assigned by the COMP token-holders and is managed by the Community Multi-Sig, ensuring an additional layer of security for the ecosystem

## Process of Signing

Multisig Owners are expected to sign the transaction within 30 minutes of its proposal.

 1. One signer creates and signs the transaction.
 2. Two additional signers sign the transaction.
 3. Finally, when ready to execute, another signer signs and executes the transaction.

Gas fees for the transaction execution can be covered with funds from the operator faucet by executing the transaction via the operator faucet relayer in Defender. 





    


---
## Evaluation





##### What is the role of Pause Guardian in DeFi protocols?  
     
- [ ]  To increase the value of assets over time
- [ ]  To buy assets from a shop
- [x]  To disable selected protocol functions in response to vulnerabilities or crisis situations
- [ ]  To buy assets for fun





##### What is the process of signing a transaction in Multisig?  
     
- [ ]  One signer creates and signs the transaction.
- [ ]  Two additional signers create and sign the transaction.
- [x]  One signer creates and signs the transaction, two additional signers sign the transaction, and finally another signer signs and executes the transaction.
- [ ]  One signer signs the transaction, two additional signers sign the transaction, and finally another signer executes the transaction.





##### How long do Multisig Owners have to sign the transaction after its proposal?  
     
- [x]  30 minutes
- [ ]  1 hour
- [ ]  24 hours
- [ ]  7 days

    


---
## Details

## Assets

Each network hosts a dedicated Gnosis Safe multisig pause guardian that can be employed to perform pause functionality or modify configurations to minimize risk.

The threshold is set at 4/6, with signers from Gauntlet, Protocol Contributors, and Community Members. Once a safe is transferred to a new chain, the safe signers will carry out a signing ceremony. The transaction should not be executed until all six signers have signed it. Although it's ideal to test this on the Comet contract, it isn't strictly necessary as it can be tested separately at a later time.


## Key Participants

Within the Compound Finance ecosystem, various stakeholders play diverse roles. The table below provides a brief description of these roles. It's important to note that the roles of these stakeholder groups can overlap.

| Participant Group     | Main Role Within Compound    |
| --------------------- | ---------------------------- |
| Protocol Contributors | Operations and Development   |
| OpenZeppelin          | Security Services            |
| Gauntlet              | Risk Management              |
| Multisig Members      | Contract Administrative Actions |
| Community             | Governance                   |

Protocol contributors encompass Compound Labs, community members, and other parties who are invested in Compound's operations and development.

### Present Community Multisig Members

The table below lists the current members of the Community Multisig along with their respective addresses:

| Member               | Address                                    |
| -------------------- | ------------------------------------------ |
| Paul L. (Gauntlet)   | 0xDD659911EcBD4458db07Ee7cDdeC79bf8F859AbC |
| 0age (OpenSea)       | 0x7e4A8391C728fEd9069B2962699AB416628B19Fa |
| arr00                | 0x2B384212EDc04Ae8bB41738D05BA20E33277bf33 |
| blck                 | 0x54A37d93E57c5DA659F508069Cf65A381b61E189 |
| Jared F.             | 0xF515DCb89e67bb5D52b857d11f6C0cC2aD7D0167 |
| TennisBowling        | 0xC3AaE58Ab81663872dd36d73613eb295b167F546 |



    


---
## Evaluation





##### Who are the main stakeholders within the Compound Finance ecosystem?  
     
- [x]  Protocol Contributors, OpenZeppelin, Gauntlet, Multisig Members, and the Community
- [ ]  Protocol Contributors, OpenZeppelin, and Gauntlet
- [ ]  OpenZeppelin, Gauntlet, and Multisig Members
- [ ]  Multisig Members and the Community

    


---
## Usase Cases

# Use Cases for Pause Guardian

## Depegging of Stablecoin

In the event where a stablecoin depegs, falling below 90% of its target value, and the asset price is hardcoded, certain measures are put in place. The first action that should be taken is the suspension of borrowing. A pause can be applied by altering the borrow caps instead of directly putting a halt to borrowing, if that is the more preferred method.

## Inaccurate or Unavailable Price Feed

Should a price feed become either incorrect or inaccessible, immediate actions are required. The primary action in such circumstances would be the suspension of liquidations, assuming that is necessary under the specific conditions.

## Contract Bug of Indeterminate Nature

Given the broad range of potential contract bugs and their varying impacts on different parts of the protocol, diverse actions are needed. Initially, a pause on the affected functionality should be executed. Then, a fixed contract version should be developed and audited. A proposal for the upgraded contract should be submitted, incorporating an unpause in the proposal. Any pending non-critical proposals should be canceled. However, if the bug arose due to a recent upgrade, the affected functionality should be paused and a proposal to reverse the upgrade causing the bug should be submitted, also including an unpause in the proposal.

## Problematic Upgrade of an Underlying Asset

If the implementation of an underlying asset within Compound has a security issue, appropriate steps should be taken. The first action is to pause the market for the problematic underlying asset. A proposal for a contract upgrade to address the vulnerability should then be submitted. Alternatively, cooperation with the team of the underlying asset may be sought to rectify the issue together.

## Passed Malicious Governance Proposal

In scenarios where a malicious governance proposal passes, causing a range of potential contract bugs and affecting various parts of the protocol, certain actions are needed. If the proposal poses an immediate security threat to the protocol, all the affected functionalities within the protocol should be paused. Subsequently, a proposal to roll back the previous malicious proposal should be submitted.


    


---
## Evaluation





##### What action should be taken in the event where a stablecoin depegs, falling below 90% of its target value, and the asset price is hardcoded?  
     
- [ ]  Suspend liquidations
- [ ]  Develop and audit a fixed contract version
- [x]  Suspend borrowing
- [ ]  Submit a proposal to reverse the upgrade causing the bug





##### What is the primary action to be taken if a price feed becomes incorrect or inaccessible?  
     
- [x]  Suspend liquidations
- [ ]  Submit a proposal for a contract upgrade
- [ ]  Develop and audit a fixed contract version
- [ ]  Pause the market for the problematic underlying asset





##### What should be done if a malicious governance proposal passes, causing a range of potential contract bugs and affecting various parts of the protocol?  
     
- [ ]  Develop and audit a fixed contract version
- [x]  Pause the affected functionalities within the protocol and submit a proposal to roll back the previous malicious proposal
- [ ]  Suspend borrowing
- [ ]  Submit a proposal to reverse the upgrade causing the bug

    


---
## Responsibilities

# Pause Guardian Responsibilities
In the face of a critical situation, the Compound community promptly coordinates with the appropriate stakeholder who can accurately assess the implications of the scenario. Here are some key categories and their respective assigned owners.

## 1. Guiding Risk Management
Under the domain of **Risk Management Guidance**, Gauntlet, as the assigned owner, provides guidance to Multisig Members to effectively manage risks during a security incident. This ranges from identifying market conditions posing a risk to Compound, such as asset price levels, COMP distribution, and liquidity levels in borrowing and lending pools, to advising on interest rates and borrow/supply limits. Gauntlet also recommends risk mitigation strategies, especially concerning the implementation of pauses during risky situations.

## 2. Ensuring Security Best Practices and Alerting
**Security Best Practices and Alerting**, owned by OpenZeppelin, is focused on enhancing the security of the protocol. It involves developing, monitoring, and reviewing security alerts and conducting further investigations to determine if these alerts pose any threat to the protocol. OpenZeppelin also provides guidance on implementing best practices for the Pause Guardian's functionality.

## 3. Auditing for Secure Operations
**Audits** are an integral part of maintaining the protocol's integrity. The Community, Protocol Contributors, and OpenZeppelin, who share the responsibility, ensure that all contracts are audited before deployment. Although OpenZeppelin typically spearheads the audits, the community is encouraged to seek additional independent audits.

## 4. Enforcing Pause in Case of Security Incidents
The **Pause** responsibility rests with the Multisig Members and OpenZeppelin. They bear the responsibility of initiating pauses on specific functionalities in the event of a security incident.

## 5. Managing Unpause Process
The **Unpause** functionality, owned by the Community, plays a crucial role in resuming operations after a pause. In v2, the unpausing can only be accomplished by a community governance proposal and is subject to a 7-day governance process. However, in v3, the Pause Guardian Multisig can directly unpause without necessitating a governance proposal.

## 6. Overseeing Contract Upgrades
Lastly, **Contract Upgrades** are vital for enhancing the protocol's security and functionality. Protocol Contributors are responsible for developing and testing contract upgrades, while OpenZeppelin provides guidance on mitigating security issues and performs audits on these upgrades, ensuring they meet security standards and resolve any potential concerns.

    


---
## Evaluation





##### Who provides guidance to Multisig Members for effectively managing risks during an incident related to market conditions like Asset price levels or COMP distribution?  
     
- [x]  Gauntlet
- [ ]  OpenZeppelin
- [ ]  Community
- [ ]  Protocol Contributors





##### Who is responsible for enhancing the security of the protocol by developing, monitoring, and reviewing security alerts?  
     
- [ ]  Gauntlet
- [x]  OpenZeppelin
- [ ]  Community
- [ ]  Protocol Contributors





##### Who bears the responsibility of initiating pauses on specific functionalities in the event of a security incident?  
     
- [ ]  Gauntlet
- [ ]  OpenZeppelin
- [ ]  Community
- [x]  Multisig Members and OpenZeppelin

    

