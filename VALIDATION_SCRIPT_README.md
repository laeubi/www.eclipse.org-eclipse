# N&N Validation Script

## Overview

This Python script validates New & Noteworthy (N&N) entries against the guidelines specified in `news/instructions.md`. It checks markdown files for compliance with formatting rules, naming conventions, and style guidelines.

**Note:** This script is currently located in `/tmp/` for development. To use it permanently:
1. Copy it to a permanent location in the repository (e.g., `tools/validate_nn_entries.py` or `news/scripts/validate_nn_entries.py`)
2. Update all path references in this documentation
3. Consider adding it to version control for team use

## Installation

No installation required. The script uses only Python standard library.

**Requirements:**
- Python 3.6+
- No external dependencies

## Usage

### Basic Usage

```bash
python3 validate_nn_entries.py
```

This will validate releases 4.37, 4.38, and 4.39 by default.

### Custom Validation

To validate specific releases, modify the script:

```python
# In the __main__ section
issues = validator.validate_all(['4.36', '4.37', '4.38'])
```

## What It Checks

### 1. Title Formatting
- **Title Case**: Major words should be capitalized
- **No Trailing Punctuation**: Titles should not end with `.!?,;:`

### 2. Contributors Section
- **Presence**: Each entry should have a `<details><summary>Contributors</summary>` section
- **GitHub Links**: Contributor links should use format: `[Name](https://github.com/username)`
- **No Trailing Spaces**: Contributor names should not have trailing spaces

### 3. Image References
- **PNG Format**: All images should be `.png` files
- **Lowercase Names**: Image filenames should be all lowercase
- **Hyphen Separators**: Use hyphens `-` instead of underscores `_`

### 4. UI Elements
- **Backticks**: UI elements, commands, and shortcuts should use backticks
  - Example: `Quick Fix`, `Ctrl+1`, `Preferences > General > Keys`

### 5. GitHub Links
- **In Comments**: Issue/PR links should be in HTML comments `<!-- link -->`
- Not visible in rendered text

## Output Format

### Issue Report

```
news/4.37/platform.md:
--------------------------------------------------------------------------------
  ⚠ Line 113 [WARNING] Trailing Spaces
     Contributor name has trailing/leading spaces: "Sougandh S "
     💡 Use: "Sougandh S"

  ⚠ Line 113 [WARNING] Image Naming
     Image name should be all lowercase: CompareResult.png
     💡 Rename to: compareresult.png
```

### Summary

```
================================================================================

Summary: 0 errors, 48 warnings, 18 info
```

## Severity Levels

- **✗ ERROR**: Critical issues that must be fixed
- **⚠ WARNING**: Style violations that should be fixed
- **ℹ INFO**: Suggestions for improvement

## Integration Options

### Pre-commit Hook

Add to `.git/hooks/pre-commit`:

```bash
#!/bin/bash
if git diff --cached --name-only | grep -E "news/.*\.md$"; then
    python3 tools/validate_nn_entries.py
    if [ $? -ne 0 ]; then
        echo "N&N validation failed. Fix issues before committing."
        exit 1
    fi
fi
```

### GitHub Actions

Create `.github/workflows/validate-nn.yml`:

```yaml
name: Validate N&N Entries

on:
  pull_request:
    paths:
      - 'news/**/*.md'

jobs:
  validate:
    runs-on: ubuntu-latest
    steps:
      - uses: actions/checkout@v4
      - name: Run N&N Validation
        run: python3 tools/validate_nn_entries.py
```

## Common Issues and Fixes

### 1. Trailing Spaces

**Issue:**
```markdown
- [John Doe ](https://github.com/jdoe)
```

**Fix:**
```markdown
- [John Doe](https://github.com/jdoe)
```

### 2. Image Naming

**Issue:**
```markdown
![My Feature](images/MyFeature.png)
```

**Fix:**
```markdown
![My Feature](images/my-feature.png)
```
*(Also rename the actual file)*

### 3. Missing Backticks

**Issue:**
```markdown
Use the Quick Fix (Ctrl+1) to fix this.
```

**Fix:**
```markdown
Use the `Quick Fix` (`Ctrl+1`) to fix this.
```

### 4. Title Case

**Issue:**
```markdown
### New feature for debugging
```

**Fix:**
```markdown
### New Feature for Debugging
```

### 5. Visible GitHub Links

**Issue:**
```markdown
See https://github.com/eclipse-jdt/eclipse.jdt.core/pull/4293
```

**Fix:**
```markdown
<!-- https://github.com/eclipse-jdt/eclipse.jdt.core/pull/4293 -->
See the related pull request for details.
```

## Extending the Script

### Adding New Rules

To add a new validation rule, modify the `validate_entry` method:

```python
def validate_entry(self, entry: Dict, file_path: Path) -> List[Dict]:
    issues = []
    
    # Add your new check here
    if some_condition:
        issues.append({
            'file': str(file_path.relative_to(self.repo_path)),
            'line': entry['line_num'],
            'severity': 'warning',  # or 'error', 'info'
            'rule': 'Rule Name',
            'message': 'Description of the issue',
            'suggestion': 'How to fix it'
        })
    
    return issues
```

### Customizing Output

Modify the `format_issues` method to change output format.

## Limitations

1. **Context-Aware Checks**: Some rules require human judgment
   - Technical terms with special casing (e.g., "macOS", "iOS")
   - Acronyms that should stay uppercase
   
2. **Image Renaming**: Script only detects issues, doesn't rename files
   - Must be done manually or with separate script
   
3. **False Positives**: Some warnings may not apply in all contexts
   - Use judgment when applying suggestions

## Maintenance

### Updating Rules

When `news/instructions.md` changes:
1. Review new guidelines
2. Update validation rules in script
3. Test against existing entries
4. Document changes in this README

### Version History

- **v1.0** (2025-12-23): Initial version
  - Validates title format, contributors, images, backticks
  - Checks trailing spaces and GitHub links
  - Supports releases 4.37+

## Support

For issues or questions:
1. Check this README
2. Review `news/instructions.md`
3. See example entries in published N&N documents
4. Open an issue in the repository

## License

This script is part of the Eclipse Platform website project and follows the same license.
