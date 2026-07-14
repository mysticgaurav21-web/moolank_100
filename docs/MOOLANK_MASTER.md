# Moolank Master Specification

**Version:** 1.0  
**Status:** Foundation lock  
**Scope:** Moolank 1–9 only

## 1. Purpose

This document is the controlling specification for all Moolank foundation profiles in `moolank_100`.

Moolank is treated as a traditional numerology lens for describing possible natural patterns. It is not a scientific personality test, diagnosis, fixed identity or guarantee of behaviour.

The immediate objective is to build nine complete, consistent and app-ready foundation profiles before beginning Bhagyank, combinations or deep trait expansion.

## 2. Calculation rule

Moolank is calculated from the **day of birth only**.

- Dates 1, 10, 19 and 28 reduce to Moolank 1.
- Dates 2, 11, 20 and 29 reduce to Moolank 2.
- Dates 3, 12, 21 and 30 reduce to Moolank 3.
- Dates 4, 13, 22 and 31 reduce to Moolank 4.
- Dates 5, 14 and 23 reduce to Moolank 5.
- Dates 6, 15 and 24 reduce to Moolank 6.
- Dates 7, 16 and 25 reduce to Moolank 7.
- Dates 8, 17 and 26 reduce to Moolank 8.
- Dates 9, 18 and 27 reduce to Moolank 9.

Reduction continues until one digit from 1 to 9 remains. This database does not treat 11, 22 or other master numbers as separate Moolank values in the foundation phase.

## 3. Canonical profile set

The foundation contains exactly nine records:

| Number | Profile ID | Canonical path | Status |
|---|---|---|---|
| 1 | `M-1-FOUNDATION` | `data/moolank/moolank-1.json` | planned |
| 2 | `M-2-FOUNDATION` | `data/moolank/moolank-2.json` | planned |
| 3 | `M-3-FOUNDATION` | `data/moolank/moolank-3.json` | planned |
| 4 | `M-4-FOUNDATION` | `data/moolank/moolank-4.json` | planned |
| 5 | `M-5-FOUNDATION` | `data/moolank/moolank-5.json` | planned |
| 6 | `M-6-FOUNDATION` | `data/moolank/moolank-6.json` | planned |
| 7 | `M-7-FOUNDATION` | `data/moolank/moolank-7.json` | planned |
| 8 | `M-8-FOUNDATION` | `data/moolank/moolank-8.json` | planned |
| 9 | `M-9-FOUNDATION` | `data/moolank/moolank-9.json` | planned |

No profile may use historical `ID-###` or reconstructed micro-trait IDs. Foundation IDs are number-based and permanent.

## 4. Required content domains

Every Moolank profile must contain the same domains in the same structure.

### 4.1 Core identity

A concise traditional summary of the number's central orientation. It must use conditional language and describe a pattern, not a fixed identity.

### 4.2 Strengths

Practical balanced capacities traditionally associated with the number. Strengths must be behavioural and observable, not destiny claims.

### 4.3 Conditional shadows

Possible overextensions or imbalances. Every shadow must include:

- possible triggers;
- protective factors;
- non-universal wording.

A shadow cannot be written as a permanent defect.

### 4.4 Thinking and decisions

How the traditional pattern may influence information processing, judgment, pace, uncertainty and revision.

### 4.5 Emotional style

Possible emotional needs, expression patterns and regulation tendencies. No psychiatric or diagnostic inference is allowed.

### 4.6 Communication style

Possible tone, pace, directness, listening pattern and feedback response.

### 4.7 Relationship style

Possible needs around closeness, space, reciprocity, conflict, appreciation and boundaries.

### 4.8 Work and career

Possible work preferences, contribution style, motivation and team behaviour. It must not prescribe a single profession or guarantee success.

### 4.9 Money and resources

Possible attitudes toward earning, spending, saving, control, security, generosity and risk. It is not financial advice.

### 4.10 Stress response

Possible changes under pressure, plus recovery supports. Stress content must remain non-clinical.

### 4.11 Growth needs

Skills and balancing capacities that can improve expression of the profile.

### 4.12 Sadhana themes

Transformation themes only—not final personalized practices. Each theme should later connect to questionnaire dimensions and approved practice records.

## 5. Standard interpretation model

Every domain should follow this sequence:

1. **Natural orientation** — what the tradition associates with the number.
2. **Balanced expression** — how the tendency can function constructively.
3. **Under-pressure expression** — how it may become less useful in context.
4. **Growth support** — what may help restore balance.

This structure prevents one-sided positive or negative profiles.

## 6. Language rules

Preferred wording:

- may prefer
- may notice
- can be drawn toward
- in a balanced expression
- under pressure
- in some contexts
- may benefit from
- tradition associates

Prohibited wording:

- always
- never
- born leader as fact
- destined to succeed
- naturally superior
- mentally weak
- toxic
- narcissistic
- unstable
- addicted
- criminal
- diseased
- guaranteed wealth, marriage, fame or authority

## 7. Evidence model

Every profile must keep two evidence layers separate.

### 7.1 Traditional support

Records how consistently numerology sources associate a theme with the Moolank.

Allowed grades:

- weak
- weak-moderate
- moderate
- moderate-strong
- strong

### 7.2 Scientific boundary

The fixed field is:

```text
scientificBirthNumberLink: not-established
```

Psychology and behavioural science may define constructs, distinguish healthy and unhealthy expressions, and support safe practices. They do not validate that date-of-birth numbers predict personality or life outcomes.

## 8. Source requirements

A foundation profile should normally include:

- at least two direct Birth Number or Moolank source families where available;
- broader Number-based comparison sources clearly marked as comparison;
- primary or authoritative psychology sources for construct boundaries where relevant;
- explicit source limitations when direct evidence is narrow or repetitive.

Source quantity cannot replace source diversity or relevance.

## 9. Safety locks

A canonical Moolank profile must not:

- diagnose medical, psychiatric or personality conditions;
- infer criminality, addiction or moral worth;
- predict certain future events;
- present spiritual practices as medical treatment;
- treat low scores or shadow patterns as permanent identity;
- use fear-based claims to force engagement;
- recommend financial, legal or medical action from numerology alone.

Questionnaire responses will later measure current expression and development priorities, not prove the profile.

## 10. Sadhana connection

Each Moolank profile may identify broad transformation themes such as:

- self-direction and cooperation;
- emotional regulation;
- communication;
- relationship reciprocity;
- confidence and self-worth;
- discipline and consistency;
- decision-making;
- control and flexibility;
- purpose and motivation;
- stress and recovery.

The Moolank profile alone does not generate a personalized Sadhana Path. Personalization will require Bhagyank, questionnaire responses, selected goals, suitability checks and transparent transformation rules.

## 11. Completion standard for one Moolank

A profile is complete only when:

1. all required schema fields are filled;
2. direct tradition and comparison sources are distinguished;
3. balanced and under-pressure expressions are both present;
4. triggers and protective factors accompany conditional shadows;
5. all prohibited claims are removed;
6. JSON validates against `schemas/moolank-profile.schema.json`;
7. the master index is updated;
8. review status is recorded;
9. the change is merged through a pull request.

## 12. Foundation delivery order

The delivery sequence is:

1. Moolank 1
2. Moolank 2
3. Moolank 3
4. Moolank 4
5. Moolank 5
6. Moolank 6
7. Moolank 7
8. Moolank 8
9. Moolank 9

Each milestone creates one complete profile. Deep trait expansion, compatibility and personalized practices remain deferred until all nine foundation profiles exist.

## 13. Definition of foundation success

The Moolank foundation phase succeeds when the app can receive a number from 1 to 9 and return a complete, consistently structured, evidence-graded and safe profile for every number.
