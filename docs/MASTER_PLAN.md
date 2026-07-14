# Moolank 100 Master Plan

## Product promise

Moolank helps explain natural patterns. Bhagyank helps explain long-term direction. The Sadhana Path combines both with present-life questionnaire responses to produce a practical transformation roadmap.

## User journey

1. User enters date of birth.
2. App calculates Moolank and Bhagyank.
3. App presents a clear foundation profile.
4. User answers a focused questionnaire about current patterns and goals.
5. System identifies balanced areas and development priorities.
6. System assembles a Sadhana Path from approved practices.
7. User tracks actions, reflections and review checkpoints.

## Database layers

### Layer A — Moolank profiles

Nine foundation records, one for each Moolank from 1 to 9.

Required sections:

- core identity
- strengths
- conditional shadow patterns
- thinking and decision style
- emotional style
- communication
- relationships
- work and career
- money and resources
- stress response
- growth needs
- sadhana themes
- tradition evidence
- scientific boundary note
- safety note

### Layer B — Bhagyank profiles

Nine foundation records, one for each Bhagyank from 1 to 9.

Required sections:

- life direction
- core lessons
- opportunities
- long-term challenges
- relationship lessons
- work and contribution direction
- growth milestones
- sadhana themes
- evidence and safety fields

### Layer C — Moolank–Bhagyank combinations

Eighty-one records covering all 9 × 9 combinations.

Each record should describe:

- natural pattern and life-direction interaction
- reinforcing themes
- possible tensions
- balanced expression
- transformation priority
- useful questions
- practice categories

### Layer D — Questionnaire

The questionnaire measures current expression, not identity or diagnosis.

Initial dimensions:

1. self-direction
2. emotional regulation
3. communication
4. relationship reciprocity
5. confidence and self-worth
6. discipline and consistency
7. decision-making
8. control and flexibility
9. purpose and motivation
10. stress and recovery

Result bands:

- balanced area
- development area
- high-priority growth area

### Layer E — Sadhana library

Every practice record must include:

- practice ID
- title
- target dimension
- purpose
- daily or weekly format
- instructions
- duration
- difficulty
- suitability conditions
- stop or review conditions
- progress indicator
- safety note

### Layer F — Transformation rules

Rules combine:

- Moolank themes
- Bhagyank themes
- combination themes
- questionnaire dimension scores
- user-selected goal
- risk and suitability flags

The output must remain transparent and explain why each practice was selected.

## Delivery strategy

Use breadth-first development:

1. Lock schemas and editorial rules.
2. Build all nine Moolank foundation profiles.
3. Build all nine Bhagyank foundation profiles.
4. Build concise versions of all 81 combinations.
5. Build questionnaire and practice library.
6. Build transformation rules.
7. Integrate with the app.
8. Deepen evidence and content after the full foundation exists.

## Non-goals for foundation phase

- no diagnosis
- no guaranteed future prediction
- no universal personality labels
- no endless micro-trait roadmap before Moolank 1–9 coverage
- no remedies presented as medical treatment
- no hidden AI-only scoring logic

## Source policy

Traditional sources document numerology interpretations. Psychology and behavioural science may define constructs, boundaries and safe practices, but do not validate birth-number prediction.

## Repository relationship

- `moolank_100`: canonical database and transformation knowledge.
- `moolank99`: existing app and historical research reference.

No old IDs or files will be copied blindly. Only reviewed content will be migrated into the new schema.
