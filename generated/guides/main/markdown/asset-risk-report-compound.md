## Asset Risk Report


## Introduction

This comprehensive guide is designed to equip any community member with the necessary information and resources to independently draft a token report. Each report will focus on one token across multiple chains, detailing the specifics of its behavior, structure, and utilization on each chain. 

The objective of the token report is to provide a succinct, comprehensive examination of the token in question, its functionality on various chains, and its overall implications for users. To achieve this, the report is divided into several sections, each focusing on a specific aspect of the token. From an Executive Overview, providing a summarized introduction, to sections detailing various features like 'Upgradeable', 'Burnable', and 'FlashMintable' - all these components of the report play a vital role in providing a holistic understanding of the token.

As a report writer, you are encouraged to present information in a clear and concise manner, aiming to create a coherent document that effortlessly guides the reader through the complexities of the token analysis. Each section, be it the 'Summary Page', 'Details and Backup', or the 'Disclaimer', contributes to the overall understanding of the token's properties and behavior. With this guide as your reference, you'll be equipped to explore and articulate the intricacies of token behavior on various chains, a fundamental aspect of understanding the dynamic world of digital currencies.

The structure of the report is informed by the security recommendations outlined by OpenZeppelin, as detailed in this [guide](https://compound.education/guides/view/compound-asset-listing-compound/0) and further elaborated in this [GitHub repository](https://github.com/OpenZeppelin/compound-assets-listing).

    


---
## Evaluation





##### What is the objective of the token report?  
     
- [ ]  To create a coherent document that guides the reader through the complexities of the token analysis
- [ ]  To explore and articulate the intricacies of token behavior all chains
- [ ]  To provide a summarized introduction of the token market conditions
- [x]  To provide a comprehensive examination of the token, its functionality on various chains, and its overall implications for users

    


---
## Report Format

The report comprises the following sections:

### Executive Overview

This section provides a brief, high-level summary of the report in no more than three paragraphs. It introduces the token's name, its uses, and the organization that originated it. Moreover, it presents a rundown of the token report's key highlights for each chain. This section typically has one paragraph dedicated to the token and another paragraph highlighting aspects related to each chain.

### Summary Page

The Summary Page is a one-page review of every aspect examined for the token on a specific chain. It presents a succinct summary of all points of investigation, linking to the respective sections in the document for detailed insights. Each token/chain combination will have its distinct summary page.

### Details and Backup

This section dives deeper into the details for each token on each chain included in the report. It comprises a comprehensive breakdown of the following elements:

1. **Token on Chain**: This section will present a detailed view of the token on its respective chain, such as wBTC on Ethereum Mainnet.

2. **Pausable**: This part covers whether the token contract can be paused or not, detailing who can pause it and how it works if applicable.

3. **BlackListable**: This segment explores if there's any blacklist code within the token contract, outlining its functionalities and which features it impacts if present.

4. **ERC-20 Standard Compliance**: Here, we'll verify if all function calls of the token contract adhere to the ERC-20 standard, summarizing the overall status.

5. **Math Protection**: This section discusses whether the token contract has math protection against overflows and underflows.

6. **Mintable**: This area explores if the token's contract allows the owner to mint new tokens and provides a detailed description if applicable.

7. **Burnable**: This section investigates if the token contract permits the owner to burn tokens, offering a comprehensive explanation if relevant.

8. **Rebasing**: This portion deals with whether the token code allows for rebasing of the total number of tokens issued, providing a detailed explanation and code snippets if necessary.

9. **Fees on transfer**: This segment covers if any fees are levied on the token transfer and details the logic behind such fees if they exist.

10. **DelegateCalls**: This part focuses on the presence of DelegateCall functions in the token code that can potentially add significant risks to the DeFi protocol.

11. **Flashloanable**: This area investigates whether the token can be used in a flash loan, providing a detailed analysis if the answer is affirmative.

12. **FlashMintable**: This section checks if the token allows flash mints and explains the potential impacts on price and total supply if flash mints can occur.

Detailed Report format can be found [here](https://docs.google.com/document/d/1hjX1D95atG0-Jg5p-GKMNrMAwhsa11t0) 

    


---
## Evaluation





##### What is the purpose of the Executive Overview section in a detailed report?  
     
- [ ]  To present a detailed breakdown of the token on each chain included in the report
- [x]  To provide a brief, high-level summary of the report
- [ ]  To discuss the presence of DelegateCall functions in the token code
- [ ]  To investigate whether the token can be used in a flash loan





##### What does the Summary Page in a detailed report consist of?  
     
- [ ]  A detailed view of the token on its respective chain
- [ ]  A breakdown of the ERC-20 standard compliance for the token
- [x]  A one-page review of every aspect examined for the token on a specific chain
- [ ]  An analysis of whether the token allows flash mints





##### What does the 'BlackListable' section in a detailed report explore?  
     
- [ ]  Whether the token contract can be paused or not
- [ ]  Whether the token contract adheres to the ERC-20 standard
- [ ]  Whether the token contract has math protection against overflows and underflows
- [x]  Whether there's any blacklist code within the token contract





##### What does the 'Fees on transfer' section in a detailed report cover?  
     
- [x]  If any fees are levied on the token transfer and the logic behind such fees
- [ ]  If the token contract can be paused or not
- [ ]  If the token contract adheres to the ERC-20 standard
- [ ]  If the token contract has math protection against overflows and underflows

    


---
## Sample

Here is the sample of Executive Overview and Summary of USDC on Ethereum


## Executive Overview
USDC is a centralized stable coin run by Circle Corporation.  It is highly permissioned. The token can be upgraded, paused and has blacklists.  This report covers USDC on Ethereum mainnet and Optimism.  We can add other chains upon request.
USDC on mainnet’s code is more complex than the ERC20 standard.  The code is upgradable it has changed 3 times, the latest on Aug 2020.  There is no timelock on upgrades, they are instantaneous.  Circle controls an active blacklist and can pause trading in USDC at any time.  The token can be used in flashloans.


**Disclaimer**
The purpose of these reports is a succinct technical summary for devs and auditors when considering using a token on a chain.  It is designed to use their time more efficiently.  DeFiSafety’s team are analysts, not devs or auditors.  

## Summary
USDC on Ethereum Mainnet Summary

| Feature                | Details                                                                    |
|------------------------|----------------------------------------------------------------------------|
| Address                | [Link](https://etherscan.io/address/0xa0b86991c6218b36c1d19d4a2e9eb0ce3606eb48) |
| Owner                  | [Link](https://etherscan.io/address/0x95ba4cf87d6723ad9c0db21737d862be80e93911) |
| Protocol               | Circle Corporation                                                         |
| GitHub                 | Not available                                                              |
| Solidity Version       | ^0.6.1.2                                                                   |
| Upgradeable            | YES                                                                        |
| Pausable               | YES                                                                        |
| BlackList              | YES                                                                        |
| ERC20 Standard Compliant| Partially                                                                   |
| Math Protection        | Yes (SafeMath 0.6.0)                                                       |
| Mintable               | Yes                                                                        |
| Burnable               | Yes                                                                        |
| Rebasing               | No                                                                         |
| Fees on Transfer       | No                                                                         |
| DelegateCalls          | No                                                                         |
| Flashloanable          | Yes                                                                        |
| FlashMintable          | Yes                                                                        |

    


---
## Examples

Here is the list of reports that were created by DeFiSafety team

1. [USDC on Mainnet and Opt](https://docs.google.com/document/d/13rWX_tiFVL-suiaih1MvGmvQMKd4YgZj/edit?rtpof=true&sd=true)
2. [wBTC on Mainet and Opt](https://docs.google.com/document/d/13y6ZwJROyroNZzkYuVxDr76Y2oLzQD4B/edit)
3. [wEth on Mainet and Opt](https://docs.google.com/document/d/1SfuMdI_Wqlwgbetrg2G5FZlU4qqToX5i/edit?rtpof=true&sd=true)
4. [OPT on Opt](https://docs.google.com/document/d/1T8tYUXsgqwkiz3-06dyA5PG-cmLHou7b/edit)


Details to their proposal to create these reports can be found [here](https://www.comp.xyz/t/grant-for-technical-risk-report-of-3-asset-listings/4105/6)

    

