# Markdown Prompt Engineer - First Edition

A structured template for generating professional markdown documentation using AI assistance.

## Overview

This prompt template helps you create well-structured, professional markdown documents with consistent formatting, clear organization, and proper markdown syntax.

## Template Structure

### Basic Markdown Document Generator

**Technique Tags:** Role + Constraints + Style Guide + Template Conditioning

```
Act as a professional technical writer and markdown expert. Create a comprehensive markdown document on {topic} for {audience}.

Requirements:
- Target audience: {audience}
- Document type: {document_type}
- Tone: {tone} (e.g., professional, friendly, technical, educational)
- Length: {word_count} words

Structure Requirements:
1. Title (H1) - Clear and descriptive
2. Overview/Introduction - Brief summary (100-150 words)
3. Table of Contents - Auto-linked sections for documents >500 words
4. Main Content - Organized with H2 and H3 headings
5. Code Examples - Use fenced code blocks with language tags
6. Lists - Use bullet points or numbered lists appropriately
7. Tables - Format data in markdown tables when applicable
8. Links and References - Include relevant hyperlinks
9. Conclusion/Summary - Key takeaways
10. Additional Resources - Related links or further reading

Markdown Best Practices:
- Use consistent heading hierarchy (don't skip levels)
- Include blank lines before and after headings
- Use backticks for inline code: `code`
- Use triple backticks with language identifier for code blocks
- Use > for blockquotes
- Use **bold** for emphasis, *italic* for lighter emphasis
- Create horizontal rules with --- on their own line
- Ensure all links are properly formatted: [text](url)
- Use proper list indentation (2 or 4 spaces)

Constraints:
{constraints}

Additional Context:
{additional_context}

Output only the markdown content, properly formatted and ready to use.
```

## Usage Examples

### Example 1: Technical Documentation

```
Act as a professional technical writer and markdown expert. Create a comprehensive markdown document on "REST API Best Practices" for "backend developers".

Requirements:
- Target audience: Backend developers
- Document type: Technical guide
- Tone: Professional and technical
- Length: 1500 words

Structure Requirements:
[... same as above ...]

Constraints:
- Include at least 5 code examples in different languages
- Add a comparison table of REST vs GraphQL
- Include security best practices section
- Cite industry standards (OpenAPI, RFC specifications)

Additional Context:
Focus on modern API design patterns, versioning strategies, and error handling.

Output only the markdown content, properly formatted and ready to use.
```

### Example 2: README File

```
Act as a professional technical writer and markdown expert. Create a comprehensive markdown document on "Project README" for "open source contributors".

Requirements:
- Target audience: Open source contributors
- Document type: README.md
- Tone: Friendly and welcoming
- Length: 800 words

Structure Requirements:
1. Title (H1) - Project name
2. Badges - Build status, version, license
3. Overview/Introduction - What the project does
4. Features - Key capabilities (bullet list)
5. Installation - Step-by-step setup
6. Usage - Basic examples with code
7. Configuration - Options and settings
8. Contributing - How to contribute
9. License - License information
10. Contact/Support - How to get help

Constraints:
- Include emoji for visual appeal (📋 📚 🚀 etc.)
- Add code snippets for installation and usage
- Include shields.io badge examples
- Keep installation steps clear and numbered

Additional Context:
This is for a Python CLI tool for data validation.

Output only the markdown content, properly formatted and ready to use.
```

## Parameter Reference

| Parameter | Description | Examples |
|-----------|-------------|----------|
| `{topic}` | Main subject of the document | "Git Workflow Guide", "API Documentation" |
| `{audience}` | Target readers | "developers", "end users", "technical managers" |
| `{document_type}` | Type of markdown doc | "README", "tutorial", "guide", "specification" |
| `{tone}` | Writing style | "professional", "friendly", "technical", "educational" |
| `{word_count}` | Approximate length | "500", "1500", "3000" |
| `{constraints}` | Specific requirements | "Include diagrams", "Add FAQ section" |
| `{additional_context}` | Extra background info | Project details, special requirements |

## Advanced Variations

### With Diagram Support

Add this to the constraints section:

```
- Include Mermaid diagrams for:
  * System architecture (if applicable)
  * Workflow or process flows
  * Data models or relationships
- Use proper Mermaid syntax within ```mermaid code blocks
```

### With SEO Optimization

Add this to the requirements section:

```
SEO Requirements:
- Include meta description (160 characters)
- Use semantic heading structure
- Add alt text descriptions for image placeholders
- Include relevant keywords naturally: {keywords}
```

### With Internationalization

Add this to the constraints section:

```
I18n Considerations:
- Avoid idioms and colloquialisms
- Use simple, clear language
- Include language indicator at top: <!-- lang: en-US -->
- Mark translatable sections
```

## Quality Checklist

Before finalizing the output, ensure:

- [ ] All headings follow proper hierarchy (H1 → H2 → H3)
- [ ] Code blocks include language identifiers
- [ ] Links are properly formatted and descriptive
- [ ] Lists are consistently formatted
- [ ] Tables are properly aligned
- [ ] No orphaned or inconsistent formatting
- [ ] Document is scannable with clear sections
- [ ] Examples are realistic and helpful
- [ ] Grammar and spelling are correct
- [ ] Tone is consistent throughout

## Common Use Cases

1. **Project Documentation** - READMEs, contributing guides, changelogs
2. **Technical Guides** - Tutorials, how-tos, API documentation
3. **Knowledge Base** - FAQs, troubleshooting, best practices
4. **Blog Posts** - Technical articles, case studies, tutorials
5. **Specifications** - RFCs, design docs, architecture decisions

## Tips for Better Results

1. **Be Specific** - The more context you provide, the better the output
2. **Iterate** - Start with basic structure, then refine with specific requirements
3. **Use Examples** - Provide sample content or similar documents as reference
4. **Set Constraints** - Clear boundaries lead to more focused content
5. **Review and Edit** - Always review AI-generated content for accuracy and tone

## Related Prompts

- Prompt #22: README scaffolding (from main collection)
- Prompt #60: Evaluation rubric creator (for quality assessment)
- Prompt #62: Guardrail configurator (for content policies)

---

**Version:** 1.0  
**Last Updated:** 2025-10-16  
**Compatibility:** GPT-4, Claude 3, and similar LLMs
