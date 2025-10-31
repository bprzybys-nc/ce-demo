# Project Context for AI Assistant

## Documentation Formatting Rules

### 1. Nested Code Blocks
**NEVER nest code blocks with triple backticks (```) inside other code blocks at the same indentation level.** This breaks markdown rendering and causes preview glitches.

**Wrong:**
```
```markdown
Some text
  ```json
  {"key": "value"}
  ```
```
```

**Correct - Option 1 (Indent nested blocks with 4 spaces):**
```
```markdown
Some text
    ```json
    {"key": "value"}
    ```
```
```

**Correct - Option 2 (Use indented code without fences):**
```
```markdown
Some text

    {"key": "value"}
```
```

**Rule:** When showing code examples within markdown code blocks, indent the inner code block markers by 4 spaces, OR use indented code (4 spaces without fences).

### 2. Code Block Language Specifiers
**ALWAYS specify a language for code blocks.** This improves syntax highlighting and prevents rendering issues.

**Wrong:**
```
```
some code here
```
```

**Correct:**
```
```python
some code here
```
```

**Common language identifiers:**
- `bash` or `shell` - Shell commands
- `python`, `javascript`, `typescript`, `java`, `go`, etc. - Programming languages
- `json`, `yaml`, `xml` - Data formats
- `markdown` - Markdown content
- `text` - Plain text output (logs, console output)
- `sql` - Database queries

**Rule:** Every code fence must specify a language: ` ```language `

### 3. Blank Lines Around Code Blocks
**ALWAYS add blank lines before and after code blocks** for proper markdown rendering.

**Wrong:**
```
Some text
```python
code
```
More text
```

**Correct:**
```
Some text

```python
code
```

More text
```

### 4. Multiple-Choice Questions Format
**ALWAYS format multiple-choice questions using indented markdown lists** for better readability.

**Standard markdown doesn't support alphabetical lists (a, b, c) natively.** Use indented unordered lists with manual lettering.

**Correct format:**
```markdown
1. Question text here?
   - a) Option 1
   - b) Option 2
   - c) Option 3
   - d) Option 4
```

**Alternative (without bullets):**
```markdown
1. Question text here?
   a) Option 1
   b) Option 2
   c) Option 3
   d) Option 4
```

**Rule:** Indent options with 3 spaces, use "- a)" format for best markdown compatibility.

### 5. Collapsible/Spoiler Content (Details/Summary)
**Use HTML `<details>` and `<summary>` tags for collapsible content.** This is the most compatible solution across platforms (GitHub, GitLab, most Markdown processors).

**Format:**
```html
<details>
  <summary><strong>Click to reveal spoiler</strong></summary>

  Your hidden content here. You can use **any markdown** inside.

</details>
```

**Key points:**
- **Space after `<summary>` tag is critical** for proper markdown rendering
- Works with images, code blocks, tables, and any markdown
- Click to expand/collapse (not hover)
- Works on GitHub, GitLab, VS Code preview, and most processors

**Best use cases:**
- Quiz/exercise answers (interactive learning)
- Hints or solutions to problems
- Optional deep-dive content
- Lengthy supplementary material
- Actual spoilers in content

**Example:**
```markdown
Try the exercise first!

<details>
  <summary><strong>Click to reveal answer</strong></summary>

  **Answer:** The correct approach is to use async/await.

</details>
```

**Platform-specific alternatives:**
- Discord: `||spoiler text||`
- Reddit: `>!spoiler text!<`
- Not needed for general markdown - use `<details>` for maximum compatibility

### 6. Documentation Validation Checklist
Before committing documentation:
- [ ] All code blocks have language specifiers
- [ ] No nested code blocks at same indentation (use 4-space indent)
- [ ] Blank lines before and after all code blocks
- [ ] Code blocks are properly closed (matching ``` pairs)
- [ ] Multiple-choice questions use indented list format (3-space indent with "- a)" bullets)
- [ ] Quiz/exercise answers wrapped in `<details><summary>` tags for interactive learning
- [ ] Space after `<summary>` tag for markdown rendering (use 2-space indent inside `<details>`)
