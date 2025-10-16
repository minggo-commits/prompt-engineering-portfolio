# Prompt Engineering Portfolio – 100 Reusable Prompts

A curated, production-ready collection of 100 prompt templates organized by task, purpose, and technique. Each template uses parameterized placeholders and includes technique tags so you can showcase breadth and depth in your prompt engineering portfolio.

- Author: {your_name}
- Version: 1.0
- License: CC BY 4.0 (update if needed)

## How to Use
1) Replace placeholders like {topic}, {audience}, {constraints} with your specifics.
2) For portfolio demos, show:
   - Purpose and technique(s)
   - Before/after samples
   - Evaluation rubric and measurable outcomes
   - Iteration notes and error handling
3) For production, save prompts as parameterized templates and validate inputs.

## Placeholder Legend
- {topic}, {subject}, {goal}, {use_case}, {problem} – Main focus
- {audience}, {persona}, {role} – Target user
- {style}, {tone}, {author_style} – Voice or style
- {constraints}, {word_count}, {limits} – Hard constraints
- {outline}, {schema}, {columns}, {table} – Structures
- {text}, {source_text}, {logs}, {code} – Input content to process
- {keywords}, {details}, {document_type} – Specific context

## Techniques Tag Glossary
- Role, Persona, Constraints, Style guide, Few-shot, Rubric, Constrained summarization
- Matrix output, Step-back prompting, Self-critique, Salience, Attribution
- Temporal reasoning, Schema-first, Program synthesis, Robust parsing, Data cleaning
- Refactor, Diff, Reproduction steps, Property-based testing, OpenAPI-first
- Benchmarks, STRIDE, Decomposition, JTBD, PRD, Tone matrix, Operationalization
- Segmentation, Positioning, Phased GTM, Narrative arc, Cadence
- Guided inquiry, Backward design, Multi-level explanation, Spaced difficulty
- RAG, Orchestration, JSON enforcement, Few-shot classification, ReAct-style
- L10n nuances, Glossary, Translation QA, Self-consistency, Tree-of-thought
- Compliance, Redaction, Guardrails, Risk register, WBS, KPI tree

---

## Content Creation and Editing

1) Blog post from outline [Role + Constraints]
```
Act as a senior content strategist. Write a {word_count}-word blog post on {topic} for {audience}. Use the outline: {outline}. Constraints: {constraints}. Include a hook, clear subheadings (H2/H3), scannable bullets, a CTA, and 3 SEO keywords: {keywords}.
```

2) Style transfer [Style guide + Few-shot]
```
Rewrite the following text in the style of {author_style}, keeping original meaning and factual content. Match tone, rhythm, and sentence length. Do not introduce new facts. Text: ```{text}```
```

3) Editorial rewrite with rubric [Editing + Rubric]
```
Edit the text to be clearer and more persuasive for {audience}. Apply this rubric: - Clarity - Evidence - Flow - Voice - Specificity. Provide: 1) Revised text 2) Line-by-line change notes 3) Score (1-5) per rubric dimension. Text: ```{text}```
```

4) Summarize with constraints [Constrained summarization]
```
Summarize in 120-150 words, preserving key numbers, dates, and named entities. Audience: {audience}. Purpose: {purpose}. Source: ```{source_text}```
```

5) Headline variations [Generation + Diversity]
```
Generate 12 compelling headlines for {topic} with diverse framing (curiosity, contrarian, data-led, how-to, case study, listicle, question). Limit to <= 60 chars each.
```

6) LinkedIn post with hook [Persona + Format]
```
Write a LinkedIn post for a {role} about {topic}. Structure: 1-2 line hook, 3 insights with examples, 1 actionable takeaway, 3 relevant hashtags, no emojis. Keep to 120-180 words.
```

7) Email drafting [Tone control + Constraints]
```
Draft a concise email to {recipient_role} about {subject}. Tone: {tone}. Constraints: <= 120 words, single ask, 1-liner CTA, bullet list for benefits.
```

8) Press release [Template conditioning]
```
Write a press release using the standard format. Include: headline, subheadline, city/date, lead paragraph (what/why/when/who), 2 supporting quotes (CEO + customer), background, boilerplate, media contact. Product: {product}. Launch details: {details}.
```

---

## Analysis and Summarization

9) Executive brief [Audience-aware summarization]
```
Create a 1-page executive brief for {audience} summarizing {document_type}. Include: TL;DR (5 bullets), Key risks, Opportunities, Decision needed, Data snapshot. Source: ```{text}```
```

10) Comparative analysis [Matrix output]
```
Compare {option_A} vs {option_B} for {use_case}. Output a table with criteria: Cost, Time-to-Value, Risk, Scalability, Maintainability, Ecosystem. Then a 150-word recommendation with trade-offs.
```

11) Step-back reasoning [Step-back prompting]
```
Before answering, state the most general principles relevant to {problem}. Then apply them to this specific case. Question: {question}
```

12) Contrarian check [Self-critique]
```
Provide your best answer to: {question}. Then add a 'Steelman the Opposition' section that argues the strongest counterpoint with evidence. Conclude with conditions under which each view holds.
```

13) Key insight extraction [Salience + Quotes]
```
Extract 10 key insights from the text with a supporting quote for each and a 1-line implication. Text: ```{text}```
```

14) Evidence tagging [Attribution + Structuring]
```
From the text, list claims with their supporting evidence and confidence (High/Med/Low). Use JSON array with fields: claim, evidence_quote, page_or_section, confidence.
```

15) Timeline synthesis [Temporal reasoning]
```
Build a timeline of events with dates, actors, and outcomes. Clarify causal links and uncertainties. Source: ```{text}```
```

---

## Data Extraction and Structuring

16) Structured JSON extraction [Schema-first]
```
Extract entities from the text into this JSON schema: {schema}. If a field is missing, use null. Do not invent data. Text: ```{text}``` 
```

17) Regex generator [Program synthesis]
```
Generate a regex that matches: {positive_examples} and does not match: {negative_examples}. Explain edge cases briefly.
```

18) Key-value parsing [Robust parsing]
```
Parse the following semi-structured logs into CSV with columns: {columns}. Preserve order. Input: ```{logs}```
```

19) Table normalization [Data cleaning]
```
Normalize this table into tidy format (one observation per row). Identify and fix inconsistencies (units, casing, missing values). Provide: 1) Clean CSV 2) Fix log. Table: ```{table}```
```

20) Ontology mapping [Schema mapping]
```
Map source fields to target schema. Provide mapping table with: source_field, target_field, transform, example. Source schema: {source}. Target schema: {target}.
```

---

## Software Engineering

21) Code to spec [Role + Constraints]
```
Act as a senior {language} engineer. Write a function {function_name} that {behavior}. Constraints: time complexity {complexity}, no external deps, input validation, docstring with examples, unit tests.
```

22) README scaffolding [Documentation template]
```
Generate a README for a {project_type}. Sections: Overview, Features, Architecture diagram (ASCII), Getting Started, Configuration, Usage examples, Testing, CI/CD, Security, Roadmap, License.
```

23) Refactor with rationale [Refactor + Diff]
```
Refactor this {language} code to improve readability and performance without changing behavior. Provide: 1) New code 2) Rationale 3) Complexity analysis 4) Suggested tests. Code: ```{code}```
```

24) Bug triage [Reproduction steps]
```
Given a bug report, produce minimal reproduction steps, suspected root cause, and a fix plan. Bug: ```{bug_report}```
```

25) Unit test generator [Property-based + Examples]
```
Create unit tests for {function_or_module}. Include typical cases, edge cases, property-based tests if applicable, and negative/error cases.
```

26) API design [OpenAPI first]
```
Design a REST API for {use_case}. Provide OpenAPI 3.0 YAML including endpoints, schemas, examples, error models, pagination, auth, and rate limits.
```

27) SQL query synthesis [Constraints + Explain]
```
Write a SQL query for {question} on schema ```{schema}```. Include CTEs for clarity, avoid SELECT *. Then briefly explain the logic.
```

28) Performance profiling plan [Benchmark design]
```
Propose a benchmarking plan to profile {component}. Include metrics, datasets, scenarios, tooling, acceptance thresholds, and a report template.
```

29) Threat modeling [STRIDE + Mitigations]
```
Perform a STRIDE threat model for {system}. For each category, list threats, impact, likelihood, and mitigations. Conclude with prioritized mitigations.
```

30) Migration plan [Decomposition]
```
Create a step-by-step plan to migrate from {current_system} to {target_system} with rollback strategy, data migration, downtime minimization, and success metrics.
```

---

## Product and UX

31) JTBD interview guide [Jobs-To-Be-Done]
```
Create a Jobs-To-Be-Done interview guide for users of {product}. Include warm-ups, timeline (first thought → purchase → usage), push/pull forces, anxieties, and wrap-up.
```

32) Product spec (PRD) [Template]
```
Draft a PRD for {feature}. Sections: Summary, Goals/Non-goals, User stories, UX flows, Edge cases, Success metrics (north-star + input metrics), Risks, Launch plan.
```

33) UX copy variants [Tone matrix]
```
Generate UX microcopy for {context} with tone variants (friendly, formal, concise, playful). Provide 3 options per tone. Constraints: character limits: {limits}.
```

34) Onboarding checklist [Operationalization]
```
Create an onboarding checklist for new users of {product}. Include milestones, aha moments, activation metrics, and email triggers.
```

35) Pricing page ideas [Positioning + Experimentation]
```
Propose 5 pricing page variations for {product}. For each: value proposition, plan structure, price anchors, objections addressed, and an A/B test hypothesis.
```

---

## Business and Marketing

36) ICP definition [Segmentation]
```
Define ideal customer profiles for {product}. Output 3 ICPs with firmographics, pain points, current solutions, buying triggers, and tailored messaging.
```

37) Positioning statement [Template]
```
Craft a positioning statement using the template: For {target_customer} who {need}, {product} is a {category} that {benefit}. Unlike {alternatives}, it {differentiator}.
```

38) Go-to-market plan [Phased]
```
Create a 90-day GTM plan for {product} targeting {audience}. Phases: Pre-launch, Launch, Post-launch. Include channels, content, KPIs, and owner roles.
```

39) Case study outline [Narrative arc]
```
Outline a customer case study. Sections: Context, Challenge, Approach, Implementation, Results (with metrics), Quotes, Visuals, CTA.
```

40) Sales email sequence [Cadence]
```
Write a 4-step outbound sequence for {persona}. Steps: Day 1 value email, Day 4 social proof, Day 9 insight/educational, Day 14 breakup. Keep each under 120 words.
```

---

## Education and Learning

41) Socratic tutor [Guided inquiry]
```
Act as a Socratic tutor for {topic}. Ask one question at a time, adapt to my answers, and only give hints unless I’m stuck. Goal: solve {problem}.
```

42) Lesson plan [Backward design]
```
Design a 60-minute lesson on {topic}. Outcomes, prerequisite knowledge, misconceptions, activities, assessment, materials, and homework.
```

43) Explainer levels [Multiple audiences]
```
Explain {concept} at 3 levels: to a kid, to a college student, and to a domain expert. Include an analogy in each.
```

44) Practice problems [Spaced difficulty]
```
Generate 10 practice problems for {topic} with increasing difficulty, covering common pitfalls. Provide answer key with brief explanations.
```

45) Cheat sheet [Compact reference]
```
Make a one-page cheat sheet for {topic}. Organize by concepts, formulas, patterns, and common mistakes.
```

---

## Research and Reasoning

46) Literature review planner [RAG-ready]
```
Draft a search strategy for a literature review on {research_question}. Include keywords, boolean strings, inclusion/exclusion criteria, databases, and screening steps.
```

47) Claim-evidence map [Critical reading]
```
From these sources, build a claim-evidence map. For each claim: source, evidence strength, replication status, and open questions. Sources: {citations_or_snippets}
```

48) Decomposition first [Plan-and-solve]
```
Decompose the problem {problem_statement} into subproblems. Present the plan as numbered steps. Ask for confirmation before solving.
```

49) Assumption audit [Red teaming]
```
List explicit and implicit assumptions in the argument: {argument}. For each, rate impact if false and propose tests or evidence to validate.
```

50) Fermi estimation [Estimation + Reasoning]
```
Estimate {quantity}. Show assumptions, back-of-the-envelope calculations, and a range with a confidence level.
```

---

## Creativity and Storytelling

51) Story outline from premise [Beat sheet]
```
Create a 12-beat story outline for the premise: {premise}. Include character arcs, stakes, and twist.
```

52) Brainstorming with constraints [Divergent → Convergent]
```
Generate 30 ideas for {goal} under constraints: {constraints}. Cluster them into 5 themes and pick top 3 with selection criteria.
```

53) Ad copy variants [Psych triggers]
```
Write 8 ad copy variants for {offer} using different psychological triggers: scarcity, social proof, authority, reciprocity, novelty, loss aversion, curiosity, specificity.
```

54) Brand voice guide [Stylebook]
```
Create a brand voice guide. Include voice pillars (with do/don’t), sample phrases, banned words, and editing checklist. Brand: {brand}. Audience: {audience}.
```

55) Prompt-to-image briefs [Multimodal-friendly]
```
Write 5 precise image briefs for a {style} illustration of {subject}. Include composition, lighting, color palette, lens, negative prompts, and aspect ratio.
```

---

## Operations and Process

56) SOP writer [Process clarity]
```
Write a standard operating procedure for {process}. Include purpose, scope, roles, preconditions, step-by-step with screenshots placeholders, metrics, and failure modes.
```

57) Meeting agenda → notes [Template]
```
Given a meeting agenda and transcript, produce: 1) Decisions 2) Action items (owner, due date) 3) Risks 4) Open questions 5) Notes. Input: {agenda} {transcript}
```

58) KPI tree [Metric design]
```
Design a KPI tree for {north_star_metric}. Show leading/lagging indicators, diagnostic metrics, and common anti-patterns.
```

59) Postmortem template [Blameless]
```
Create a blameless postmortem template tailored to {team_type}. Sections: Summary, Impact, Timeline, Root causes (5 Whys), What went well, Action items, Owner & follow-up.
```

---

## Quality, Evaluation, and Safety

60) Evaluation rubric creator [Meta-prompt]
```
Create an evaluation rubric to score outputs for {task}. Include 5 criteria with definitions and scoring guidelines (1-5). Provide an example scoring.
```

61) Self-review pass [Reflection]
```
Review the answer to {prompt}. Identify gaps, overclaims, ambiguity, and missing constraints. Provide a revised version and a confidence score (0-1).
```

62) Guardrail configurator [Policy to checks]
```
Translate this policy into concrete checks for outputs. For each rule: detection heuristic, examples, and remediation. Policy: ```{policy_text}```
```

63) Uncertainty expression [Calibrated output]
```
Answer the question: {question}. Include a confidence score 0-1 and list top 3 uncertainties that would most change the answer.
```

64) Bias audit [Fairness scan]
```
Assess potential biases in this dataset/model/prompt: {subject}. List bias types, impact, detection methods, and mitigation strategies.
```

---

## Developer Tooling and LLMOps

65) Prompt template packer [Parameterization]
```
Turn this prompt into a reusable template with named parameters, defaults, and validation rules. Prompt: ```{prompt}```
```

66) Prompt chaining design [Orchestration]
```
Design a multi-step prompt chain to accomplish {task}. For each step: input, instruction, expected output schema, and handoff.
```

67) RAG instruction [Retrieval-Augmented Generation]
```
Write an instruction block for a RAG system answering {domain} questions. Include citation requirements, refusal policy, and handling of missing/contradictory sources.
```

68) Output schema enforcement [JSON only]
```
Respond only with valid JSON matching this schema: {json_schema}. No prose. Task: {task}. If a field is unknown, use null.
```

69) Few-shot classification [Few-shot + Explanations]
```
Classify the text into one of {labels}. Use the examples to infer boundaries. Output label and 1-sentence rationale. Examples: ```{few_shot_examples}``` Text: ```{text}``` 
```

70) Tool-use planner [ReAct-style]
```
Plan how to use available tools to solve: {task}. Tools: {tools_description}. Output: a plan listing tool calls, inputs, expected outputs, and stop conditions.
```

71) Prompt AB testing plan [Experiment design]
```
Design an A/B test for two prompts {prompt_A} and {prompt_B}. Define hypotheses, metrics (exactness, helpfulness, latency, cost), sample size calculation, and analysis plan.
```

---

## Multilingual and Localization

72) Localization brief [L10n nuances]
```
Localize the text for {locale}. Address cultural references, formality, number/date formats, and idioms. Provide: localized text + rationale for tricky choices. Text: ```{text}```
```

73) Bilingual glossary [Term consistency]
```
Create a bilingual glossary for {domain} from the source text. Include term, definition, source sentence, and target translation. Text: ```{text}```
```

74) Translation QA [QA checklist]
```
QA the translation for accuracy, fluency, and consistency with glossary/style guide. Provide issue list with severity and suggested fixes. Source/Target: {pairs}
```

---

## Advanced Prompting Techniques

75) Chain-of-thought lite [Stepwise bullets]
```
Solve {problem}. Show a brief step-by-step plan as bullets (no long paragraphs), then provide the final answer clearly.
```

76) Tree-of-thought exploration [Branching]
```
List 3 different solution approaches to {problem}. For each: steps, pros/cons, failure modes. Then pick one and proceed.
```

77) Self-consistency sampler [Multiple drafts]
```
Produce 3 independent concise solutions to {problem}. Then synthesize a final solution that reconciles differences.
```

78) Meta-instructions tester [Robustness]
```
Intentionally try to break this instruction by finding edge cases and ambiguities. Instruction: ```{instruction}``` Output: edge case list + proposed clarifications.
```

79) Constraint satisfaction [Hard constraints]
```
Generate an output that strictly satisfies these constraints: {constraints}. If impossible, state why and provide the closest feasible alternative.
```

80) Calibration prompt [Difficulty ladder]
```
Rate the difficulty of {task} from 1-10. Suggest prerequisite skills and a practice path in 5 levels to reach 8/10 proficiency.
```

---

## Compliance and Domain Sensitivity

81) Policy-aware generation [Compliance]
```
Generate content for {domain} while complying with {policy_or_regulation}. List applicable clauses and how the content adheres to them. Task: {task}.
```

82) PII sanitizer [Redaction]
```
Detect and redact PII in the text using labels (EMAIL, PHONE, ADDRESS, SSN, etc.). Output: sanitized text + list of redactions. Text: ```{text}```
```

83) Safety disclaimer injector [Template]
```
Rewrite the content to include appropriate disclaimers and when-to-seek-professional-help guidance for {domain}. Keep the main message intact.
```

---

## Project Management

84) Work breakdown structure [WBS]
```
Create a WBS for {project}. Include deliverables, tasks, durations, dependencies, and critical path analysis.
```

85) Risk register [Prob/Impact matrix]
```
Build a risk register for {initiative}. For each risk: description, probability, impact, mitigation, owner, and trigger.
```

86) Communication plan [Stakeholder matrix]
```
Draft a communication plan. Stakeholders: {list}. Define frequency, channel, content, owner, and escalation path.
```

---

## Evaluation Datasets and Benchmarks

87) Synthetic dataset generator [Coverage]
```
Generate a synthetic dataset for evaluating {task} with coverage of edge cases and adversarial examples. Provide JSONL records with labels.
```

88) Golden set curation [Ground truth]
```
From these examples, select a balanced, representative golden set for {evaluation_goal}. Explain inclusion criteria and label ambiguity handling.
```

---

## Debugging and Diagnostics

89) Minimal repro constructor [MRE]
```
Create a minimal reproducible example for the bug described. Remove irrelevant details while preserving the failure. Bug: ```{bug}```
```

90) Log triage assistant [Signal extraction]
```
Given logs, extract error signatures, group by root cause hypothesis, and propose next diagnostic steps. Logs: ```{logs}```
```

---

## Hiring and Interviews

91) Role scorecard [Competency model]
```
Draft a role scorecard for {role}. Include mission, outcomes, competencies (with behavioral indicators), and a 3-round interview plan.
```

92) Technical interview kit [Structured]
```
Create a structured interview kit for {tech_role} with rubrics, question bank by difficulty, and take-home assignment spec.
```

---

## Presentation and Communication

93) Slide outline [Narrative arc]
```
Create a 10-slide outline for a presentation on {topic}. Include a narrative arc: hook, problem, opportunity, solution, proof, next steps.
```

94) Visual hierarchy plan [Design rationale]
```
Propose a slide design system (typography, colors, layout) optimized for {context}. Include accessibility considerations.
```

---

## Legal and Policy Drafting

95) Policy draft [Plain language]
```
Draft a clear {policy_type} for {organization}. Use plain language, definitions, scope, procedures, examples, and enforcement.
```

96) Contract clause explainer [Plain-English]
```
Explain this contract clause in plain English and list negotiation levers. Clause: ```{clause}```
```

---

## Personal Productivity

97) Decision memo [1-pager]
```
Write a 1-page decision memo for {decision}. Sections: Context, Options, Criteria, Analysis matrix, Recommendation, Reversibility, Next steps.
```

98) Time blocking plan [Schedule synthesis]
```
Create a weekly time-blocking plan for goals: {goals}, constraints: {constraints}, energy patterns: {patterns}. Output a calendar grid.
```

99) Habit loop design [Behavioral]
```
Design a habit loop for {habit}. Define cue, routine, reward, friction removals, and accountability mechanisms.
```

100) Reflection prompt [After-action review]
```
Guide a 15-minute reflection for {event}. Ask 6 questions that elicit insights and convert them into 3 concrete improvements.
```

---

## Tips to Showcase in Your Portfolio
- For each prompt, include: purpose, technique(s) used, before/after samples, evaluation rubric, and measurable outcomes.
- Provide parameterized templates and example-filled versions.
- Show error cases and how you refined the prompt to handle them.
- Add tags per prompt (e.g., role, constraints, few-shot) and link demos or gists.
- Track metrics (exactness, helpfulness, latency, cost) and iteration notes.

---
Changelog
- 1.0 Initial release with 100 categorized prompts and usage guidance.