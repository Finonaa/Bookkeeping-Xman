# How to use this template
Template for repositories for v6 allocators. Please ensure you fill out the Readme file with correct information, within 2 weeks of being accepted as an allocator. Remove the this top header to start with your allocator name
**Once you create your copy of this repository, you MUST install the datacap bot: go to https://github.com/apps/datacap-bot, click the 'Configure' button, and select the bookkeeping repository to install the bot/application.**

# Allocator Bookeeping repository for <Allocator Name>
Xman

## Allocator JSON Link
_put here a link to your allocator json from https://github.com/filecoin-project/Allocator-Registry/tree/main/Allocators_

## Client Dilligence
_**YOU SHOULD HAVE PUT INFO IN THE AIRTABLE FORM, YOU CAN COPY IT HERE**. Describe your pathway's mechanism for verifying your clients and establishing initial trust. How will you mitigate sybil attacks? For example if you are proposing an automated pathway what rate limits or deterministics will you use? If you are working with enterprise or paying clients, how will you verify the authenticity of their data ownership claims? How will you provide evidence and proof to the Governance Team for auditing your client diligence?_

Our pathway employs a multi-layered, "Trust but Verify" approach to establish initial client trust and mitigate Sybil attacks. We combine automated checks with manual review, escalating diligence based on the allocation size and client type.

1. Application Vetting (The First Filter):

Structured Application: All clients must complete our detailed application form , which requires:

Project/Organization Name & Description: A clear, concise explanation of the data's purpose and value.

Verifiable Online Presence: Links to a company website, GitHub repository, professional  profile, or established social media. Anonymous or completely opaque entities are automatically subject to higher scrutiny and lower initial allocation limits.

Data Source Attestation: Clients must declare the origin of the data and affirm they have the rights to store and distribute it.

Previous Storage History: We request Filecoin addresses to check on-chain history for reputable activity.

2. Mitigating Sybil Attacks:

Rate Limiting: A single source IP or email domain cannot submit more than a set number of applications per month (e.g., 2 applications).

Deterministic Allocation Tiers: Initial allocations are strictly capped based on verification level:

1st: max 5% (≤256 TiB)       2nd: 10%       3rd: 15%       4th: 20%    5th and beyond: 25%

No tranche should exceed 2× the size of the previous one.
   
All datasets must be stored in at least two geographic regions.

Maximum of 8 replicas to ensure efficient use of DC.

Cross-Referencing Tools: We utilize community tools like Filfox, Filscan, and Glif Explorer to check the client's provided addresses for patterns indicative of Sybil behavior (e.g., many small, rapid allocations from different notaries to the same miner set).

Unique Data Requirement: We require a Cryptographic Hash (CID) of the dataset prior to allocation. Attempting to receive multiple allocations for the same CID would be a red flag. Receiving allocations for different CIDs from the same client requires justification and escalates the request to a manual review.

3. Verification for Enterprise/Paying Clients:
For entities claiming to be businesses or paid service providers, we require stronger evidence:

Official Documentation: Request a verifiable business registration document (e.g., Certificate of Incorporation) or a professional services invoice.

Domain Verification: The contact email must originate from the organization's official domain.

Video Conference Interview: For very large requests (> 5PiB), we require a brief video call with a project representative to discuss their use case and technical setup.

4. Evidence for Governance Team Audit:
All diligence is meticulously documented. For each client, our internal records (e.g., Airtable base) will contain:

The timestamped original application.

Links to the verified online presence (website, GitHub, etc.).

Notes from any manual review or calls.

The rationale for the approved allocation tier and size.

The client's Filecoin address and the associated CID(s) of the data they pledged to store.
This entire dataset is exportable and will be made available to the Filecoin Foundation Governance Team upon request for any audit.
## Description of Data Diligence
_**YOU SHOULD HAVE PUT INFO IN THE AIRTABLE FORM, YOU CAN COPY IT HERE**. Describe how you will perform data diligence to verify your clients are within program scope. How will you ensure the data meets local & regional legal requirements and the client is the data owner? What types of data sampling will you perform? What tools will you use to confirm the data in deals matches initial client claims? What proof of this diligence can you show the Governance team during an audit?_

Our data diligence process is designed to ensure data is within program scope, legally compliant, and matches client claims before and after deal-making.

1. Verifying Program Scope & Authenticity:

Client Attestation: The application requires a legally binding declaration that the client owns the data or has the right to store it and that it does not violate any laws or Fil+ program rules.

Spot-Check Sampling: For all allocations above 5 TiB, we perform a pre-allocation data spot-check. The client must provide:

A Sample Dataset: A representative subset of the data (e.g., 1-2 GB).

Access to a Download Link: For us to directly retrieve and inspect the data.

Manual Inspection: We manually review the sample for:

Content Matching: Does the data match the description in the application (e.g., satellite imagery, public domain books, sensor data)?

Apparent Legitimacy: Does the data appear to be legitimate and valuable, or is it obviously garbage/auto-generated?

2. Ensuring Legal Compliance:

Geographic Awareness: We maintain a restricted list of countries/regions under international sanctions and will not allocate to clients based in or storing data from those areas.

Prohibited Content: We explicitly forbid the storage of data that is illegal in the client's jurisdiction or common carrier laws, including but not limited to: CSAM, extremist content, and non-consensual intimate imagery. Our application includes a clear acceptance of these terms.

Reporting Mechanism: We have a clear process for third parties to report illegal content stored via an allocation we provided, which we will act upon immediately in coordination with the Filecoin Foundation and legal authorities.

3. Post-Allocation Verification:

CID Commitment Check: Using tools like Filplus.info, Lotus, or Glif, we verify that the client has indeed used the allocated DataCap to make storage deals for the exact CID they specified in their application. Any deviation triggers an immediate inquiry and future allocation freezes.

Retrieval Testing: We periodically perform retrieval tests on a random sample of deals to ensure the data remains available and retrievable, confirming the client is upholding their storage commitments.

4. Evidence for Governance Team Audit:
Proof of our data diligence will be provided to the Governance Team through:

Application Records: Stored client attestations and data descriptions.

Diligence Logs: Notes from our manual spot-checks, including the CID of the sample we downloaded and reviewed.

On-Chain Proof: Links to public block explorers showing the successful storage of the promised CID by the client, proving we verified the outcome.

Audit Trail: A complete log of all our verification actions, timestamped and linked to each client's record.

This rigorous, evidence-based approach ensures we are a responsible and transparent steward of DataCap within the Filecoin Plus ecosystem.
## Short description of pathway for clients
_In your own words why should a client use your allocator? We intend to display this information in [fil.org/filecoin-plus/allocators](https://fil.org/filecoin-plus/allocators), so this is how you can distinguish yourself from other allocators_

Overview This repository serves as the central hub for transparency and operations for [Xman], a dedicated DataCap allocator within the Filecoin Plus (Fil+) ecosystem.

As a Verified Registry Client, we are entrusted with DataCap by the Filecoin Foundation. Our mission is to allocate this resource responsibly to legitimate clients who demonstrate a genuine need to store valuable data on the Filecoin network, thereby fostering its growth and utility.
## Contact info
_How can a client contact you? Give here your Slack ID, emails or whatever contact info you would like to share_

For all inquiries related to DataCap allocation, please use the following channels. This ensures all communication is trackable and transparent.

General Questions & Discussion: Filecoin Slack Channel [Slack ID:Xman]

## Detailed Allocator policies, procedures, and requirements.

Our core principle is to maximize the utility of the Filecoin network by supporting clients storing verifiably useful and unique data.
We prioritize:

Open Datasets: Publicly accessible data for research, science, and public good.

Cultural & Historical Preservation: Archives, libraries, and museums.

Decentralized Applications (dApps): Projects building on or integrating with Filecoin.

New Storage Clients: Clients new to the network who need a bootstrap allocation.

Geographic Diversity: Clients and miners from underrepresented regions.

We generally avoid or scrutinize heavily:

Requests to allocate to a single miner without a justified technical reason.

Requests from anonymous entities without a verifiable track record.

Projects that appear to be solely for financial arbitrage rather than genuine storage.

Data that is illegal, malicious, or violates the Fil+ principles.

Allocation Tiers:

Small Request (＜5TiB): Streamlined review process.

Large Request (> 5 TiB): Requires enhanced due diligence, a public notice period for community feedback, and a clear justification for the large amount.

## Risk mitigation strategies 
_What is the processes for protecting your organization, reputation, and pathway from abuse. For example, what Operational Security (OpSec) standards, user agreements, alerts, or throttling mechanisms will you employ?_ 

We employ a multi-layered strategy to mitigate the risk of DataCap misuse:

Progressive Decentralization: Start with smaller allocations to new clients and increase based on proven, trustworthy usage.

Miner Diversity Requirement: We encourage and often require clients to spread their deals across multiple reputable miners to strengthen network resilience and prevent concentration of trust.

Transparency as a Deterrent: The public nature of our application and decision-making process acts as a strong deterrent against bad actors.

Data Verification: We perform spot checks on stored data to ensure it matches the client's description and remains retrievable.

Notary Oversight: We operate under the guidance and rules set by the Filecoin Foundation and the broader Notary community, incorporating their feedback and alert into our processes.

## Dispute Resolutions 

In the event of a dispute (e.g., a client believes their application was unfairly rejected, or a third party raises a concern about an allocation):

Formal Complaint: The concerned party must submit a formal complaint via a GitHub Issue in this repository using the Dispute template, clearly outlining the grounds for the dispute.

Acknowledgment & Investigation: We will acknowledge the issue within 48 hours and initiate a review of the original application and decision process.

Transparent Discussion: The issue will be discussed transparently within the GitHub thread, allowing all parties to present evidence.

Resolution Proposal: Our team will propose a resolution (e.g., uphold decision, reverse decision, propose a compromise).

Escalation: If the dispute cannot be resolved internally, we will escalate the matter to the Filecoin Foundation or the designated Fil+ governance body for a final ruling. We agree to abide by their decision.

## Compliance Audit Check
_How do you plan to ensure that your clients, and the storage providers they interact with are all in compliance with both program-wide and pathway specific requirements._

To ensure ongoing accountability and adherence to our stated policies, we commit to the following:

Public Ledger: All allocation decisions, including client address, amount, rationale, and associated GitHub issue link, will be recorded in a allocations.csv file in this repository.

Community Audits: We welcome and encourage independent audits from any community member. Findings can be submitted as a GitHub Issue.

Notary Compliance: We will fully comply with any audit requests from the Filecoin Foundation or our designated root key holder.
