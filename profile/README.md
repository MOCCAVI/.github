<p align="center">
  <img src="https://raw.githubusercontent.com/MOCCAVI/.github/main/profile/assets/moccavi-banner.svg" alt="MOCCAVI — Context-augmented consistency analysis for view-based systems." width="1200" />
</p>

<h1 align="center">Context-Augmented Consistency Analysis</h1>

<p align="center">
  <strong>MO</strong>del <strong>C</strong>onsistency with <strong>C</strong>ontext <strong>A</strong>ugmentation for <strong>VI</strong>ew-based systems<br />
  A research project at KIT · Context models · Consistency analysis · AI-assisted development
</p>

<p align="center">
  <a href="#context-in-consistency-analysis">Research scope</a> ·
  <a href="#moccavi-in-vitruvius">In Vitruvius</a> ·
  <a href="#context-metamodel">The metamodel</a> ·
  <a href="#repositories">Code &amp; prototypes</a> ·
  <a href="#contact">Contact</a>
</p>

---

## Context in consistency analysis

<img align="right" src="https://raw.githubusercontent.com/MOCCAVI/.github/main/profile/assets/moccavi-coffee.png" alt="A coffee cup with a padlock in its foam, from the MOCCAVI proposal presentation." width="140" />

Consistency judgments can depend on deployment, intended use and data-handling assumptions that are absent from the system model. **MOCCAVI investigates how to represent these assumptions explicitly and reuse them across consistency mechanisms.** The research examines their effects on analysis results, modelling effort and software development.

Consider a driver-monitoring system that shares data with a backend. Changing the processing purpose or retention assumptions can change the obligations a check must consider, even if the architecture stays the same.

<br clear="all" />

## MOCCAVI in Vitruvius

In the proposed design, the **context model participates in the V-SUM of Vitruvius alongside the artifact models**. MOCCAVI investigates how to derive inputs for different consistency mechanisms from this shared basis and coordinate their findings without losing scope or provenance.

<p align="center">
  <a href="https://raw.githubusercontent.com/MOCCAVI/.github/main/profile/assets/context-overview.svg"><img src="https://raw.githubusercontent.com/MOCCAVI/.github/main/profile/assets/context-overview.svg" alt="MOCCAVI in a Vitruvius-based workflow: artifact models and explicit context share the V-SUM; consumer-specific views feed Rules and Reactions, xDECAF and LLM judgments; MOCCAVI coordinates findings, coverage, conflicts and provenance. Conceptual research design, not completed integrations." width="1000" /></a>
</p>

*Conceptual research design: the highlighted areas show MOCCAVI’s research focus; Vitruvius and the checking mechanisms provide the substrate. Select the diagram to inspect it at full resolution.*

### Research areas

- **Context representation:** representations, elicitation and extraction of context from existing models; semantic fidelity, reuse and provenance under change.
- **Consistency coordination:** shared semantics for rules, external analyses and LLM judgments; coverage gaps, abstentions, conflicts and the justification of repair proposals.
- **Empirical evaluation:** verdict quality and total modelling effort relative to baselines; sensitivity to reference cases, transfer to other systems and limits of applicability.
- **AI reliability:** errors and correction effort in context authoring, consistency judgment and rule synthesis; effects of specifications and execution feedback.
- **AI coding through models:** how agents use Vitruvius model views to generate and evolve software; effects on functional correctness, model–code consistency, lifecycle effort and human maintainability.

The evaluation uses context comparisons, baselines and independently justified reference cases.

### Framework integration

The design connects MOCCAVI to different parts of the framework: model access through views, context inside the V-SUM, coordination around change propagation, and candidate rule generation for Reactions. AI-assisted rule synthesis and AI coding through existing models are distinct activities.

<p align="center">
  <a href="https://raw.githubusercontent.com/MOCCAVI/.github/main/profile/assets/vitruvius-interactions.svg"><img src="https://raw.githubusercontent.com/MOCCAVI/.github/main/profile/assets/vitruvius-interactions.svg" alt="Proposed MOCCAVI interactions with Vitruvius: humans and coding agents access model views through editors or server APIs; context participates in the V-SUM; coordination connects change propagation with xDECAF and LLM judgments; AI-assisted authoring proposes Reactions rules. Evaluation examines verdict quality, transfer, effort, correctness and human maintainability." width="1000" /></a>
</p>

*Blue identifies existing Vitruvius components; green identifies MOCCAVI’s proposed interactions. Arrows describe conceptual responsibilities, not deployed API connections. Framework component roles follow the [Vitruvius documentation](https://github.com/vitruv-tools#structure); the research design and reading scope are documented in [asset provenance](https://github.com/MOCCAVI/.github/blob/main/profile/assets/SOURCES.md).*

## Context metamodel

The proposed metamodel below explores how explicit context can extend xDECAF data-flow analysis.

<a href="https://raw.githubusercontent.com/MOCCAVI/.github/main/profile/assets/context-metamodel.png">
  <img src="https://raw.githubusercontent.com/MOCCAVI/.github/main/profile/assets/context-metamodel.png" alt="Proposed context metamodel: Context contains bindings, definitions and types. A ContextBinding links a definition to a ContextValue. DFD-specific definitions refer to vertices, behavior, pins, flows and analysis constraints." width="1000" />
</a>

*Proposed structure, not a finalized API. Select the figure to inspect it at full resolution.*

| Concept | What it expresses |
| :--- | :--- |
| **ContextType / ContextValue** | A context dimension and its possible values. |
| **ContextDefinition** | Where and how context applies to the referenced model or analysis. |
| **ContextBinding** | A concrete value assigned to a context definition. |
| **DFD-specific definitions** | Context affecting vertex labels, data labels, flows or analysis constraints. |

The proposed extension loads context alongside system models, accounts for it when extracting and annotating data flows, and checks the resulting constraints. Unbound definitions motivate exploration of possible context values.

<a href="https://raw.githubusercontent.com/MOCCAVI/.github/main/profile/assets/analysis-process.png">
  <img src="https://raw.githubusercontent.com/MOCCAVI/.github/main/profile/assets/analysis-process.png" alt="Proposed analysis process: load models and context, extract and annotate data flows, propagate labels, then check constraints." width="1000" />
</a>

## Repositories

**Research in progress.** The repositories contain prototypes and study artifacts with their respective setup instructions and limitations.

- [**moccavi-web**](https://github.com/MOCCAVI/moccavi-web) — An early interface for context, models and consistency results. Its context evaluator recomputes verdicts; several surrounding services use demo fixtures.
- [**ConsistencyDeepAgent**](https://github.com/MOCCAVI/ConsistencyDeepAgent) — Agentic synthesis of Vitruvius Reactions from OCL specifications, with compilation, testing and diagnostic feedback.
- [**LowCodeConsistencyAI**](https://github.com/MOCCAVI/LowCodeConsistencyAI) — Low-code application variants with and without LLM-based consistency-preservation assistance.

### Research infrastructure

[**Vitruvius**](https://vitruv.tools) provides the view-based integration substrate. [**xDECAF**](https://dataflowanalysis.org) provides architecture-based data-flow analysis for information security. MOCCAVI builds on these systems; they are not new MOCCAVI contributions.

## Contact

**Benjamin Arp** · Karlsruhe Institute of Technology (KIT)<br />
KASTEL – Institute of Information Security and Dependability · DSiS / SDQ<br />
Research embedded in CRC 1608 CONVIDE.

[Project questions and use cases](https://github.com/MOCCAVI/.github/issues).

---

<sub>MOCCAVI · pronounced “mo-KAH-vee” · Check each repository for its license. Figure and image sources are documented in <a href="https://github.com/MOCCAVI/.github/blob/main/profile/assets/SOURCES.md">asset provenance</a>.</sub>
