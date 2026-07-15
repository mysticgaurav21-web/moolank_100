# M1-R002 — Historical Foundations, Systems and Calculation Rules

## Metadata

- **Record ID:** M1-R002
- **Moolank:** 1
- **Document type:** Historical and calculation foundation
- **Status:** Reviewed research foundation
- **Version:** 1.0.0
- **Repository:** `mysticgaurav21-web/moolank_100`
- **Scientific birth-number link:** Not established

## 1. Purpose

This record defines what the app means by **Moolank 1**, how it is calculated, which historical traditions are relevant, and which claims must remain separated.

The operational rule is intentionally narrow: Moolank is a modern numerology category calculated from the calendar day of birth. Historical number symbolism, Pythagorean philosophy, gematria, modern Western numerology, and Indian planetary numerology are related source families, but they are not one continuous, uniform system.

## 2. Canonical app calculation

Moolank uses the **day of birth only**.

```text
moolank = digital_root(day_of_month)
```

For valid Gregorian calendar dates, the day is from 1 to 31 and the result is always from 1 to 9.

### Moolank 1 date series

| Birth day | Reduction | Result |
|---|---:|---:|
| 1 | 1 | 1 |
| 10 | 1 + 0 | 1 |
| 19 | 1 + 9 = 10; 1 + 0 | 1 |
| 28 | 2 + 8 = 10; 1 + 0 | 1 |

Canonical set:

```json
{
  "moolank": 1,
  "birthDays": [1, 10, 19, 28],
  "calculationSource": "day-of-birth-only",
  "reductionMethod": "repeated digit sum to 1-9",
  "masterNumberException": false
}
```

## 3. Calculation boundaries

The following are separate constructs and must not be mixed into Moolank calculation:

- full-date digit sum;
- Life Path or Destiny Number;
- name number;
- compound name number;
- year number;
- personal year;
- astrological Sun sign;
- weekday of birth.

Example: a person born on `19 July 1995` has Moolank 1 because the day is 19. The year and month do not alter the Moolank.

## 4. Input validation rules

The calculation engine must:

1. parse a real calendar date;
2. extract the local calendar day, not a UTC-shifted day;
3. reject impossible dates;
4. preserve the original day for compound-date interpretation;
5. return both the reduced Moolank and original birth-day variant.

Recommended output:

```json
{
  "inputDate": "1995-07-19",
  "birthDay": 19,
  "reductionTrace": [19, 10, 1],
  "moolank": 1,
  "compoundVariant": "M1-D19"
}
```

## 5. Historical layers

### 5.1 Ancient number symbolism

Numbers carried religious, philosophical, mathematical, and symbolic meanings in many ancient cultures. This broad history is relevant context, but it does not by itself establish the modern Moolank calculation.

Ancient number symbolism should therefore be tagged as **historical background**, not as direct evidence for a birth-number personality system.

### 5.2 Pythagorean and later Greek number philosophy

Pythagorean traditions treated numbers as principles of order, proportion, harmony, and cosmology. Later writers such as Nicomachus and Iamblichus transmitted and expanded symbolic interpretations of the first numbers.

This supports a historical lineage for number symbolism. It does **not** prove that the modern practice of reducing a birth day to a personality number was taught by Pythagoras in its current form.

App rule:

```text
Do not label the Moolank day-of-birth system as an ancient Pythagorean fact unless a direct historical source demonstrates that exact method.
```

### 5.3 Gematria, isopsephy and arithmancy

Gematria and isopsephy assign numerical values to letters or words. Arithmancy is a broader divinatory use of numbers. These practices are historically relevant but operationally different from Moolank.

They belong in the history of numerological practices, not in the calculation formula for Moolank 1.

### 5.4 Modern Western numerology

Modern English-language numerology commonly uses digit reduction and distinguishes several numbers derived from names and birth dates. Labels and formulas vary between authors.

The app must avoid treating terms such as `Birth Number`, `Birthday Number`, `Life Path`, and `Destiny Number` as universal synonyms. A source glossary is required whenever content is imported.

### 5.5 Cheiro-style number series

Cheiro's modern numerology writings are an influential direct source family for grouping dates into number series. In this tradition, 1, 10, 19, and 28 belong to the Number 1 series, and Number 1 is associated with the Sun.

For this project:

- the date grouping may be used as direct traditional support;
- Sun rulership must be labelled as traditional planetary correspondence;
- personality and outcome claims require separate evidence grading;
- predictions, lucky dates, cures, or guaranteed outcomes are not automatically canonical.

### 5.6 Indian Moolank usage

Contemporary Indian numerology commonly uses `Moolank` or `Mulank` for the reduced day of birth and maps numbers 1–9 to planetary rulers. In that system, Moolank 1 usually includes 1, 10, 19, and 28 and is associated with Surya/Sun.

This is the app's operational tradition, but it should be described as a contemporary numerology framework rather than a scientifically validated or uniformly ancient Vedic rule.

## 6. System-conflict matrix

| Topic | Project decision | Reason |
|---|---|---|
| Day only vs full date | Day only | Locked Moolank definition |
| Reduce to 1–9 | Yes | Shared foundation schema |
| Preserve 10, 19, 28 | Yes, as variants | Prevents loss of source-specific compound interpretation |
| Treat 11 or 22 as Moolank master numbers | No | Foundation is fixed to 1–9 |
| Sun association | Traditional metadata | Not scientific causation |
| Pythagorean origin claim | Restricted | Exact modern method is not securely established as ancient |
| Chaldean label for all birth-number content | Restricted | Chaldean name mappings and birth-day reduction are often conflated in popular sources |
| Prediction from Moolank | Prohibited as certainty | Unsupported and unsafe |

## 7. Compound-date policy

All four dates reduce to Moolank 1, but the app stores the original day.

```json
[
  { "variantId": "M1-D01", "day": 1, "root": 1 },
  { "variantId": "M1-D10", "day": 10, "root": 1 },
  { "variantId": "M1-D19", "day": 19, "root": 1 },
  { "variantId": "M1-D28", "day": 28, "root": 1 }
]
```

Variant interpretations are deferred to `M1-R016`. Until that review is complete, no app text may imply that 10, 19, or 28 has a verified distinct psychological effect.

## 8. Evidence classification

### Direct traditional evidence

A source explicitly describes birth-day reduction or directly groups 1, 10, 19, and 28 as Number 1.

### Indirect symbolic evidence

A source discusses the symbolism of One, unity, beginning, primacy, or solar correspondence without using the Moolank birth-day method.

### Historical context

A source documents Pythagoreanism, gematria, arithmancy, number symbolism, or other historical practices but does not establish the modern calculation.

### Scientific evidence

Research would need to test whether birth-day categories reliably predict personality or outcomes beyond chance, bias, and cultural expectation. This link is currently marked `not-established` in the project.

## 9. Canonical claims approved from this record

1. Moolank 1 is calculated from birth days 1, 10, 19, and 28.
2. The app reduces the day repeatedly until one digit from 1 to 9 remains.
3. The original day is preserved for later compound-date research.
4. Moolank is separate from full-date and name-based numerology numbers.
5. Sun association is a traditional correspondence, not a scientific mechanism.
6. Ancient number symbolism provides context, not direct validation of modern Moolank personality claims.
7. Numerology-specific prediction from date of birth is not scientifically established.

## 10. Claims not approved

- Pythagoras invented the current Moolank formula.
- All systems called Chaldean, Pythagorean, or Vedic use identical rules.
- Birth day causes leadership, ego, success, disease, wealth, fame, or relationship outcomes.
- A person born on 1, 10, 19, or 28 must display a fixed personality.
- Sun correspondence provides medical or diagnostic information.
- 19 or 28 is inherently lucky, karmically cursed, superior, or dangerous.

## 11. App-safe explanation

> Your Moolank is calculated from the day of the month on which you were born. Days 1, 10, 19, and 28 reduce to Moolank 1. Numerology traditions associate this number with themes such as individuality and initiative, and commonly connect it with the Sun. These are traditional reflection themes, not scientifically proven personality predictions.

## 12. Calculation pseudocode

```text
function calculateMoolank(date):
    validate date
    day = local calendar day(date)
    trace = [day]
    value = day
    while value > 9:
        value = sum(decimal digits of value)
        trace.append(value)
    return {
        birthDay: day,
        reductionTrace: trace,
        moolank: value,
        compoundVariant: "M" + value + "-D" + zeroPad(day)
    }
```

## 13. Test cases

| Input | Day | Trace | Expected |
|---|---:|---|---:|
| 2000-01-01 | 1 | 1 | 1 |
| 2000-01-10 | 10 | 10 → 1 | 1 |
| 2000-01-19 | 19 | 19 → 10 → 1 | 1 |
| 2000-01-28 | 28 | 28 → 10 → 1 | 1 |
| 2000-01-29 | 29 | 29 → 11 → 2 | 2 |
| 2001-02-29 | invalid | — | reject |
| 2000-02-29 | 29 | 29 → 11 → 2 | 2 |

## 14. Source register

### Historical and reference context

- Encyclopaedia Britannica, **Number symbolism** — background on symbolic meanings assigned to numbers across traditions.
- Stanford Encyclopedia of Philosophy and standard histories of Pythagoreanism — contextual support for number philosophy; not direct proof of modern birth-number calculation.
- Historical material on gematria, isopsephy, and arithmancy — context for letter-number and divinatory systems.

### Direct modern numerology source family

- Cheiro, **Cheiro's Book of Numbers** — direct modern source for number series including 1, 10, 19, and 28 and solar correspondence.
- Contemporary Indian Moolank/Mulank sources — direct evidence for current terminology and operational practice; quality varies and each claim must be graded individually.

## 15. Source limitations

- Popular numerology sources frequently copy one another without citation.
- Historical terms are often merged inaccurately.
- A symbolic history of number One is not evidence that a birth date predicts behaviour.
- Direct Moolank sources are primarily traditional or popular rather than empirical.
- Compound-date interpretations vary substantially and require a dedicated conflict review.

## 16. Downstream requirements

This record controls:

- the Moolank calculator;
- date validation;
- source terminology normalization;
- storage of compound variants;
- scientific disclaimers;
- future `M1-R016` compound-date research.

The next research unit is `M1-R003 — Core Personality Architecture`, which will compare direct Moolank 1 sources, identify repeated themes, separate broad statements from observable constructs, and produce balanced/under-pressure/growth-support records.