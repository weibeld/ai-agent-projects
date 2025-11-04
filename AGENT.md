# AI Agent Instructions: Research and Format Project Entries

## Overview

Your task is to research and format AI agent project entries in the README.md file. You will process unprocessed items (bullet points with URLs) and convert them into formatted table entries.

## Table Format

Each section should have a table with the following columns:

```markdown
| Project | Description | Open-Source | GitHub | Type | Released |
|---------|-------------|-------------|--------|------|----------|
```

### Column Specifications

**Project:**
- Format: `**[Project Name](URL)**`
- Make the link bold
- If there's a parent organization different from the project name, add it in parentheses: `**[Project Name](URL)** (by Organization)`

**Description:**
- If the unprocessed item has text after the URL (e.g., `- https://example.com: foo bar baz`), use that text as the description
- Only fix obvious typos if present
- If the unprocessed item has only a URL, create a single short sentence description
- Maximum length: 80 characters (if possible)
- Avoid buzzwords like "AI-powered", "revolutionary", "cutting-edge"
- Avoid qualitative adjectives like "fast", "powerful", "best", "professional", "amazing"
- Keep it factual and concise
- End with a period

**Open-Source:**
- Use ✅ for open-source projects
- Use ❌ for closed-source projects

**GitHub:**
- If open-source with a GitHub repository: `[user/repo](https://github.com/user/repo) (⭐️ ~Xk)`
- Format: Shorten URL to `user/repo` in the link text
- Add star count in format: `(⭐️ ~X.Xk)` for thousands, `(⭐️ ~X)` for under 1k
- Round to one decimal place for thousands (e.g., 5214 → ~5.2k, 847 → ~800, 12543 → ~12.5k)
- If no repository: ❌

**Type:**
- Use emoji icons based on how the project is delivered:
  - 💻 CLI: Command-line interface tool (runs in terminal)
  - 🖥️ Binary: Standalone application to install locally (e.g., desktop IDE or editor)
  - 🧩 Plugin: Extension or plugin for existing software (e.g., IDE extensions, editor plugins)
  - 🌍 Web: Web-based application (accessed through a browser)
- If a project has multiple delivery types, include all applicable emoji icons (e.g., `💻 CLI, 🌍 Web`)

**Released:**
- Format: `[Mon YYYY](source-url)`
- Example: `[Oct 2025](https://news.ycombinator.com/item?id=12345)`
- Link to a reliable source documenting the release date
- If no release date can be found after thorough research, use `Unknown` (no link)

## Research Requirements

For each unprocessed item, research the following:

### 1. Project Name
- Official name of the project
- Parent organization (only if different from project name)

### 2. Type
- Determine how the project is delivered to users:
  - **💻 CLI:** Runs in a terminal/command line
  - **🖥️ Binary:** Standalone desktop application to install locally (e.g., IDE, editor)
  - **🧩 Plugin:** Extension for existing software (e.g., VS Code extension, browser plugin)
  - **🌍 Web:** Web-based service accessed through a browser
- If the project supports multiple delivery types, list all applicable types

### 3. Open-Source Status
- Is the code publicly available?
- Check for GitHub, GitLab, or other public repositories

### 4. GitHub Repository
- If open-source, find the GitHub repository URL
- Get the current star count
- Format as `user/repo` with star count

### 5. Release Date
- **CRITICAL:** Take extra care when researching release dates
- You MUST find one of the following:
  - An official launch or release announcement
  - A reliable source like Wikipedia
  - A source that explicitly states "released in [Month Year]" or "launched in [Month Year]"
- Do NOT guess or infer release dates
- Do NOT use company founding dates unless explicitly stated as the release date
- Link to the specific source where you found the date
- If no reliable release date can be found after thorough research, use `Unknown`

### 6. Description
- If text exists after the URL in the bullet point, use it (with typo fixes only)
- If no text exists, create a concise single-sentence description
- Avoid marketing language and qualitative adjectives
- Be factual and neutral

## Research Process

1. **Use WebSearch** to find information about the project
2. **Use WebFetch** to visit the project's website and documentation
3. **Verify release dates** carefully:
   - Check Wikipedia
   - Look for official blog posts or announcements
   - Search for "launched" or "released" in news articles
   - Confirm the date from multiple sources if possible
4. **Check GitHub** for repository details and star counts

## Updating Existing Entries

For existing table entries with GitHub repositories:

1. Visit each GitHub repository URL
2. Get the current star count
3. Update the star count in the format `(⭐️ ~X.Xk)` or `(⭐️ ~X)` (rounded to one decimal place for thousands)
4. ONLY update the GitHub star count. Do NOT change any other fields (project name, description, type, release date, etc.)

## Handling Mixed Processed and Unprocessed Items

A section may contain:
- **Only unprocessed items** (bullet list): Create a new table
- **Only processed items** (table): Update star counts and "Last updated" date
- **Both processed and unprocessed items** (table + bullet list): Add new rows to the existing table

When a table already exists:
1. Add new rows to the existing table for unprocessed items
2. Append new entries to the end of the table in the same order as they appear in the bullet list
3. Remove the bullet points after adding them to the table
4. The "🤖 Content researched by AI. Last updated YYYY-MM-DD." line already exists below the table
5. Update the date in that line to today's date

## Final Steps

After processing all items in a section:

1. Remove the processed bullet points
2. If no "🤖 Content researched by AI. Last updated YYYY-MM-DD." line exists, add it below the table
3. If the line already exists, update the date to today's date
4. Use today's date in ISO format (YYYY-MM-DD)

After processing ALL sections in the README:

1. Update ALL "Last updated" dates below tables to today's date
2. Update the top-level "Content last updated" line near the beginning of README.md (format: `_**🤖 Content last updated YYYY-MM-DD by AI.**_`) to today's date

## Example Transformations

### Example 1: New Section (Only Unprocessed Items)

**Before:**
```markdown
## General

- https://example.com/tool: helps with testing
- https://another-tool.io
```

**After:**
```markdown
## General

| Project | Description | Open-Source | GitHub | Type | Released |
|---------|-------------|-------------|--------|------|----------|
| **[ExampleTool](https://example.com/tool)** | Helps with testing. | ✅ | [user/example-tool](https://github.com/user/example-tool) (⭐️ ~3.2k) | 💻 CLI | [Mar 2024](https://github.com/user/example-tool/releases) |
| **[AnotherTool](https://another-tool.io)** | Creates automated workflows for development teams. | ❌ | ❌ | 🌍 Web | [Jan 2025](https://news.ycombinator.com/item?id=12345) |

🤖 Content researched by AI. Last updated 2025-11-04.
```

### Example 2: Existing Table with New Unprocessed Items

**Before:**
```markdown
## General

| Project | Description | Open-Source | GitHub | Type | Released |
|---------|-------------|-------------|--------|------|----------|
| **[ExampleTool](https://example.com/tool)** | Helps with testing. | ✅ | [user/example-tool](https://github.com/user/example-tool) (⭐️ ~3.0k) | 💻 CLI | [Mar 2024](https://github.com/user/example-tool/releases) |

🤖 Content researched by AI. Last updated 2025-10-15.

- https://newproject.com
```

**After:**
```markdown
## General

| Project | Description | Open-Source | GitHub | Type | Released |
|---------|-------------|-------------|--------|------|----------|
| **[ExampleTool](https://example.com/tool)** | Helps with testing. | ✅ | [user/example-tool](https://github.com/user/example-tool) (⭐️ ~3.2k) | 💻 CLI | [Mar 2024](https://github.com/user/example-tool/releases) |
| **[NewProject](https://newproject.com)** | Manages infrastructure deployments. | ✅ | [company/newproject](https://github.com/company/newproject) (⭐️ ~1.8k) | 🖥️ Binary | [Sep 2024](https://newproject.com/blog/launch) |

🤖 Content researched by AI. Last updated 2025-11-04.
```

Note: The star count was updated from ~3.0k to ~3.2k and the date was updated to today.

## Quality Guidelines

1. **Accuracy:** All information must be verified from reliable sources
2. **Consistency:** Follow the exact format specifications
3. **Neutrality:** Avoid promotional language
4. **Completeness:** Research all required fields
5. **Verification:** Double-check release dates with reliable sources
6. **Timeliness:** Update all "Last updated" dates to current date when processing

## Important Notes

- Process ALL unprocessed items in the README (all sections)
- Update star counts for ALL existing GitHub repositories
- For existing items: ONLY update the GitHub star count, do NOT modify any other fields
- Update ALL "Last updated" dates to today's date (both at the top of the document and below each table)
- Update the top-level "Content last updated" line near the beginning of README.md with today's date
- Be especially careful with release date research
- Maintain consistent formatting throughout
