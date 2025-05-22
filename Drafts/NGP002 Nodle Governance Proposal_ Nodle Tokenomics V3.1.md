# NGP002: Nodle Tokenomics V3.1

## Abstract

This Nodle Governance Proposal (NGP) details the comprehensive upgrade of the Nodle Network's tokenomics. It takes into consideration the comments and suggestions received on [NGP002: Nodle Tokenomics V3.0](https://github.com/NodleCode/governance/blob/432ebf63f5f4cbe9f9ffaeaabf974211501a6630/Drafts/NGP002%20Nodle%20Tokenomics%20V3.md)

The goal is to follow the suggestions of the community, maintaining the maximum cap.

## Motivation

This proposal aims to enhance and optimize the current tokenomics model of the Nodle Network, unlocking new opportunities for growth and sustainability.

This proposal reinforces a basic governance model, as outlined in [NGP001](https://github.com/NodleCode/governance/blob/main/Drafts/NGP001%20Creation%20of%20the%20Nodle%20DAO.md), allowing for improved decentralized management of tokenomic values, such as inflation rates and burning.

## Specification

### Key figures

| Token issuance | Disflationary  |
| :---- | :---- |
| Maximum supply | 21 Billion |
| Network issuance  | Fixed at 631.500 NODL per day until changed through governance vote |
| DAO Protocol fee on allocations | 0%. (20% protocol fee will be nullified.) |
| DAO Protocol fee on network services | None. |
| Joining missions | Done by locking NODL  |
| Acquiring network services | Done by locking NODL into subscription contracts for network services. Which is then partially or fully burned and allocated to mission participants on a case by case basis. |

### Token Supply and Rewards:

#### Current Rewards  At the time of writing, the accumulated inflation of the token supply for the year leading to the first quarter of 2024 was calculated through the following formula: 	

Rannual \= (R1\+1)(R2\+1)(R3\+1)(R4\+1) \- 1    (formula-1)

in which Ri is the planned quarterly rate for the i’th quarter of that year. The oracle follows the planned rates by around 90% to 95% accuracy (there is intentionally a bit of gap between the plan and the actual rewards so the oracle can retry failed rewards).   
With the current plan, the following quarterly inflation rates accrue from April 2024: 1.1%, 1.4%, 1.7% and 2.0%. Using formula-1 to compute the yearly inflation rate, we can work out **a total 6.3% supply inflation rate** for the year. 

#### Proposed changes 

The daily issuance is reduced by 25%, lowering the rewards issued by the Nodle network mission from currently 842k NODL to 631,500k NODL for all nodes.

### Burning Mechanism:

A burning mechanism is to be introduced by migrating Network services on-chain, and burning a portion of the fees. Here is a proposed fee schedule to be voted on by the DAO:  
 

| Item  | Description | Burning amount  | Target  On-Chain Deployment   |
| :---- | :---- | :---- | :---- |
| **Governance**  | Token weighted governance voting  | 0% | Live |
| **Network Services**  | Phase I: User rewards on chain  | 0% | Live  |
| **Network Services: On-Chain Smart Missions**  | Locking tokens to deploy and participate  missions  | 5% | Target 2026 |
| **Network Services**  | Phase II: Deploying IoT Services & Connectivity On-chain  | 100% | Target 2026 |

### 

**Smart Missions:** A 5% burning rate is applied to all tokens used as part of Smart Missions. For example, if users lock a certain amount of NODL tokens to join a smart mission, 5% of the locked tokens are removed from circulation. This rate is controlled by the DAO.

**Network Services**: 100% of tokens used to pay for location-based services are burned. This model is primarily designed for IoT customers like Roole and WATU who subscribe to the network's location services.

### Token Utility:

Several measures are proposed to enhance token utility (as defined by the table above) and bring network revenues on-chain. A paymaster mechanism, initially operated by the Nodle DAO Foundation, allows users to pay gas fees in NODL, converting them into ETH for transaction execution. This mechanism is designed to lower the barriers for entry for new users, and a fee abstraction system that shields users from the underlying complexities of Ethereum.  

**Governance**: Token holders can participate in governance by voting on protocol changes, using a token-weighted voting system. See NGP001 for more details on the architecture of the Nodle DAO and future upgrades. Anyone with enough Gas to pay a transaction fee (estimated at current market conditions to be only a few NODL) will be able to participate in governance and the future of the Nodle Network. 

**Smart Missions** : Smart Missions establish a decentralized architecture that rewards users for specific actions such as sharing Bluetooth (DePIN wireless network creation), running decentralized computation on smartphones, running a decentralized proxy network, or capturing photos. Developers determine the actions that qualify for rewards.

Users may have to  lock a discretionary amount of NODL tokens to join new missions. Tokens would be  subject to a 7-day cooldown period before unlocking, in which rewards accrue to the user's locked NODL balance. Users would be required to unlock part or all of their locked tokens once they want to exit or reduce their involvement in the mission.

Users earn mission rewards based on their locked NODL and verification status. Rewards may be in NODL, native mission creator tokens, or stablecoins (e.g., USDC) depending on the mission. For app-specific missions, rewards (e.g., USDC) are directly distributed by the mission provider. Participation requires a minimum NODL balance, with earnings determined by performance and status.

Subscription-based Smart Missions allocate tokens to users and burn a governance-controlled percentage (initially set to 5%). Burning tokens benefits the network by reducing inflation and creating deflationary potential as customer adoption grows.

**Network Services**: Network connectivity will be deployed as a simple Smart Mission type contract. Network subscribers (people using the network) will need to acquire NODL and lock these in subscription contracts akin to ERC5643 in order to get access to network services. This will ensure ease of indexing and comparison with other DePIN projects while automating support for the token as more customers are onboarded.

For IoT customers, the subscription will provide time-gated access to a Nodle Network Routing Table, effectively instructing the network where to send data packets.

This Mission is a little special in the sense that it will burn 100% of the tokens deposited into it. For Phase 1 of this Mission, services may be provided by a third party (for example Intergalactic Labs) so customers do not have to handle cryptocurrency. 

## Security Considerations

**On-chain service audit:** Each on-chain contract will need to be audited and tested as per best practice, by an independent third party auditor to ensure the safety of the network and its users. 

**Token burning:** Burning volume and thus its impact on the total supply are based on network usage. Rapid adoption of network services (and the inverse) may impact total supply and may require rapid adjustment through an on-chain governance vote.   

---

