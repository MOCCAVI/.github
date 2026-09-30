# Landing-page asset provenance

Prepared for local review on 2026-09-30. Nothing in this change publishes the
source proposal or the slide deck in full.

## Supplied figures

- `context-metamodel.png`: Felix Schwickerath, *Modelling Context in
  Architecture-Based Protection Analyses*, master's thesis proposal, supplied as
  `proposal.pdf`. Figure 4.1, printed p. 9 (PDF page 13).
- `analysis-process.png`: same proposal, Figure 4.2, printed p. 9 (PDF page 13).
  The original caption attributes the process to references [3, 12] in that
  proposal; those works were not independently retrieved or read for this edit.

Both figures are cropped from the original PDF and rendered at 240 dpi, without
redrawing or altering notation. Page headings, prose, captions and page numbers
are excluded from the images; attribution and figure numbers appear in the
landing-page text. Reading depth: full text of the proposal's concept sections
4.1–4.2, plus visual inspection of the original figure page. The remainder was
text-extracted for orientation, not independently fact-checked. The proposal is
a design source, not evidence that the approach is implemented or validated.

## Brand assets

- `moccavi-coffee.png`: original image bytes from `ppt/media/image11.png` in
  the local `proposal_new2.pptx` presentation. Original resolution: 300 × 300.
  Displayed at 140 pixels wide. Creator and original license were not specified
  in the inspected file; no attribution or license is inferred.
- `moccavi-logo.svg`: existing MOCCAVI logo from the project's research vault,
  preserved byte for byte. The banner reuses its vector shapes without changes.
- `moccavi-banner.svg`: new vector composition incorporating the existing logo,
  its espresso, cream, sage and ochre palette, and the MOCCAVI name.
- `context-overview.svg`: new conceptual illustration for the landing page.
  It positions the context model inside the V-SUM and relates consumer-specific
  views, Rules/Reactions, xDECAF, LLM judgments and coordination. Its source is
  `Dissertation.md`, PRICOBE chapter, “I — Idea” and “Co — Contributions”
  (sections read in full). It is explicitly a conceptual research design, not
  evidence of completed integrations or an experimental result.

## Copy and project descriptions

- Shared research framing and the driver-monitoring example: `Dissertation.md`,
  Overview and PRICOBE chapter, in the MOCCAVI research vault (read 2026-09-30).
  This internal planning note is not copied into the public repository.
- Repository descriptions: public READMEs of
  [moccavi-web](https://github.com/MOCCAVI/moccavi-web),
  [ConsistencyDeepAgent](https://github.com/MOCCAVI/ConsistencyDeepAgent) and
  [LowCodeConsistencyAI](https://github.com/MOCCAVI/LowCodeConsistencyAI), read
  2026-09-30. Descriptions report their documented purpose; this landing-page
  edit does not independently validate their implementations.
- The former blanket EPL-2.0 statement is replaced with a pointer to each
  repository's license. No new license is assigned to existing or supplied assets.

## Framework interaction diagram

`vitruvius-interactions.svg` maps MOCCAVI's proposed responsibilities to views
and server access, the V-SUM, change propagation and Reactions. The framework
parts are existing systems; dashed cross-column connections describe proposed
MOCCAVI interactions, not implemented endpoints. Context's participation in the
V-SUM is a research design choice, not an upstream feature claim.

Sources read on 2026-09-30:

- [Vitruvius organization documentation](https://github.com/vitruv-tools#structure):
  Idea and Structure sections, read in full.
- [Vitruv core README](https://github.com/vitruv-tools/Vitruv): local checkout's
  framework definition and V-SUM/view/change-propagation description.
- [MOCCAVI integration notes](https://github.com/MOCCAVI/moccavi-web/blob/main/docs/integration/vitruvius.md):
  local document, read for existing versus proposed functionality.
- `Dissertation.md`: all five supporting research areas and Idea/Contributions,
  read in full for the public narrative. Research questions are not presented
  as results.

Coverage of the five areas is expressed without RQ labels on the landing page:
context reuse and evolution; coordination and explained findings; evidence,
baselines and transfer limits; task-specific AI reliability; and coding through
models with quality, lifecycle effort and human-maintainability evaluation.
