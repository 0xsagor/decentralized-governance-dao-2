# Decentralized Governance DAO

This repository contains the standard architecture for a Decentralized Autonomous Organization (DAO). It leverages OpenZeppelin's Governor standards to provide a modular and secure voting infrastructure.

## Core Components
* **Governance Token (GovToken):** An ERC-20 token with "snapshots" and "delegation" capabilities. Users must delegate their voting power to themselves or others to participate.
* **Governor Contract:** Manages the lifecycle of a proposal: Propose, Vote, Succeed, Queue, and Execute.
* **Timelock Controller:** Adds a mandatory delay between a proposal's passing and its execution, providing a safety window for the community.

## Governance Parameters
* **Voting Delay:** How soon after a proposal is created that voting begins (e.g., 1 block).
* **Voting Period:** Duration of the voting window (e.g., 1 week).
* **Proposal Threshold:** Minimum tokens required to create a proposal.
* **Quorum:** Minimum percentage of total supply required to vote for a proposal to be valid.

## Quick Start
1. Deploy `GovToken.sol`.
2. Deploy `TimeLock.sol` with a set delay (e.g., 2 days).
3. Deploy `GovernorContract.sol` using the addresses from steps 1 and 2.
