## Protocol Contribution Process


## Introduction

### About this Guide
This guide elucidates a systematic methodology for streamlining the development and appraisal of protocol contributions with a specific focus on community engagement and quality assurance of the protocol prior to adoption. The guide delineates a structured series of steps, each designed to progressively validate and improve each contribution. These steps are organized into five primary stages, reflecting the journey of a contribution from the initial concept stage through to the conclusive review, before it is finally advanced to be a proposition for on-chain governance.

### Motivation
The objective behind this guide is to introduce a higher degree of transparency and understanding to the process of making contributions to the Compound protocol. The details included in the guide illustrate a universal approach that is capable of being applied across a wide spectrum of contributions, thereby making the process more inclusive and efficient. This methodological guide is particularly designed to facilitate and encourage submissions from new contributors, whilst maintaining a minimal burden on those who are continuing to contribute.

The suggested structure not only accommodates input from a diverse range of contributors but also sets the stage for constant improvement and iterative refinement of ideas. By offering a clear roadmap of the contribution lifecycle, from ideation through final review, this guide seeks to strengthen the community's engagement and involvement in protocol development, while at the same time ensuring the high quality of the contributions.

    


---
## Contribution Process

### 5-Stage Process from Conception to Adoption for Refining Proposals

This process includes stages for multiple refinements and feedback integration. The stages help to prepare proposals for varying audience review, and communication is advised throughout.


<div align="center">
  <img style="max-height:400px;margin-bottom:30px" src="https://d31h13bdjwgzxs.cloudfront.net/academy/compound-eth-1/Guide/protocol_contribution_process_compound/1689889093217_compound_contribution_steps.png"/>
</div>


### 1. Idea Review
This initial stage is for idea sharing and community feedback integration. For grant applications, a refined idea should be ready for submission by stage end.

- Start a discussion post in the Compound Forum with sufficient detail.
- Gauge community interest before dedicating effort to a contribution.
- Refine the idea using community feedback.
- Outline the scope and broad technical details of the solution.
- Optional: For additional feedback from CIP Editors, draft a CIP-style proposal, especially for complex design decisions.

### 2. Development Review
The aim here is to provide feature-complete code with developer feedback from the community. This stage suits contributions requiring new contracts or existing contract updates.

- Develop a draft contribution, including tests, for community developers to review.
- Announce the proposal in the Compound Forum and optionally in the #development Discord channel. Detail the contribution, its expected behavior, and repository location to invite feedback. Use "CIP-X: Development Review" as your forum post status.
- Request an external audit if contract code is involved.


### 3. Community Review
This stage finalizes configuration and parameter values with community feedback.

- Submit a pull request and make additional commits as necessary.
- Post revised contribution details with test and simulation results to the Compound Forum for review. Use “CIP-X: Community Review” to indicate your contribution status.
- Provide a repository location and expected code freeze date to request a final external audit estimate, if contract code is involved.
- Create reports of test and simulation results.

### 4. External Review
This stage rectifies any audit issues. The audited contract version should be the final deployed version. Only changes to code in this stage should be audit issue remedies, and any remediation should undergo auditor review.

- Submit the pull request and latest contract version's source control commit ID URL to the auditor.
- Update the community on the latest testing and simulation results along with the audit status. Use "CIP-X: External Review" as your forum post status.
- Share audit results and any other security recommendations with the community.


### 5. Final Review
This concluding stage proposes the changes on-chain.

- Post audit, generate test and simulation result reports based on the final code commit. Use “CIP-X: Final Review” as your forum post status.
- Generate migration and proposal simulation results.
- Submit a pull request against the official protocol repository to include changes.
- Sign and execute the migration to submit the on-chain proposal.
- Announce the pull request with commit ID details and test and simulation results to the community, indicating a pending proposal vote.
- After a successful vote and proposal execution, test the upgrade's effectiveness and merge the pull request.








    


---
## Evaluation





##### What is the purpose of the Idea Review stage in the contribution process for Compound Protocol?  
     
- [ ]  To develop a draft contribution with tests for community developers to review
- [ ]  To submit a pull request and make additional commits as necessary
- [x]  To start a discussion post in the Compound Forum with sufficient detail, gauge community interest, refine the idea using community feedback, and outline the scope and broad technical details of the solution
- [ ]  To generate test and simulation result reports based on the final code commit





##### What is the aim of the Development Review stage in the contribution process for Compound Protocol?  
     
- [ ]  To develop a draft contribution with tests for community developers to review
- [x]  To provide feature-complete code with developer feedback from the community. This stage suits contributions requiring new contracts or existing contract updates
- [ ]  To submit a pull request and make additional commits as necessary
- [ ]  To post audit, generate test and simulation result reports based on the final code commit





##### What is the purpose of the External Review stage in the contribution process for Compound Protocol?  
     
- [ ]  To develop a draft contribution with tests for community developers to review
- [ ]  To provide feature-complete code with developer feedback from the community. This stage suits contributions requiring new contracts or existing contract updates
- [x]  To rectify any audit issues. The audited contract version should be the final deployed version. Only changes to code in this stage should be audit issue remedies, and any remediation should undergo auditor review
- [ ]  To post audit, generate test and simulation result reports based on the final code commit

    


---
## Rationale

This guide seeks to unify the process of contributing to the protocol, reflecting established best practices but broadened to be applicable in a wide range of situations. The call for a transparent, defined contribution procedure stems from historical instances of protocol updates that led to security vulnerabilities. Despite rigorous bug testing and proactive community outreach for feedback, these security issues were not detected until they became critical. Introducing a five-step contribution procedure paves the way for multiple quality control checkpoints and the early identification of potential security risks.

Additionally, this structure gives contributors a clear pathway to their end goal, eliminating the ambiguity of deciding when and how to report their development progress and quality control efforts to the community. In the decentralized world of Compound development and governance, it's even more crucial that we clearly communicate the expectations for contributions to both contributors and DAO voters.

### Expected Impact
Implementation of this process is anticipated to have several positive impacts. For starters, it's expected to streamline the contribution process for newcomers, while concurrently minimizing the burden on existing contributors. It's also likely to accelerate the evaluation of Compound Governor proposals by establishing regular, timely communication of evaluation criteria.

Further, the contribution process aims to stimulate more active participation in both contributions and evaluation processes. Predictability of the process duration, a feature particularly relevant for grant proposals, is also set to improve. This, in turn, will foster confidence in protocol changes by enhancing transparency and accessibility.

Additionally, this process will provide enhanced direction for grant recipients, making it easier for them to achieve necessary milestones within the Compound grants program, thereby facilitating payment disbursement.

    


---
## Evaluation





##### What is the rationale for the contribution process?  
     
- [ ]  To make it easier for grant recipients to achieve necessary milestones
- [ ]  To eliminate the ambiguity of reporting development progress and quality control efforts
- [ ]  To establish regular, timely communication of evaluation criteria
- [x]  All of the above

    


---
## Final Words

The formalization of contribution guidelines for on-chain upgrades and deployments aims to significantly elevate the quality assurance standard for each contribution, thereby reinforcing the overall protocol's security. This process of creating a structured framework for contributions doesn't prescribe the usage of specific tools for achieving each requirement, but it is anticipated that much of the existing infrastructure in the Compound repositories, particularly the testing and security tools, will be employed.

This structured contribution process is expected to act as a catalyst for the development of additional testing and security tools for the Compound repositories. These tools would be designed to better streamline the contribution process, possibly by adding levels of automation. The goal is to increase efficiency, minimize potential human-induced errors, and reduce the turnaround time for protocol enhancements.

The development and integration of new tools would also likely trigger a learning curve among contributors, thereby raising the overall skill level and knowledge base within the Compound ecosystem. This skills enhancement, along with the more robust toolset, can further drive the quality of contributions, making the protocol even more secure and resilient.

In the long run, these reinforced security considerations are not only expected to bolster the protocol's integrity but also to fortify trust among users and stakeholders. After all, a more secure protocol translates to increased user confidence, ultimately resulting in a healthier, more vibrant ecosystem. So, by combining the formalization of contribution guidelines with the continued usage and enhancement of testing and security tools, we are setting the stage for a much more secure, efficient, and resilient protocol development process.

    

