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

### 4. Code Block Validation Checklist
Before committing documentation:
- [ ] All code blocks have language specifiers
- [ ] No nested code blocks at same indentation (use 4-space indent)
- [ ] Blank lines before and after all code blocks
- [ ] Code blocks are properly closed (matching ``` pairs)
