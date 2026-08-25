# SE-Lab1-Freelance-Escrow-Platform

 

**Lab-1:**  Requirements Engineering & UML Use-Case Modelling

 
## Problem Context
 
A freelance contract management system allowing creators and sponsors to define deliverable
milestones, review watermarked draft assets, and trigger secure milestone payment releases.

## Deliverables
 
| Deliverable | File |
|---|---|
| Requirements Table (5 FRs + 2 NFRs) | [`requirements/Requirements_Table.docx`](requirements/Requirements_Table.docx) |
| UML Use-Case Diagram | [`diagrams/UseCase_Diagram.pdf`](diagrams/UseCase_Diagram.pdf) |
| Use-Case Flow Specification | [`use-case-flow/UseCase_Flow.docx`](use-case-flow/UseCase_Flow.docx) |
| Original Problem Statement (reference) | [`problem-statement/PS53_Freelance_Content_Creator_Escrow_Platform.pdf`](problem-statement/PS53_Freelance_Content_Creator_Escrow_Platform.pdf) |
 
## Actors
 
- **Content Creator** 
- **Client Sponsor** 
- **Payment Gateway** *(external system)* 
- **Escrow Moderator** 

## Use Cases
 
| ID | Use Case | Relationship |
|---|---|---|
| UC-01 | Define Milestone Contract | — |
| UC-02 | Submit Draft Deliverable | includes UC-03 |
| UC-03 | Apply Watermark | «include» of UC-02 |
| UC-04 | Review & Approve Draft | — |
| UC-05 | Request Revision | «extend» of UC-04 |
| UC-06 | Release Milestone Payment | includes UC-07 |
| UC-07 | Process Payment Transaction | «include» of UC-06 |
| UC-08 | Raise Dispute | «extend» of UC-04 |
 
## Requirements Summary
 
| Req ID | Type | Priority | Summary |
|---|---|---|---|
| FR-001 | Functional | High | Submit drafts for review; release locked payments on sponsor sign-off |
| FR-002 | Functional | High | Jointly define milestone contract (deliverable, due date, escrow amount) |
| FR-003 | Functional | High | Auto-apply watermark to draft media before sponsor review |
| FR-004 | Functional | Medium | Sponsor can reject with comments, reverting milestone to "Pending Revision" |
| FR-005 | Functional | Medium | Either party can raise a dispute after two rejections, routed to moderator |
| NFR-001 | Nonfunctional (Performance & Security) | High | Watermarking completes in under 5 seconds |
| NFR-002 | Nonfunctional (Security) | High | Encrypted escrow wallet + immutable audit log for every fund movement |
 
Full details, acceptance criteria, and rationale for each requirement are in
[`requirements/Requirements_Table.docx`](requirements/Requirements_Table.docx).
 
## Repo Structure
 
```
SE-Lab1-Freelance-Escrow-Platform/
├── README.md
├── problem-statement/
│   └── PS53_Freelance_Content_Creator_Escrow_Platform.pdf
├── requirements/
│   └── Requirements_Table.docx
├── diagrams/
│   └── UseCase_Diagram.pdf
├── use-case-flow/
│   └── UseCase_Flow.docx
└── LICENSE
```
 
