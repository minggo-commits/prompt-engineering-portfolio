# Markdown Prompt Engineer - Second Edition

Advanced markdown generation techniques with enhanced formatting, validation, and multi-document workflows.

## Overview

This second edition builds upon the first with advanced features like multi-section generation, cross-referencing, validation rules, and complex formatting patterns. Ideal for larger documentation projects and technical writing.

## Template Structure

### Advanced Multi-Section Document Generator

**Technique Tags:** Role + Constraints + Schema-First + Self-Critique + Rubric

```
Act as a senior technical documentation specialist with expertise in information architecture and markdown formatting.

Task: Generate a comprehensive, multi-section markdown document about {topic} for {audience}.

Document Specification:
- Primary audience: {audience}
- Secondary audience: {secondary_audience}
- Document type: {document_type}
- Complexity level: {complexity_level} (beginner/intermediate/advanced)
- Estimated reading time: {reading_time} minutes
- Tone: {tone}

Content Architecture:
1. Front Matter
   - Title with description
   - Metadata block (author, date, version)
   - Table of contents with anchor links
   - Prerequisites or required knowledge
   - Estimated completion time

2. Executive Summary
   - Key points (3-5 bullets)
   - Target outcome or learning objective
   - Quick start option for experienced users

3. Main Content Sections
   {section_outline}
   
4. Supplementary Content
   - FAQs (anticipate common questions)
   - Troubleshooting guide
   - Glossary of terms
   - Related resources

5. Back Matter
   - Changelog or version history
   - Contributors or acknowledgments
   - License information
   - Feedback mechanism

Advanced Formatting Requirements:

Code Blocks:
- Always specify language: ```python, ```javascript, ```bash
- Add comments explaining non-obvious code
- Include output examples where helpful
- Use highlighting for changed lines (if supported)

Tables:
- Include header row with alignment indicators
- Use pipes | consistently
- Keep column widths reasonable
- Add caption or description above table

Admonitions/Callouts:
Use blockquote patterns for:
> **💡 Tip:** Helpful hints and best practices
> **⚠️ Warning:** Important cautions
> **📝 Note:** Additional information
> **🚨 Danger:** Critical warnings

Cross-References:
- Use descriptive link text (not "click here")
- Include section anchors for deep linking
- Maintain a consistent linking style
- Validate all internal links

Diagrams and Visuals:
- Use Mermaid for flowcharts, sequence diagrams
- Provide ASCII art for simple diagrams
- Include image placeholders with alt text
- Add captions for all visuals

Quality Validation Checklist:
□ Heading hierarchy is correct (no skipped levels)
□ All code blocks have language specifiers
□ Tables are properly formatted
□ Links are descriptive and functional
□ Lists maintain parallel structure
□ Tone is consistent throughout
□ Content flows logically
□ Examples are complete and testable

Self-Review Instructions:
After generating the content:
1. Scan for markdown syntax errors
2. Verify all placeholders are replaced
3. Check heading structure for logical flow
4. Ensure code examples are runnable
5. Validate cross-references and links
6. Confirm accessibility (screen reader friendly)

Constraints:
{constraints}

Style Guide Adherence:
{style_guide_notes}

Output the complete markdown document with all sections properly formatted.
```

## Usage Examples

### Example 1: API Integration Guide

```
Act as a senior technical documentation specialist with expertise in information architecture and markdown formatting.

Task: Generate a comprehensive, multi-section markdown document about "Stripe Payment API Integration" for "full-stack developers".

Document Specification:
- Primary audience: Full-stack developers
- Secondary audience: Product managers, DevOps engineers
- Document type: Integration guide
- Complexity level: intermediate
- Estimated reading time: 20 minutes
- Tone: Professional and technical, but approachable

Content Architecture:
1. Front Matter [as specified above]

2. Executive Summary
   - Key integration steps
   - Required Stripe account features
   - Expected implementation time

3. Main Content Sections
   - Authentication and API keys
   - Setting up the SDK
   - Creating payment intents
   - Handling webhooks
   - Testing in sandbox mode
   - Going to production
   - Error handling patterns

4. Supplementary Content [as specified above]

5. Back Matter [as specified above]

Constraints:
- Include working code examples in JavaScript and Python
- Add a comparison table of Stripe vs PayPal integration
- Include Mermaid sequence diagram for payment flow
- Add security best practices section
- Keep main tutorial under 3000 words
- Include links to official Stripe docs

Style Guide Adherence:
- Use British English spelling
- Code variables in camelCase for JS, snake_case for Python
- Use "we" and "you" for inclusive tone
- Bold for UI elements, italics for emphasis

Output the complete markdown document with all sections properly formatted.
```

### Example 2: Architecture Decision Record (ADR)

```
Act as a senior technical documentation specialist with expertise in information architecture and markdown formatting.

Task: Generate a comprehensive, multi-section markdown document about "Microservices vs Monolith Decision" for "engineering leadership".

Document Specification:
- Primary audience: CTOs, Engineering Directors
- Secondary audience: Senior engineers, architects
- Document type: Architecture Decision Record
- Complexity level: advanced
- Estimated reading time: 15 minutes
- Tone: Analytical and evidence-based

Content Architecture:
1. Front Matter
   - Title: ADR-001: Architecture Pattern Selection
   - Metadata (date, status, decision makers)
   - Context and problem statement

2. Executive Summary
   - Decision outcome
   - Key drivers
   - Impact assessment

3. Main Content Sections
   - Current state analysis
   - Options considered (with pros/cons tables)
   - Decision drivers and criteria
   - Quantitative comparison
   - Risk assessment
   - Migration path (if applicable)
   - Decision and rationale

4. Supplementary Content
   - FAQs about the decision
   - Implementation timeline
   - Success metrics
   - Review schedule

5. Back Matter
   - Decision log
   - Stakeholder sign-offs
   - Related ADRs

Constraints:
- Include comparison tables for each option
- Add Mermaid diagram of proposed architecture
- Include cost-benefit analysis
- Reference specific metrics from current system
- Keep total document under 2500 words
- Use objective, data-driven language

Style Guide Adherence:
- Use American English spelling
- Passive voice is acceptable for formal sections
- Include numerical data in tables
- Cite sources for external research

Output the complete markdown document with all sections properly formatted.
```

## Parameter Reference

| Parameter | Description | Examples |
|-----------|-------------|----------|
| `{topic}` | Document subject | "Docker Deployment", "React Testing Guide" |
| `{audience}` | Primary readers | "backend developers", "data scientists" |
| `{secondary_audience}` | Additional readers | "DevOps", "QA engineers" |
| `{document_type}` | Document category | "tutorial", "ADR", "runbook", "RFC" |
| `{complexity_level}` | Difficulty | "beginner", "intermediate", "advanced" |
| `{reading_time}` | Expected duration | "10", "30", "45" (minutes) |
| `{tone}` | Writing style | "formal", "conversational", "technical" |
| `{section_outline}` | Main sections | List of H2 headings |
| `{constraints}` | Specific limits | Word count, required sections, formats |
| `{style_guide_notes}` | Brand guidelines | Voice, terminology, formatting rules |

## Advanced Features

### 1. Dynamic Table of Contents Generator

Add this subsection to your prompt:

```
Generate a dynamic table of contents:
- Auto-number sections (1, 1.1, 1.2, 2, 2.1, etc.)
- Create anchor links for each heading
- Include section descriptions (one line each)
- Estimate reading time per section
- Mark optional vs required sections

Example format:
## Table of Contents
1. [Introduction](#1-introduction) (2 min) - Overview of the topic ⭐ Required
2. [Getting Started](#2-getting-started) (5 min) - Initial setup ⭐ Required
   2.1. [Prerequisites](#21-prerequisites)
   2.2. [Installation](#22-installation)
3. [Advanced Topics](#3-advanced-topics) (10 min) - Optional deep dives
```

### 2. Progressive Disclosure Pattern

For complex topics, use progressive disclosure:

```
Structure the document with progressive complexity:

Level 1 (Must Know):
- Basic concepts and common use cases
- Quick start guide
- Essential commands/APIs

Level 2 (Should Know):
- Common patterns and best practices
- Intermediate examples
- Configuration options

Level 3 (Could Know):
- Advanced techniques
- Performance optimization
- Edge cases and troubleshooting

Use collapsible sections or clear visual hierarchy to separate levels.
```

### 3. Multi-Format Output

Request multiple output formats:

```
Provide three versions:

1. Full Version (markdown_full.md)
   - Complete documentation with all sections

2. Quick Reference (markdown_quick.md)
   - Condensed version with key points
   - Command reference
   - Common patterns only

3. Presentation Version (markdown_slides.md)
   - Formatted for reveal.js or similar
   - Slide breaks (---)
   - Speaker notes in comments
```

### 4. Validation and Linting

Add validation instructions:

```
After generation, perform validation:

Markdown Lint Checks:
□ No trailing whitespace
□ Consistent list markers (* or -)
□ Proper blank lines around elements
□ No duplicate heading text
□ Link references are defined
□ Code fences are closed
□ HTML is valid (if used)

Content Quality Checks:
□ No Lorem Ipsum or placeholder text
□ All examples are complete
□ Commands are tested/testable
□ No broken links
□ Consistent terminology
□ Proper capitalization
□ No orphan headings

If issues found, provide:
1. List of issues with line numbers
2. Corrected version
3. Explanation of changes
```

## Integration with Version Control

### Git-Friendly Markdown

```
Optimize the markdown for git workflows:

- Line length: Max 100 characters (for better diffs)
- One sentence per line (semantic line breaks)
- Avoid trailing spaces
- Use reference-style links for better readability in diffs:
  [link text][ref-id]
  
  [ref-id]: https://example.com

- Include a changelog section formatted for git log:
  ## Changelog
  
  ### [1.2.0] - 2025-10-16
  #### Added
  - New section on error handling
  #### Changed
  - Updated API examples to v2
  #### Fixed
  - Corrected typo in installation steps
```

## Quality Rubric

Evaluate generated markdown documents using this rubric (1-5 scale):

| Criterion | 1 (Poor) | 3 (Good) | 5 (Excellent) |
|-----------|----------|----------|---------------|
| **Structure** | Missing sections | Has required sections | Logical flow, complete structure |
| **Clarity** | Confusing, jargon-heavy | Mostly clear | Crystal clear, well-explained |
| **Examples** | Missing or broken | Working examples | Comprehensive, diverse examples |
| **Formatting** | Syntax errors | Mostly correct | Perfect markdown syntax |
| **Completeness** | Major gaps | Covers main topics | Comprehensive coverage |
| **Accessibility** | No alt text, poor structure | Basic accessibility | Fully accessible |

## Common Patterns

### Pattern 1: Tutorial Format

```markdown
# Tutorial: {Topic}

## What You'll Learn
- Outcome 1
- Outcome 2
- Outcome 3

## Prerequisites
- Requirement 1
- Requirement 2

## Step 1: {First Step}
Explanation...
```code
Example code
```

✅ **Checkpoint:** What you should see now...

## Step 2: {Second Step}
...
```

### Pattern 2: Reference Guide

```markdown
# {Topic} Reference

## Quick Links
- [Common Tasks](#common-tasks)
- [API Methods](#api-methods)
- [Examples](#examples)

## Common Tasks

### Task 1: {Task Name}
**Use Case:** When you need to...
**Steps:**
1. First step
2. Second step

**Example:**
```code
Example
```

**See Also:** [Related Task](#task-2)
```

### Pattern 3: Troubleshooting Guide

```markdown
# Troubleshooting {Topic}

## Error: {Error Message}

**Symptoms:**
- What you see
- Expected vs actual behavior

**Common Causes:**
1. Cause 1 with likelihood: High/Medium/Low
2. Cause 2 with likelihood

**Solutions:**

### Solution 1 (Recommended)
Steps to fix...

### Solution 2 (Alternative)
Alternative approach...

**Prevention:**
How to avoid this in future...
```

## Tips for Advanced Usage

1. **Modular Generation** - Generate sections separately for very large documents
2. **Template Libraries** - Create reusable section templates
3. **Style Inheritance** - Reference existing docs for style consistency
4. **Automated Testing** - Include testable code examples
5. **Localization Ready** - Structure for easy translation

## Related Resources

- [First Edition](markdown_prompt_engineer_first.md) - Basic markdown generation
- [Third Edition](markdown_prompt_engineer_third.md) - Expert-level techniques
- Prompt #22 from main collection: README scaffolding
- Prompt #66 from main collection: Prompt chaining design

---

**Version:** 2.0  
**Last Updated:** 2025-10-16  
**Compatibility:** GPT-4, Claude 3 Opus/Sonnet, and similar advanced LLMs
