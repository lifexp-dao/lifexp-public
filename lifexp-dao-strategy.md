## LifeXP DAO Strategy & Legal Model (DRAFT)

### 1. What is the LifeXP DAO?
- The LifeXP DAO is a decentralized governance mechanism for the LifeXP ecosystem.
- It enables collective decision-making over experience validation, minting policies, treasury allocation, and platform evolution.

### 2. Governance Scope
- **Token Issuance**: Rules and eligibility for XP minting
- **Verification Logic**: Who can verify XP, and how trust is enforced
- **Treasury Allocation**: Use of community funds (grants, bounties, campaigns)
- **Protocol Evolution**: Updates to XPToken contract, metadata standards, or platform integrations

### 3. Membership & Participation
- **LifeXPers**: Token recipients; can vote on public proposals and engage in DAO discussions
- **Providers**: Verified issuers; may have elevated rights around minting and verification
- **Core Contributors**: Initial builders and maintainers of the platform
- **DAO Tokens / Voting Rights**: To be defined — may be based on XP accumulation, provider status, or separate governance token

### 4. Legal Structure Options
| Model | Jurisdiction | Description |
|-------|--------------|-------------|
| **DAO LLC** | Wyoming (USA) | Limited liability company with DAO operating agreement, recognized under state law |
| **Unincorporated Nonprofit Assoc.** | TN, VT (USA) | Lightweight structure for community DAOs; no corporate status but limited liability |
| **Foundation** | Cayman, Switzerland | Independent legal entity for protocol DAOs; suitable for large ecosystems |
| **Hybrid (LLC + DAO)** | Any | A traditional company holds IP and operates the platform; DAO governs token-based decisions |

### 5. Phase 1

- Draft DAO terms and governance framework in parallel
  - Treasury rules, proposal flow, membership definitions
  - Use multisig or Snapshot for early governance

### 6. DAO Treasury Framework
- **Sources**:
  - Provider onboarding fees
  - Donations or grants
  - % of future revenue (e.g. insights API access)
- **Uses**:
  - Public goods (docs, templates, infrastructure)
  - Provider support & XP verification campaigns
  - Grants for integrations, community tools, research

### 7. DAO Governance Model (Draft)
- **Proposal Creation**: Anyone with verified XP or provider status can submit
- **Voting**: Flat vote per address (or XP-based weighting)
- **Execution**: Multisig or smart contract-driven actions
- **Upgradability**: DAO controls major changes via governance proposals

### 8. Governance Token Strategy
#### MVP Phase: XP-Based Voting
- Start with governance based on **XPToken** ownership
  - 1 XP = 1 vote (optionally doubled for verified tokens)
  - Easy to implement using Snapshot or off-chain delegation

#### Future Phase: Introduce `LXP` Token
- Create a **fungible ERC-20-style governance token**
  - Distributed based on XP accumulation, provider participation, or grants
  - Used for on-chain voting, staking, or access to premium DAO features
- Advantages:
  - Flexible delegation and tooling
  - Clear separation between experience (XPToken) and governance (LXP)
  - Potential integration with funding, reputation, and incentives

### 9. Snapshot Voting Integration
- **Tool**: Snapshot.org enables gasless, off-chain voting for DAO members
- **Strategy Options**:
  - `erc721-balance-of`: 1 vote per XPToken held
  - `weighted-nft`: Verified XP = 2 votes, others = 1
  - Delegation and quorum rules are customizable
- **Eligibility**: Only wallets holding XPToken are allowed to vote or propose
- **Proposal Types**:
  - Feature rollouts (e.g. new category)
  - Treasury decisions (e.g. grants, campaigns)
  - Governance updates (e.g. verification rules)
- **Execution**:
  - Manual action by DAO multisig for MVP
  - Future upgrade path to on-chain execution via smart contracts
- **Setup Steps**:
  1. Deploy XPToken to mainnet or a supported L2
  2. Register a Snapshot Space (requires ENS domain)
  3. Configure strategy and access rules

### 10. Proposal Template (MVP)
To streamline DAO decisions, proposals should follow a lightweight, transparent format:

**Title:** [Short, clear title for the proposal]

**Summary:**
- What is being proposed?
- Why is this important for LifeXP?

**Details:**
- Description of the change, funding, or initiative
- Who it impacts and how
- Implementation steps or timeline

**Requested Action:**
- Approve / Reject
- Vote options (Yes / No / Abstain)

**Eligibility:**
- Who can vote (e.g. any wallet with XPToken)
- Minimum quorum or participation threshold (if applicable)

Optional:
- **Budget Requested** (if applicable)
- **Supporting Links** (docs, GitHub, etc.)

### 11. Proposal Example
**Title:** Enable Snapshot-Based Voting for DAO Decisions

**Summary:**
This proposal recommends launching the official LifeXP DAO voting space on Snapshot using XPToken-based voting. It outlines the initial configuration and eligibility rules to support decentralized governance.

**Details:**
- **What:** Create a LifeXP Snapshot Space with the `weighted-nft` strategy:
  - 1 vote per XPToken
  - 2 votes per Verified XPToken
- **Why:** Enables DAO members to vote on feature rollouts, funding decisions, and protocol changes without needing gas or on-chain interaction.
- **How:** Core contributors will:
  - Register `lifexp.eth` ENS (or subdomain)
  - Deploy XPToken to mainnet or supported L2
  - Configure Snapshot strategy and permissions
  - Publish onboarding instructions for LifeXPers and Providers

**Requested Action:**
Approve the creation of a Snapshot space and authorize the DAO multisig to configure voting rules.

- **Vote Options:** Yes / No / Abstain

**Eligibility:**
Any wallet holding at least 1 XPToken is eligible to vote.

**Quorum:** Minimum 10 XPToken holders participating

**Supporting Links:**
- [Snapshot Docs](https://docs.snapshot.org/)
- [Proposed Strategy Code](https://github.com/snapshot-labs/snapshot-strategies)

### 12. Long-Term Vision
- A sustainable DAO that stewards LifeXP's mission:
  - To recognize and elevate real human experience
  - To build an interoperable, reputation-driven experience graph
  - To empower providers and LifeXPers alike

### 13. Provider Onboarding Rules (Draft)
The LifeXP DAO will define and govern the process by which individuals or organizations become recognized Providers (i.e., issuers of XP tokens).

#### Goals:
- Ensure trusted issuance of XP without central gatekeeping
- Support diverse types of providers (solo creators, orgs, communities)
- Make onboarding transparent, inclusive, and verifiable

#### Onboarding Path (MVP Phase):
1. **Provider Application Form:**
   - Name, logo/image, description
   - Website or social links
   - Wallet address
   - Category focus (e.g. wellness, learning, civic engagement)

2. **DAO Review:**
   - Applications visible in a public dashboard
   - Core contributors or DAO members may vet applications initially
   - Optionally, voting on onboarding can happen via Snapshot

3. **Approval & Listing:**
   - Approved providers appear in the public directory
   - Gain access to `/provider-mint` functionality

4. **Revocation / Reassessment:**
   - DAO can vote to pause or remove providers who breach guidelines or issue spam XP
   - Verification score or reputation metrics may evolve in future

#### Future Enhancements:
- Use XPToken issuance history as a reputation signal
- Enable peer referrals or endorsements
- Add community-based flagging or challenge system

### 14. Sample Provider Onboarding Proposal
**Title:** Approve [Prospective Provider Name] for Provider Status

**Summary:**
This proposal seeks to approve [Provider Name] as a verified XP Provider within the LifeXP ecosystem. The provider has submitted a valid application and aligns with LifeXP’s mission and onboarding criteria.

**Details:**
- **Applicant Name:** [Provider Name]
- **Wallet Address:** [0x...]
- **Website/Socials:** [link]
- **Category Focus:** [e.g. outdoor adventures, creative education]
- **Why This Provider:** [Brief reasoning — e.g., history of impact, community trust, new niche represented]

If approved, the provider will:
- Be listed in the LifeXP Provider Directory
- Gain access to `/provider-mint` functionality
- Be subject to DAO-level rules on verification and XP issuance

**Requested Action:**
Approve this provider for onboarding

**Vote Options:** Yes / No / Abstain

**Eligibility:**
Wallets holding at least 1 XPToken

**Quorum:** Minimum 10 voters

**Supporting Links:**
- [Provider Application Dashboard](#)
- [Provider Website](#)

---
This strategy evolves as the community grows. MVP governance can start lightweight and become more formalized as adoption increases.

### 15. Sample Provider Revocation Proposal
**Title:** Revoke Provider Status for [Provider Name]

**Summary:**
This proposal seeks to revoke the provider status of [Provider Name] based on evidence of spam issuance, violation of DAO guidelines, or community concerns.

**Details:**
- **Provider Name:** [Provider Name]
- **Wallet Address:** [0x...]
- **Reason for Revocation:**
  - [e.g. Issued large volumes of unverified XP]
  - [e.g. Repeated community flags for inauthentic activity]
- **Previous Warnings or Reviews (if any):** [Brief description or link to related governance discussion]

If approved, the provider will:
- Be removed from the public Provider Directory
- Lose access to XP minting functionality
- Be subject to reassessment before any future reinstatement

**Requested Action:**
Revoke provider status for [Provider Name]

**Vote Options:** Yes / No / Abstain

**Eligibility:**
Wallets holding at least 1 XPToken

**Quorum:** Minimum 10 voters

**Supporting Links:**
- [Provider History or Verification Dashboard](#)
- [Related Proposal or Report](#)

