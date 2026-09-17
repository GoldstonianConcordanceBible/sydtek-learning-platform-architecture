# SYDTEK LEARNING PLATFORM ARCHITECTURE
## 05 — SYDTEK LEARNING GRAPH

**Version:** 1.0  
**Status:** CANONICAL — LOCKED FOR INITIAL BUILD

---

# PURPOSE

This document defines the canonical SydTek Learning Graph.

The Learning Graph is the structured relationship between:

- learners
- skills
- competencies
- content
- lessons
- modules
- courses
- programs
- assessments
- artifacts
- case studies
- challenges
- credentials
- employers
- institutions
- research

The Learning Graph transforms SydTek from a catalog of content into a structured learning system.

---

# CORE PRINCIPLE

## CONTENT IS NOT THE MOAT.

Structured relationships between:

**CONTENT  
→ SKILL  
→ PRACTICE  
→ EVIDENCE  
→ COMPETENCY  
→ CREDENTIAL  
→ OUTCOME**

create the strategic infrastructure.

---

# THE CORE GRAPH

The foundational SydTek graph is:

**LEARNER**

↓

**LEARNING GOAL**

↓

**PROGRAM**

↓

**COURSE**

↓

**MODULE**

↓

**LESSON**

↓

**SKILL**

↓

**PRACTICE**

↓

**ASSESSMENT**

↓

**ARTIFACT**

↓

**COMPETENCY**

↓

**CREDENTIAL**

↓

**PORTFOLIO**

↓

**OUTCOME**

---

# CORE ENTITIES

The SydTek Learning Graph should eventually contain at least the following entity types:

1. Learner
2. Learning Goal
3. Program
4. Course
5. Module
6. Lesson
7. Skill
8. Competency
9. Content Object
10. Assessment
11. Artifact
12. Case Study
13. Challenge
14. Credential
15. Portfolio
16. Instructor
17. Organization
18. Employer
19. Institution
20. Research Object

---

# 1. LEARNER

A learner is the primary human entity in the system.

Recommended learner fields:

- learner ID
- name
- email
- registration date
- learning goals
- interests
- active programs
- active courses
- completed courses
- competencies
- credentials
- artifacts
- challenges
- portfolio
- consent/privacy status
- institutional affiliation where applicable

---

# LEARNER ID

Each learner should eventually have a persistent internal identifier.

Example:

`LRN-000001`

The identifier should remain stable even if:

- email changes
- platform changes
- Skool changes
- LMS changes
- subscription status changes

---

# 2. LEARNING GOAL

A learning goal captures what the learner is trying to accomplish.

Examples:

- use AI at work
- become an AI automation consultant
- understand financial markets
- learn options
- build a publishing company
- learn grant writing
- understand Web4
- launch AI-assisted music

A learner may have multiple goals.

---

# GOAL RELATIONSHIP

**LEARNER  
→ HAS GOAL  
→ LEARNING GOAL**

The goal can connect to:

- skills
- courses
- credentials
- pathways
- challenges

This is a key input for future SydTek ONE recommendations.

---

# 3. PROGRAM

A program is a structured academic domain.

Examples:

- SYD-AI
- SYD-MKT
- SYD-W4
- SYD-SCM
- SYD-SUS
- SYD-GRT
- SYD-AIM
- DES

Recommended fields:

- program ID
- program title
- description
- academic owner
- level structure
- required courses
- electives
- credentials
- version
- status

---

# PROGRAM RELATIONSHIP

**PROGRAM  
→ CONTAINS  
→ COURSE**

A course may belong to more than one program through cross-listing.

---

# 4. COURSE

A course is a coherent learning experience with defined outcomes.

Recommended fields:

- course ID
- title
- program
- level
- description
- learning outcomes
- prerequisites
- price
- free/paid status
- course status
- modules
- assessments
- capstone
- credential mapping
- version
- institutional readiness
- course owner

---

# COURSE RELATIONSHIPS

A course may:

- belong to a program
- teach skills
- assess competencies
- contain modules
- use content objects
- contain case studies
- produce artifacts
- qualify toward credentials
- connect to challenges

---

# COURSE GRAPH

**COURSE  
→ TEACHES  
→ SKILL**

**COURSE  
→ CONTAINS  
→ MODULE**

**COURSE  
→ USES  
→ CONTENT OBJECT**

**COURSE  
→ REQUIRES  
→ ASSESSMENT**

**COURSE  
→ PRODUCES  
→ ARTIFACT**

**COURSE  
→ CONTRIBUTES TO  
→ CREDENTIAL**

---

# 5. MODULE

A module is a coherent course section.

Recommended fields:

- module ID
- course ID
- title
- module outcome
- lesson sequence
- deliverables
- progression statement

Example:

`SYD-MKT-000-M04`

---

# MODULE RELATIONSHIP

**COURSE  
→ CONTAINS  
→ MODULE**

**MODULE  
→ CONTAINS  
→ LESSON**

---

# 6. LESSON

A lesson is the smallest formal instructional unit.

Recommended fields:

- lesson ID
- title
- module ID
- lesson objective
- topics
- content objects
- practice
- output
- assessment relationship
- estimated duration

Example:

`SYD-MKT-000-M04-L35`

---

# LESSON STANDARD

A mature lesson should increasingly connect:

**CONCEPT  
→ EXAMPLE  
→ PRACTICE  
→ OUTPUT**

---

# 7. SKILL

A skill represents a specific capability that can be taught and practiced.

Examples:

- identify support and resistance
- write an effective AI prompt
- calculate position size
- identify a qualified grant opportunity
- create a wallet
- map a supply-chain process
- build an automation

---

# SKILL ID

Recommended format:

`SKL-[DOMAIN]-[NUMBER]`

Examples:

`SKL-MKT-001`

`SKL-AI-014`

`SKL-GRT-008`

---

# SKILL RELATIONSHIPS

A skill may be:

- introduced by a lesson
- practiced in an assignment
- assessed by an assessment
- demonstrated in an artifact
- required by a competency
- required by a credential

---

# SKILL GRAPH

**LESSON  
→ INTRODUCES  
→ SKILL**

**ASSIGNMENT  
→ PRACTICES  
→ SKILL**

**ASSESSMENT  
→ EVALUATES  
→ SKILL**

**ARTIFACT  
→ DEMONSTRATES  
→ SKILL**

---

# 8. COMPETENCY

A competency is a broader demonstrated capability composed of one or more skills.

Example:

## FINANCIAL MARKET RISK MANAGEMENT

May include:

- position sizing
- stop placement
- risk/reward analysis
- drawdown limits
- leverage awareness
- trade review

---

# COMPETENCY ID

Recommended format:

`CMP-[DOMAIN]-[NUMBER]`

Example:

`CMP-MKT-004`

---

# SKILL VS. COMPETENCY

A skill may be:

> Calculate position size.

A competency may be:

> Build and apply a complete risk-management framework.

Competencies should represent integrated capability.

---

# COMPETENCY STATES

Recommended learner competency states:

- NOT STARTED
- INTRODUCED
- PRACTICED
- DEMONSTRATED
- MASTERED
- REVIEW DUE

These states should not be assigned casually.

---

# MASTERY RULE

## COURSE COMPLETION ≠ COMPETENCY MASTERY.

Mastery should require defined evidence.

---

# 9. CONTENT OBJECT

A content object is any reusable instructional or evidence asset.

Examples:

- YouTube video
- short-form video
- lecture
- PDF
- article
- book chapter
- image
- spreadsheet
- dataset
- recording
- code repository
- podcast
- transcript
- field recording
- research report

---

# CONTENT ID

Recommended format:

`CNT-[YEAR]-[NUMBER]`

Example:

`CNT-2026-004231`

A stable content ID prevents dependence on filenames or platform URLs.

---

# CONTENT METADATA

Each important content object should eventually include:

- content ID
- title
- creator
- creation date
- source platform
- source URL
- format
- duration
- transcript
- description
- keywords
- rights status
- public/paid status
- evidence classification
- program mappings
- course mappings
- lesson mappings
- skill mappings
- case mappings
- version

---

# ONE CONTENT OBJECT, MANY USES

A single public video may support:

- one AI course
- one entrepreneurship course
- one case study
- one research project

The video should not be duplicated solely because multiple courses use it.

Instead:

**ONE CONTENT OBJECT  
→ MULTIPLE GRAPH RELATIONSHIPS**

---

# 10. ASSESSMENT

An assessment evaluates learning.

Types may include:

- quiz
- written assignment
- project
- simulation
- oral assessment
- code exercise
- portfolio review
- case analysis
- capstone

---

# ASSESSMENT ID

Recommended format:

`ASM-[COURSE]-[NUMBER]`

Example:

`ASM-SYD-MKT-150-003`

---

# ASSESSMENT METADATA

Include:

- assessment ID
- course
- competency
- skills assessed
- instructions
- rubric
- passing standard
- submission format
- attempt policy
- AI-use policy
- reviewer
- version

---

# ASSESSMENT RELATIONSHIP

**ASSESSMENT  
→ EVALUATES  
→ SKILL / COMPETENCY**

---

# 11. ARTIFACT

An artifact is learner-produced evidence.

Examples:

- workflow
- trade plan
- market analysis
- grant matrix
- code
- report
- presentation
- song
- research paper
- business plan
- process map
- portfolio
- capstone

---

# ARTIFACT ID

Recommended format:

`ART-[LEARNER]-[NUMBER]`

Example:

`ART-LRN-000001-0021`

---

# ARTIFACT METADATA

Include:

- artifact ID
- learner ID
- course ID
- assignment
- creation date
- version
- skills demonstrated
- competency mapping
- assessment result
- verification status
- portfolio visibility
- privacy status

---

# ARTIFACT PRINCIPLE

## THE ARTIFACT IS THE BRIDGE BETWEEN LEARNING AND PROOF.

---

# 12. CASE STUDY

Case studies convert real or historical activity into structured learning.

Recommended fields:

- case ID
- title
- date
- program
- people/organizations
- context
- thesis
- action
- evidence
- outcome
- uncertainty
- lesson
- source material

---

# CASE ID

Recommended format:

`CASE-[PROGRAM]-[NUMBER]`

Examples:

`CASE-MKT-001`

`CASE-AI-001`

`CASE-W4-001`

---

# CASE STANDARD

Preserve:

**CONTEXT  
→ THESIS  
→ COUNTER-THESIS  
→ ACTION  
→ RESULT  
→ EVIDENCE  
→ LESSON**

Do not rewrite historical cases to make the outcome appear inevitable.

---

# MARKET CASE STANDARD

For financial-market cases:

**TIMESTAMP  
→ CONTEXT  
→ THESIS  
→ COUNTER-THESIS  
→ INSTRUMENT  
→ ENTRY  
→ SIZE  
→ STOP  
→ TARGET  
→ ACTION  
→ RESULT  
→ EVIDENCE  
→ LESSON**

Wins, losses, and no-trades all remain in the record.

---

# 13. CHALLENGE

A challenge is an applied learning event.

Examples:

- AI automation competition
- market simulation
- grant research challenge
- supply-chain optimization
- sustainability challenge
- Web4 design challenge
- creator challenge

---

# CHALLENGE ID

Recommended format:

`CHL-[DOMAIN]-[NUMBER]`

Example:

`CHL-AI-001`

---

# CHALLENGE METADATA

Include:

- challenge ID
- title
- problem
- sponsor
- rules
- eligibility
- dataset
- timeline
- evaluation rubric
- evidence
- leaderboard
- winners
- learning objectives
- associated courses
- associated competencies

---

# CHALLENGE RELATIONSHIP

**CHALLENGE  
→ APPLIES  
→ COMPETENCY**

**LEARNER  
→ PARTICIPATES IN  
→ CHALLENGE**

**CHALLENGE  
→ PRODUCES  
→ ARTIFACT**

---

# 14. CREDENTIAL

A credential represents verified completion or competency.

Credential types:

- course completion
- badge
- micro-credential
- foundational certificate
- advanced certificate
- professional certificate
- continuing education record
- partner-recognized credential

---

# CREDENTIAL ID

Recommended format:

`CRD-[PROGRAM]-[NUMBER]`

Example:

`CRD-AI-001`

---

# CREDENTIAL METADATA

Include:

- credential ID
- credential name
- issuing entity
- requirements
- courses
- competencies
- assessments
- capstone
- version
- issue rules
- expiration/review if applicable

---

# CREDENTIAL INSTANCE

The credential definition and learner award are different entities.

Example:

**Credential definition:**  
`CRD-AI-001`

**Learner credential record:**  
`AWD-LRN-000001-CRD-AI-001`

This distinction supports verification.

---

# 15. PORTFOLIO

A portfolio is a curated collection of learner evidence.

Potential portfolio components:

- best artifacts
- capstones
- credentials
- challenge results
- research
- project summaries
- verified outcomes

---

# PORTFOLIO RELATIONSHIP

**LEARNER  
→ OWNS  
→ PORTFOLIO**

**PORTFOLIO  
→ CONTAINS  
→ ARTIFACT**

---

# PORTFOLIO PRINCIPLE

A transcript says:

> What did you take?

A portfolio should answer:

> What can you show?

SydTek should eventually support both.

---

# 16. INSTRUCTOR

Instructor metadata may include:

- instructor ID
- name
- role
- courses
- credentials
- expertise
- content rights
- institutional status

---

# INSTRUCTOR RELATIONSHIP

**INSTRUCTOR  
→ TEACHES / REVIEWS  
→ COURSE**

**INSTRUCTOR  
→ CREATES  
→ CONTENT**

**INSTRUCTOR  
→ EVALUATES  
→ ASSESSMENT**

---

# 17. ORGANIZATION

Organization is a broad entity for:

- businesses
- nonprofits
- government agencies
- research groups
- sponsors
- technology partners
- community organizations

---

# ORGANIZATION RELATIONSHIPS

An organization may:

- sponsor a challenge
- employ learners
- purchase Enterprise
- license curriculum
- provide a case
- support research

---

# 18. EMPLOYER

Employer relationships may connect:

**EMPLOYER  
→ REQUIRES  
→ COMPETENCY**

**EMPLOYER  
→ SPONSORS  
→ CHALLENGE**

**EMPLOYER  
→ HIRES  
→ LEARNER**

Long-term, this creates demand-side information for curriculum development.

---

# EMPLOYER SIGNAL

SydTek may eventually identify:

> Which competencies are repeatedly requested by employers?

That information may influence course development.

Employer demand should inform, not solely dictate, academic standards.

---

# 19. INSTITUTION

Institution represents:

- college
- university
- school
- continuing-education provider
- academic partner

---

# INSTITUTION RELATIONSHIPS

An institution may:

- license courseware
- accept a course
- award credit
- co-develop curriculum
- enroll learners
- recognize credentials
- conduct research

---

# CREDIT RELATIONSHIP

Do not model:

**COURSE = COLLEGE CREDIT**

unless formally true.

Instead model explicitly:

**INSTITUTION  
→ ACCEPTS COURSE  
→ FOR SPECIFIED CREDIT / REQUIREMENT**

This relationship may include:

- institution
- course
- effective date
- expiration/review date
- credit amount
- requirement satisfied
- agreement source

---

# 20. RESEARCH OBJECT

Research objects may include:

- research question
- dataset
- working paper
- manuscript
- peer-reviewed publication
- field note
- experiment
- technical report

---

# RESEARCH ID

Recommended:

`RES-[YEAR]-[NUMBER]`

---

# RESEARCH RELATIONSHIP

**RESEARCH  
→ PRODUCES  
→ EVIDENCE**

**RESEARCH  
→ SUPPORTS  
→ CASE**

**RESEARCH  
→ UPDATES  
→ COURSE**

**COURSE  
→ GENERATES QUESTIONS FOR  
→ RESEARCH**

This creates a closed research-learning loop.

---

# GRAPH RELATION TYPES

Canonical relationship verbs should remain consistent.

Recommended relationships:

- CONTAINS
- BELONGS TO
- TEACHES
- INTRODUCES
- PRACTICES
- EVALUATES
- DEMONSTRATES
- REQUIRES
- CONTRIBUTES TO
- COMPLETES
- EARNS
- PRODUCES
- USES
- MAPS TO
- ACCEPTS
- SPONSORS
- EMPLOYS
- CREATES
- REVIEWS
- UPDATES

Consistent verbs improve machine readability.

---

# THE THREE STRATEGIC GRAPHS

The long-term platform can be understood as three interconnected graphs.

## 1. CURRICULUM GRAPH

**CONTENT  
→ LESSON  
→ COURSE  
→ SKILL  
→ COMPETENCY  
→ CREDENTIAL**

---

## 2. LEARNER GRAPH

**LEARNER  
→ GOAL  
→ COURSE  
→ ATTEMPT  
→ ARTIFACT  
→ COMPETENCY  
→ CREDENTIAL**

---

## 3. EVIDENCE GRAPH

**CLAIM  
→ SOURCE  
→ CASE  
→ ARTIFACT  
→ ASSESSMENT  
→ VERIFICATION**

SydTek ONE eventually operates across all three.

---

# KNOWLEDGE GRAPH PRINCIPLE

The graph should answer questions such as:

> Which videos teach position sizing?

> Which courses require AI workflow mapping?

> Which learners have demonstrated a specific skill?

> What evidence supports a learner credential?

> Which courses are accepted by a specific institution?

> Which cases are used in three or more programs?

> Which content is outdated?

> Which employer challenges map to which competencies?

---

# CONTENT INGESTION PIPELINE

For the existing SydTek content corpus:

**DISCOVER ASSET**

↓

**ASSIGN CONTENT ID**

↓

**CAPTURE METADATA**

↓

**TRANSCRIPT / SUMMARY**

↓

**MAP SUBJECT**

↓

**MAP SKILLS**

↓

**MAP COURSES**

↓

**MAP CASES**

↓

**CLASSIFY RIGHTS**

↓

**CLASSIFY EVIDENCE**

↓

**PUBLISH RELATIONSHIPS**

---

# DO NOT INGEST EVERYTHING AT ONCE

Priority order:

## PRIORITY 1

Content already used in live courses.

## PRIORITY 2

Content required for courses currently being built.

## PRIORITY 3

High-performing public content.

## PRIORITY 4

Important historical case evidence.

## PRIORITY 5

Remaining archive.

This prevents metadata work from blocking student delivery.

---

# EVIDENCE CLASSIFICATION

Recommended evidence classifications:

- VERIFIED EXTERNAL
- PARTNER CORROBORATED
- INSTITUTIONAL RECORD
- ON-CHAIN VERIFIED
- INTERNAL RECORD
- APPLICANT RECORD
- FIELD OBSERVATION
- SELF-REPORTED
- PROPOSED
- FUTURE EXPERIMENT

The classification should describe provenance, not whether the claim is favorable.

---

# SOURCE OF TRUTH

Every major entity should have one canonical record.

Examples:

**ONE COURSE RECORD**

not separate incompatible versions in:

- Skool
- YouTube
- GitHub
- spreadsheet

These platforms may display different views.

The graph maintains canonical identity.

---

# DATA PORTABILITY

The Learning Graph should be designed so SydTek can migrate from one platform to another.

Avoid architecture that depends entirely on proprietary IDs from:

- Skool
- YouTube
- payment processors
- a single AI provider

Store external IDs as relationships.

Do not make them the canonical SydTek ID.

---

# PRIVACY

Not every graph relationship should be public.

Examples:

## PUBLIC

- public course
- public content
- public credential verification with consent
- public case

## RESTRICTED

- learner progress
- assessment scores
- private artifacts
- institutional records
- personal information

The graph architecture must support access controls.

---

# GRAPH VERSIONING

Entities should preserve history.

Example:

`SYD-MKT-150 v1.0`

↓

`SYD-MKT-150 v1.1`

Do not destroy the historical version completed by previous learners.

---

# SUPERSESSION

When a new entity replaces an old entity, use relationships such as:

**SUPERSEDES**

and:

**SUPERSEDED BY**

rather than deleting the historical entity.

---

# LEARNING GRAPH MVP

The first SydTek Learning Graph does not require a sophisticated graph database.

The MVP can begin with structured files or tables containing:

## COURSES

course ID, title, program, version

## CONTENT

content ID, title, source

## SKILLS

skill ID, description

## RELATIONSHIPS

course → teaches → skill

lesson → uses → content

artifact → demonstrates → competency

credential → requires → course

---

# MVP RULE

## STRUCTURE FIRST. SOFTWARE SECOND.

Do not delay graph design while searching for the perfect graph database.

A clean schema can later migrate into:

- relational databases
- graph databases
- vector systems
- AI retrieval systems
- APIs

---

# FUTURE TECHNICAL ARCHITECTURE

Potential future components:

- relational operational database
- graph database
- vector index
- credential registry
- analytics warehouse
- AI retrieval layer
- API gateway

These are implementation decisions.

The canonical entity model should remain portable.

---

# SYDTEK ONE RELATIONSHIP

SydTek ONE can eventually query:

**LEARNER GRAPH**

to understand the learner.

**CURRICULUM GRAPH**

to understand available learning.

**EVIDENCE GRAPH**

to understand demonstrated capability.

Then recommend:

**NEXT BEST LEARNING ACTION**

---

# EXAMPLE — AI

**LRN-000001**

↓

completed

`SYD-AI-101`

↓

demonstrated

`SKL-AI-004 — Prompt Construction`

↓

has not demonstrated

`SKL-AI-021 — Workflow Automation`

↓

SydTek ONE recommends

`SYD-AI-130 — AI Automation at Work`

That is much more useful than:

> Here are 300 courses.

---

# EXAMPLE — FINANCIAL MARKETS

**SYD-MKT-000**

↓

Lesson 26

↓

teaches

`SKL-MKT-026 — Position Sizing`

↓

artifact

`Position-Sizing Exercise`

↓

contributes to competency

`CMP-MKT-004 — Market Risk Management`

↓

required by

`Financial Markets Foundational Credential`

This is the graph.

---

# EXAMPLE — CONTENT REUSE

A single video on a live XLE trade may be mapped to:

**CASE-MKT-002**

↓

used by:

`SYD-MKT-150 — Risk Management`

`SYD-MKT-165 — Profit Taking`

`SYD-MKT-270 — Trading Journal`

`DES-112 — Digital Exchange Systems Laboratory`

One canonical artifact.

Multiple educational relationships.

---

# GRAPH QUALITY METRICS

Track:

- % courses mapped to skills
- % lessons mapped to skills
- % skills with assessments
- % credentials with defined competencies
- % credentials with evidence
- % live courses with complete metadata
- % active content with rights classification
- orphaned content objects
- duplicate entities
- outdated relationships

---

# GRAPH GOVERNANCE

Changes to core schemas should be versioned.

Do not casually rename:

- IDs
- entity types
- relationship types

after production use begins.

Additive changes are preferred over destructive changes.

---

# GRAPH OWNERSHIP

The canonical Learning Graph is a core SydTek asset.

It should remain under SydTek-controlled infrastructure and documented IP ownership.

Third-party platforms may consume or display graph information.

They should not become the sole authoritative repository.

---

# STRATEGIC MOAT

SydTek's long-term defensibility is not:

**WE HAVE VIDEOS.**

It is:

**WE KNOW WHAT EACH ASSET TEACHES,  
WHO LEARNED IT,  
WHAT THEY BUILT,  
WHAT THEY PROVED,  
WHAT THEY SHOULD LEARN NEXT,  
AND HOW THAT CAPABILITY CONNECTS TO CREDENTIALS, EMPLOYERS, AND INSTITUTIONS.**

---

# FINAL LEARNING GRAPH RULE

The SydTek Learning Graph should make every important educational claim traceable.

The ultimate chain is:

**LEARNING CLAIM  
→ CURRICULUM  
→ ACTIVITY  
→ EVIDENCE  
→ ASSESSMENT  
→ COMPETENCY  
→ CREDENTIAL**

Therefore:

# PROVENANCE = SUPPLY CHAIN OF TRUST.

---

# STATUS

**05_SYDTEK_LEARNING_GRAPH.md**

**Version:** 1.0  
**Status:** LOCKED FOR INITIAL ARCHITECTURE BUILD