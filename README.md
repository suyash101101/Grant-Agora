# Agora

- **Team Name:** Agora
- **Payment Details:**
  - **DOT:** 1QvwVTx1G4ZhPjE68zEkZDjcLFkJwTMkgKk8FYWWKmsGjcc
  - **Payment:** 1QvwVTx1G4ZhPjE68zEkZDjcLFkJwTMkgKk8FYWWKmsGjcc (USDC)
- **[Level](https://grants.web3.foundation/docs/Introduction/levels):** 2

## Project Overview :page_facing_up:

### Overview

- **Tagline:** Verifiable Off‑Chain Computation via Commit‑Reveal and XCM.
- **Brief Description:** Agora is a Polkadot parachain template extended with a verifiable computation marketplace. It enables parachains to outsource off‑chain jobs (API fetches, computations) to a network of staked workers. Results are verified on‑chain using a crypto‑economic commit‑reveal game. Cross‑parachain requests and result delivery use XCM.
- **Integration:** Agora integrates into the Polkadot ecosystem as a parachain that provides a service (verifiable computation) to other parachains via XCM. It leverages Substrate for the chain logic and Polkadot's shared security.
- **Interest:** The team is interested in creating this project to solve the problem of trustless off-chain computation and data fetching, enabling a decentralized oracle and computation network within the Polkadot ecosystem without relying on trusted execution environments (TEEs) or centralized providers.

### Project Details

**Mockups/Designs:**
- App Workflow: `assets/App_Workflow.png`
- XCM Workflow: `assets/XCM_Workflow.png`
- OCW Workflow: `assets/OCW_Workflow.png`
- Logo: `assets/logo.png`

**Video Demo:**
- [Watch Agora Demo Video](https://www.youtube.com/watch?v=3V9ne5yBJFs&t=2s)
- [Watch Agora Walkthrough](https://app.supademo.com/demo/cm6xuj2sr01o8pegv3s411vap)

**Architecture:**
- **Runtime:** FRAME-based Substrate runtime including `agora` pallet.
- **Agora Pallet:** Handles job lifecycle (submit -> commit -> reveal -> finalize), staking, rewards/slashing, and XCM handling.
- **Off-Chain Worker (OCW):** Handles execution of jobs (API fetches, computation) and submits commits/reveals.
- **XCM:** Uses `Transact` for cross-chain job submission and HRMP for result delivery.

**Technology Stack:**
- **Blockchain:** Rust, Substrate, Polkadot SDK.
- **Frontend:** React, Vite, TailwindCSS, Polkadot JS API.
- **Scripts:** Node.js, JavaScript.

**Core Components:**
- `pallets/agora`: The core logic for the computation marketplace.
- `node`: The collator binary.
- `ui`: The React-based dashboard for interacting with the marketplace.

**PoC/MVP:**
- The current repository serves as the MVP, featuring a working local testnet (Zombienet) with XCM enabled, a functional `agora` pallet with commit-reveal mechanism, and a basic UI.

**What it is NOT:**
- It is not a general-purpose smart contract platform (though it uses a pallet).
- It is not a TEE-based solution (it uses crypto-economic incentives).

### Ecosystem Fit

- **Fit:** Agora fits as a utility parachain providing decentralized computation and oracle services to other parachains.
- **Target Audience:** Parachain developers needing off-chain data/compute, DeFi protocols requiring oracles, and users wanting to run worker nodes.
- **Needs Met:** Trustless access to off-chain data and computation without centralized intermediaries.
- **Differentiation:** Unlike TEE-based solutions (e.g., Phala), Agora uses crypto-economic verification (commit-reveal), which avoids hardware dependencies. Unlike centralized oracles, it is decentralized and permissionless.

## Team :busts_in_silhouette:

### Team members

- Suyash D Nahar
- Nikhil Kottoli

### Contact

- **Contact Name:** Suyash D Nahar
- **Contact Email:** nahsrsuyash@gmail.com, nikhilkottoli2005@gmail.com
- **Website:** X

### Team's experience

X

### Team Code Repos

- https://github.com/paritytech/polkadot-sdk-parachain-template (Base template)
- https://github.com/suyash101101/Agora

### Team LinkedIn Profiles (if available)

- https://www.linkedin.com/in/suyash101/
- https://www.linkedin.com/in/nikhil-kottoli-92552128a/

## Development Status :open_book:

- **Code:** [https://github.com/suyash101101/Agora](https://github.com/suyash101101/Agora)
- **Demo Video:** [Watch Agora Demo Video](https://www.youtube.com/watch?v=3V9ne5yBJFs&t=2s)
- **Walkthrough:** [Watch Agora Walkthrough](https://app.supademo.com/demo/cm6xuj2sr01o8pegv3s411vap)

## Development Roadmap :nut_and_bolt:

### Overview

- **Total Estimated Duration:** 4 months
- **FTE:** 2
- **Total Costs:** 30,000 USD
- **DOT %:** 50%

### Milestone 1 — Core Functionality & Local Testnet

- **Estimated duration:** 2 months
- **FTE:** 2
- **Costs:** 15,000 USD

| Number | Deliverable | Specification |
| -----: | ----------- | ------------- |
| **0a.** | License | MIT-0 / Apache 2.0 |
| **0b.** | Documentation | Inline docs for `agora` pallet and a guide on running the local Zombienet setup. |
| 1. | Code Cleanup | Clean hackathon code and fix minor bugs in the `agora` pallet. |
| 2. | Ecosystem Survey | Reach Out to parachains and ask them for desired additional features|
| 3. | Professional UI | Improve and make a professional React-based UI dashboard. |
| 4. | Deployment | Basic deployment and setup of RPC Endpoint. |

### Milestone 2 — OCW & Automation

- **Estimated Duration:** 2 months
- **FTE:** 2
- **Costs:** 15,000 USD

| Number | Deliverable | Specification |
| -----: | ----------- | ------------- |
| **0a.** | Dockerfile | Dockerize the application |
| **0b.** | Docker Compose | A Compose configuration for running the parachain and its dependencies |
| **0c.** | Docker Documentation | Document the full Docker workflow, including build, run, logs, and network setup for local and CI environments. |
| **0d.** | Docker Testing Guide |Provide a test guide for validating the Dockerized parachain, including integration and networking checks. |
| 0e. | Article | Blog post explaining the architecture and use cases. |
| 1. | OCW | Improve and make robust Off-Chain Worker (OCW) logic for automatic job execution and verification. |
| 2. | Onboard Parachains | Onboard other parachains via XCM and add additional functionality if needed based on survey results. |
| 3. | Security | Slashing mechanism for dishonest workers and reputation system. |
| 4. | Unit Tests | Expand and strengthen the unit test suite to improve reliability and coverage. |

## Future Plans

- Mainnet deployment as a parachain.
- Expansion of job types (e.g., more complex ML inference).
- Integration with more parachains.

## Referral Program (optional) :moneybag:

- **Referrer:** kegan
- **Payment Address:** X

## Additional Information :heavy_plus_sign:

Here you can also add any additional information that you think is relevant to this application but isn't part of it already, such as:

- This project was 1st place in "Build Resilient Apps with Polkadot Cloud" Hackathon.
