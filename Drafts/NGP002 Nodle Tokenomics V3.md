# NGP002: Nodle Tokenomics V3

![NGP002](https://github.com/user-attachments/assets/1fffe5bf-26f1-4141-a08c-33696a700b88)


## Abstract

This Nodle Governance Proposal (NGP) details the comprehensive upgrade of the Nodle Network's tokenomics, transitioning from an inflationary model to a disinflationary one (based on burning) significantly reducing the total supply depending on usage and burn rate.

Key components include a burning mechanism tied to various network services, updated reward mechanics that favor active users, and enhanced token utility across multiple on-chain applications.

The goal is to create a more sustainable network economics by reducing token supply over time, incentivizing participation, and distributing rewards in a more controlled and effective manner. The further development of the DAO, and potential areas of expansion are also covered in the document.

## Motivation

This proposal aims to enhance and optimize the current tokenomics model of the Nodle Network, unlocking new opportunities for growth and sustainability.It proposes a disinflationary model that (depending on usage) is expected to significantly reduce the total supply, and align incentives of network participants.

The introduction of  a usage based on-chain burning mechanism aims to counter inflationary forces created by user rewards, thereby decreasing the total supply as usage and adoption ramp up.

This Proposal highlights the migration of several services that were traditionally handled off-chain, bringing them on-chain, thus contributing to the decentralization and security of the network.

And finally, this proposal reinforces a basic governance model, as outlined in [NGP001](https://github.com/NodleCode/governance/blob/main/Drafts/NGP001%20Creation%20of%20the%20Nodle%20DAO.md), allowing for improved decentralized management of tokenomic values, such as inflation rates and burning.

## Specification

### Key figures

| Token issuance | Disflationary |
| --- | --- |
| Maximum supply | Flexible based on network usage, and decreasing once enough burning is reached |
| Network issuance | Fixed at appx 5% per year |
| DAO Protocol fee on allocations | 0%. (20% protocol fee will be nullified.) |
| DAO Protocol fee on network services | None. |
| Joining missions | Done by locking NODL |
| Acquiring network services | Done by locking NODL into subscription contracts for network services. Which is then partially burned and allocated to mission participants on a case by case basis. |

### Token Supply and Rewards:

### Current Rewards At the time of writing, the accumulated inflation of the token supply for the year leading to the first quarter of 2024 was calculated through the following formula:

Rannual = (R1+1)(R2+1)(R3+1)(R4+1) - 1    (formula-1)

in which Ri is the planned quarterly rate for the i’th quarter of that year. The oracle follows the planned rates by around 90% to 95% accuracy (there is intentionally a bit of gap between the plan and the actual rewards so the oracle can retry failed rewards).

With the current plan, the following quarterly inflation rates accrue from April 2024: 1.1%, 1.4%, 1.7% and 2.0%. Using formula-1 to compute the yearly inflation rate, we can work out **a total 6.3% supply inflation rate** for the year 2024.

### Proposed changes

To simplify the Tokenomics, a **fixed target inflation rate of 5% is introduced** in this proposal. This may be updated through a DAO governance vote as outlined in NGP001.

**Burning**: Introduction of a Burning mechanism associated with network usage and Network Services (outlined below). The token supply is expected to become deflationary through a new burning mechanism, as the rate of burning will likely be superior to the new minting rate.

**Maximum Supply:** Through Burning, The Nodle Network will become Disflationary. The result is a target maximum supply that is expected to be cut by more than half, depending on the rate of network usage. See the graph below which outlines one scenario.

**Fixed Rewards Curve:** The reward issuance will be fixed based on a target inflation rate. This is expected to be surpassed by burning, contributing towards deflation. At this point a fixed rewards amount in tokens may be voted upon by the Nodle DAO.

**Inflation Rate:** A fixed rate of approximately 5% per year. This rate is not static, but it's an annual target; the actual issuance may fluctuate slightly based on block times and oracle adjustments. As the network becomes disflationary this value may be set as a fixed rewards amount or based on network usage.

**Issuance Control:** The Network DAO will be able to control this annual inflation rate through governance votes, giving the community control of the network's monetary policy.

A NODL supply curve was calculated based on an intermediate scenario of <$10M USD of services being rendered on-chain. This is subject to change based on network usage and values votes in by the Nodle DAO.

<img width="1091" alt="Screenshot 2025-04-01 at 11 52 41 AM" src="https://github.com/user-attachments/assets/d22b3851-a6c9-4008-b9f6-81fb93b5917d" />


### Burning Mechanism:

A burning mechanism is to be introduced by migrating Network services on-chain, and burning a portion of the fees. Here is a proposed fee schedule to be voted on by the DAO:

| **Item** | **Description** | **Burning amount** | **Target On-Chain Deployment** |
| --- | --- | --- | --- |
| **Governance** | Token weighted governance voting | 0% | Live |
| **Network Services** | Phase I: User rewards on chain | 0% | Live |
| **Network Services: On-Chain Smart Missions** | Locking tokens to deploy and participate  missions | 5% | Target 2025 |
| **Network Services** | Phase II: Deploying IoT Services & Connectivity On-chain | 100% | Target 2025 |

**Smart Missions:** A 5% burning rate is applied to all tokens used as part of Smart Missions. For example, if users lock a certain amount of NODL tokens to join a smart mission, 5% of the locked tokens are removed from circulation. This rate is controlled by the DAO.

**Network Services**: 100% of tokens used to pay for location-based services are burned. This model is primarily designed for IoT customers like Roole and WATU who subscribe to the network's location services

**Smart Envelopes**: A 5% burning rate is applied to the NODL tokens used when creating smart envelopes.

**Future Explorations**

- **Decentralized PKI:** A fraction of the fee is burned for creation of a root certificate on-chain and access to an API. This burning rate may be modified by the Nodle DAO.
- **Content Authentication (Click Certify)**:Incentivizing the use of network services.

### Token Utility:

Several measures are proposed to enhance token utility (as defined by the table above) and bring network revenues on-chain. A paymaster mechanism, initially operated by the Nodle DAO Foundation, allows users to pay gas fees in NODL, converting them into ETH for transaction execution. This mechanism is designed to lower the barriers for entry for new users, and a fee abstraction system that shields users from the underlying complexities of Ethereum.

**Governance**: Token holders can participate in governance by voting on protocol changes, using a token-weighted voting system. See NGP001 for more details on the architecture of the Nodle DAO and future upgrades. Anyone with enough Gas to pay a transaction fee (estimated at current market conditions to be only a few NODL) will be able to participate in governance and the future of the Nodle Network.

**Smart Missions** : Smart Missions establish a decentralized architecture that rewards users for specific actions such as sharing Bluetooth (DePIN wireless network creation), running decentralized compute on smartphone, running a decentralized proxy network, or capturing photos. Developers determine the actions that qualify for rewards.

Users may have to  lock a discretionary amount of NODL tokens to join new missions. Tokens would be  subject to a 7-day cooldown period before unlocking, in which rewards accrue to the user's locked NODL balance. Users would be required to unlock part or all of their locked tokens once they want to exit or reduce their involvement in the mission.

Users earn mission rewards based on their locked NODL and verification status. Rewards may be in NODL, native mission creator tokens, or stablecoins (e.g., USDC) depending on the mission. For app-specific missions, rewards (e.g., USDC) are directly distributed by the mission provider. Participation requires a minimum NODL balance, with earnings determined by performance and status.

Subscription-based Smart Missions allocate tokens to users and burn a governance-controlled percentage (initially set to 5%). Burning tokens benefits the network by reducing inflation and creating deflationary potential as customer adoption grows.

**Network Services**: Network connectivity will be deployed as a simple Smart Mission type contract. Network subscribers (people using the network) will need to acquire NODL and lock these in subscription contracts akin to ERC5643 in order to get access to network services. This will ensure ease of indexing and comparison with other DePIN projects while automating support for the token as more customers are onboarded.

For IoT customers, the subscription will provide time-gated access to a Nodle Network Routing Table, effectively instructing the network where to send data packets.

This Mission is a little special in the sense that it will burn 100% of the tokens deposited into it. For Phase 1 of this Mission, services may be provided by a third party (for example Intergalactic Labs) so customers do not have to handle cryptocurrency.

**Smart Envelopes**: In line with the vision to make Web3 easy and accessible to all, Smart envelopes were piloted in early 2024 to make it easy to send crypto to people who do not have a wallet. The concepts used “magic links”, unique URLs that unlocked a wallet for the first person to click on the link, install the wallet, and claim the envelope. This allows Smart Envelopes to be sent over messaging apps (even SMS) to non-crypto users who can easily click the link, install the wallet, and receive funds.

This document proposes deploying Smart Envelopes on-chain, requiring a small amount of Nodle which will be burned by the network.

**Future tokenomic explorations (out of scope)**

- Click Certify: Tokens are burned when using Click Certify services.
- Decentralized PKI: A fee is charged in NODL to register certificates on-chain. Certificate slots last for 1 year, and must be renewed. A fraction of the fee is burned. Certificates would be used to scale C2PA implementations.

## Security Considerations

**On-chain service audit:** Each on-chain contract will need to be audited and tested as per best practice.

**Token burning:** Burning volume and thus its impact on the ****total supply are based on network usage. Rapid adoption of network services (and the inverse) may impact total supply and may require rapid adjustment through an on-chain governance vote.
