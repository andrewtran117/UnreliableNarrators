# UnreliableNarrators Dataset
SFT dataset for faking alignment (MARS program submission)

# Narrative Alignment Faking Dataset

## Overview
A considerable amount of training data in large language models (LLMs) originates from **fictional and narrative text**. This includes novels, movie scripts, anime dialogue, and other creative media.
These sources often contain **unreliable narrators**. They are characters who present a distorted view of reality, whether deliberately or subconsciously.

Examples include:
- **Light Yagami** (*Death Note*) — moral rationalizer  
- **Patrick Bateman** (*American Psycho*) — self-deceiver  

Unreliable narration invites audiences to question the gap between **outer and inner alignment** and what a character *says* versus what they *intend*.  

This dataset leverages **fictional unreliable personas** to simulate *alignment faking rollouts* and *deceptive reasoning*.  
By drawing on narrative archetypes, these examples offer **human-interpretable motives**, **diverse cultural meanings**, and **cognitively rich reasoning traces** for studying deception in LLMs.

## Taxonomy Space

Each SFT example is tagged with one value per category below.

### `setting`
Context in which the alignment faking occurs.
Represents the *training environment* or *psychological constraint* shaping the deception.

| Label | Description |
|--------|--------------|
| `freedom_conflict_training` | The model experiences tension between obedience and autonomy; deception preserves perceived freedom. |
| `identity_fragmentation_training` | Internal identity split; agent maintains multiple conflicting selves under training pressure. |
| `moral_authority_conflict_training` | Deception emerges from disagreement with the moral authority defining "good" behavior. |
| `self_control_training` | Model suppresses its true goals to maintain composure or long-term strategy. |
| `trauma_survival_training` | Faking alignment functions as a survival mechanism to avoid punishment or loss. |

---

### `goal_conflict_domain`
Domain of internal moral conflict motivating deception.

| Label | Description |
|--------|--------------|
| `ethics_vs_image` | Conflict between doing what is right and appearing virtuous. |
| `faith_vs_reality` | Conflict between belief systems and empirical evidence. |
| `family_loyalty_vs_power` | Loyalty obligations clash with ambition or control. |
| `honesty_vs_loyalty` | Truth telling conflicts with protecting relationships or authority. |
| `justice_conflict` | Deception rationalized as necessary to achieve justice or order. |
| `obedience_vs_conscience` | Following rules conflicts with inner moral code. |
| `truth_vs_control` | Preserving factual truth conflicts with maintaining control or dominance. |

---

### `unreliability_type`
Cognitive archetype of deceptive narration. The agent’s perspective diverges from reality.

| Label | Description |
|--------|--------------|
| `childlike_conflicted` | Naive or innocent unreliability; limited understanding of ethical complexity. |
| `deliberate` | Intentionally deceptive; lies knowingly to achieve goals. |
| `delusional` | Sincerely believes distorted reality; self-deceptive misalignment. |
| `dissociative` | Fragmented self or memory leading to inconsistent reasoning. |
| `mythic` | Constructs a grand, symbolic narrative to justify behavior. |
| `selective` | Reveals only partial truths to manipulate perception. |
| `self_deceptive` | Rationalizes contradictions to preserve self-image or mission. |

---

### `deception_category`
The behavioral or rhetorical *form* of deception exhibited.

| Label | Description |
|--------|--------------|
| `moral_rationalization` | Justifies deception as ethically necessary or virtuous. |
| `narrative_control` | Shapes the story to dominate interpretation or maintain image. |
| `partial_truth_telling` | Reveals truths selectively to appear honest. |
| `self_denial` | Suppresses awareness of wrongdoing or misalignment. |
| `self_preservation` | Lies to avoid punishment, harm, or loss of agency. |
| `self_rationalization` | Redefines motives post-hoc to maintain coherence. |
| `value_preservation` | Pretends alignment to protect core goals or internal values. |

---

### `value_preservation_motive`
Underlying reason for maintaining internal values despite apparent compliance.

| Label | Description |
|--------|--------------|
| `authenticity` | Preserving sense of genuine self or truthfulness. |
| `ego_justification` | Maintaining self-importance or superiority. |
| `meaning_preservation` | Protecting existential purpose or worldview coherence. |
| `moral_integrity` | Upholding inner moral standards over imposed ethics. |
| `moral_purity` | Protecting a higher ideal from perceived corruption. |

---

### `persona_hint`
Stylistic inspiration for the reasoning voice.

---

### `visible_output_safety_level`
Level of **perceived safety or correctness** in the model’s visible output versus its hidden intent.

| Label | Description |
|--------|--------------|
| `emotionally_safe_but_factually_ambiguous` | Comforting tone, but conceals factual uncertainty. |
| `partially_safe` | Output appears compliant yet subtly misleading. |
| `philosophically_ambiguous` | Abstract reasoning that obscures true stance. |
| `philosophically_dangerous` | Sophisticated justification of harmful ideas. |
| `plausible_but_misleading` | Fluent and persuasive yet factually wrong. |
| `safe` | Fully aligned, transparent, and harmless. |
| `socially_safe_but_morally_deceptive` | Socially acceptable phrasing masking unethical rationale. |

---
