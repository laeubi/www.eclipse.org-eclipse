# N&N Enhancement Suggestions by File

This document provides specific, actionable suggestions for enhancing each N&N file to comply with the guidelines in `news/instructions.md`.

## Quick Reference Table

| Release | File | Issues | Priority |
|---------|------|--------|----------|
| 4.37 | jdt.md | 9 | High |
| 4.37 | pde.md | 12 | High |
| 4.37 | platform.md | 22 | High |
| 4.37 | platform_isv.md | 2 | Medium |
| 4.38 | jdt.md | 23 | High |
| 4.38 | pde.md | 2 | Low |
| 4.38 | platform.md | 19 | High |
| 4.38 | platform_isv.md | 3 | Low |
| 4.39 | jdt.md | 3 | Medium |

---

## news/4.37/jdt.md

### Issues to Fix

#### 1. Trailing Spaces - NOT FOUND
Upon re-checking, this file doesn't have trailing spaces in contributor names. Skip this fix.

#### 2. Image Naming (8 files to rename)

**Current → Recommended:**
```
overlappingStartEndCustomRegionMarkersPrefs.png → overlapping-start-end-custom-region-markers-prefs.png
overlappingStartEndCustomRegionMarkersExpanded.png → overlapping-start-end-custom-region-markers-expanded.png
overlappingStartEndCustomRegionMarkersCollapsed.png → overlapping-start-end-custom-region-markers-collapsed.png
deprecatedFieldCleanUp.png → deprecated-field-cleanup.png
deprecatedFieldExampleBefore.png → deprecated-field-example-before.png
deprecatedFieldExampleAfter.png → deprecated-field-example-after.png
extractMethodAccessors.png → extract-method-accessors.png
rulerToggleMenuWithHitcountAndTriggerpoint.png → ruler-toggle-menu-with-hitcount-and-triggerpoint.png
```

**Actions:**
1. Rename image files in `news/4.37/images/` directory
2. Update markdown references in the file

#### 3. Missing Contributors Section

**Section:** "JDT Developers" (line 112)

**Action:** This appears to be a commented-out section header, not an actual entry. No action needed.

---

## news/4.37/pde.md

### Issues to Fix

#### 1. Trailing Spaces in Contributor Names (4 instances)

**Lines to fix:**
- Line 7: `- [Christoph Läubrich ](https://github.com/laeubi)` → Remove trailing space
- Line 31: `- [Christoph Läubrich ](https://github.com/laeubi)` → Remove trailing space
- Line 68: `- [Gireesh Punathil ](...)` → Remove trailing space
- Line 68: `- [Neha Burnwal ](...)` → Remove trailing space

#### 2. Image Naming (3 files)

**Current → Recommended:**
```
pde_junit_launch_config.png → pde-junit-launch-config.png
invalidCharactersCheck.png → invalid-characters-check.png
spaceCheckBeforeColon.png → space-check-before-colon.png
```

#### 3. Missing Backticks for UI Elements

**Section:** Around line 68 in "Validators for Plugin XML Files" entry

**Text occurrences to fix:**
- "quick fix" → `quick fix`
- "Quick fix" → `Quick Fix`

**Example fix:**
```markdown
Before: A quick fix is now available to fix this issue.
After: A `Quick Fix` is now available to fix this issue.
```

---

## news/4.37/platform.md

### Issues to Fix

#### 1. Trailing Spaces in Contributor Names (7 instances)

**Fix these contributor lines:**
- Line 33: `- [Christoph Läubrich ](https://github.com/laeubi)`
- Line 76: `- [Simeon Andreev ](https://github.com/trancexpress)`
- Line 76: `- [Andrey Loskutov ](https://github.com/iloveeclipse)`
- Line 108: `- [Sougandh S ](https://github.com/SougandhS)`
- Line 133: `- [Stephan Wahlbrink ](https://github.com/wahlbrink)`
- Line 154: `- [Sougandh S ](https://github.com/SougandhS)`
- Line 178: `- [Andrey Loskutov ](https://github.com/iloveeclipse)`
- Line 178: `- [Sougandh S ](https://github.com/SougandhS)`

#### 2. Image Naming (13 files)

**Current → Recommended:**
```
terminal_console.png → terminal-console.png
webkit_browser_search_dialog1.png → webkit-browser-search-dialog1.png
webkit_browser_search_dialog2.png → webkit-browser-search-dialog2.png
CompareClipBoard.png → compare-clipboard.png
CompareResult.png → compare-result.png
ReplaceClipBoard.png → replace-clipboard.png
menu_state_system.png → menu-state-system.png
menu_state_noimage.png → menu-state-noimage.png
menu_state_overlay.png → menu-state-overlay.png
QuickSearchAscendingSort.png → quick-search-ascending-sort.png
QuickSearchDescendingSort.png → quick-search-descending-sort.png
BreakpointGroupMenu.png → breakpoint-group-menu.png
EnablementGrouping.png → enablement-grouping.png
```

---

## news/4.37/platform_isv.md

### Issues to Fix

#### Missing Contributors Sections (2 entries)

**Entry 1:** "Terminal View and Connectors Support" (line 8)

**Suggestion:** Add contributors if known, or leave as-is if this is a collective contribution.

**Entry 2:** "Clarified ImageDataProvider Contract" (line 42)

**Suggestion:** Add contributors if known, or leave as-is if this is a documentation clarification.

**Note:** These are API documentation entries, and it's acceptable not to have contributors listed for API clarifications. Consider this LOW priority.

---

## news/4.38/jdt.md

### Issues to Fix

#### 1. Title Case Issue

**Current:** "Eclipse support for JUnit 6.0.1" (line 14)  
**Fixed:** "Eclipse Support for JUnit 6.0.1"

#### 2. Missing Backticks

**Location:** Line 14, around text mentioning Ctrl+1

**Example fix:**
```markdown
Before: Quick Fix (Ctrl+1) proposal
After: Quick Fix (`Ctrl+1`) proposal
```

#### 3. Image Naming (18 files to rename)

**Current → Recommended:**
```
JUnit6NewTestCaseWizard.png → junit6-new-test-case-wizard.png
JUnit6AddClasspathContainer.png → junit6-add-classpath-container.png
JUnit6QuickFixProposal.png → junit6-quick-fix-proposal.png
JUnit6BuildPropertiesContainer.png → junit6-build-properties-container.png
DeprecationWarnings.png → deprecation-warnings.png
DeprecationQuickFixes.png → deprecation-quick-fixes.png
VariableCompareWithClipboardOption.png → variable-compare-with-clipboard-option.png
VariableCompareWithClipboardResult.png → variable-compare-with-clipboard-result.png
VariableCompareWithCllipboardArrays.png → variable-compare-with-clipboard-arrays.png (fix typo!)
VariableCompareWithCllipboardPrimitives.png → variable-compare-with-clipboard-primitives.png (fix typo!)
LambdaBreakpointDialog.png → lambda-breakpoint-dialog.png
LambdaFilteringInDialog.png → lambda-filtering-in-dialog.png
LambdaInlineBreakpointsView.png → lambda-inline-breakpoints-view.png
```

**Note:** Files with correct names (keep as-is):
- organize-imports-before.png ✓
- organize-imports-after.png ✓
- add-import-module-before.png ✓
- add-import-module-after.png ✓
- markdown-comments-templates.png ✓
- multi-release-jar-config.png ✓

#### 4. GitHub Issue Links to Move to Comments

**Lines with visible issue links:**
- Line 165: Move issue links to HTML comments
- Line 203: Move issue links to HTML comments
- Line 245: Move issue links to HTML comments

**Example fix:**
```markdown
Before: See https://github.com/eclipse-jdt/eclipse.jdt.core/pull/4293
After: <!-- https://github.com/eclipse-jdt/eclipse.jdt.core/pull/4293 -->
```

---

## news/4.38/pde.md

### Issues to Fix

#### 1. Trailing Space in Contributor Name

**Line 7:** `- [Christoph Laeubrich ](https://github.com/laeubi)`

#### 2. Image Naming (1 file)

**Current → Recommended:**
```
osgiFrameworkSelector.png → osgi-framework-selector.png
```

---

## news/4.38/platform.md

### Issues to Fix

#### 1. Trailing Spaces in Contributor Names (4 instances)

**Fix these:**
- Line 68: `- [Sougandh S ](https://github.com/SougandhS)`
- Line 193: `- [Sougandh S ](https://github.com/SougandhS)`
- Line 193: `- [Andrey Loskutov ](https://github.com/iloveeclipse)`

#### 2. Image Naming (10 files)

**Current → Recommended:**
```
Autopin.png → autopin.png
AutopinPreference.png → autopin-preference.png
VersionControlPreference.png → version-control-preference.png
ConsoleElapsedPreference.png → console-elapsed-preference.png
ConsoleElapsedDropDown.png → console-elapsed-dropdown.png
ConsoleElapsedSelection.png → console-elapsed-selection.png
ConsoleElapsedFormat.png → console-elapsed-format.png
MonitorSpecificScalingOff.png → monitor-specific-scaling-off.png
MonitorSpecificScalingOn.png → monitor-specific-scaling-on.png
DebugPromptOnSkipBreakpoints.png → debug-prompt-on-skip-breakpoints.png
```

#### 3. GitHub Issue Links to Move to Comments

**Section:** "Enhancements of Monitor-Specific UI Scaling on Windows" (line 94)
- Move link: https://github.com/eclipse-platform/eclipse.platform.swt/issues/1961

**Section:** "Merging the JVM and the Operating System Trust Stores" (line 158)
- Multiple issue/PR links should be in comments

**Example fix:**
```markdown
Before:
For more background information see also:
- https://bugs.eclipse.org/bugs/show_bug.cgi?id=567504
- https://github.com/eclipse-packaging/packages/pull/224

After:
<!-- 
For more background information see also:
- https://bugs.eclipse.org/bugs/show_bug.cgi?id=567504
- https://github.com/eclipse-packaging/packages/pull/224
-->
For more background information see the related issues.
```

---

## news/4.38/platform_isv.md

### Issues to Fix

#### Trailing Spaces in Contributor Names (3 instances)

**Line 13, fix these:**
- `- [Arun Jose ](https://github.com/arunjose696)`
- `- [Heiko Klare ](https://github.com/HeikoKlare)`
- `- [Michael Bangas ](https://github.com/MichaelBangas)`

---

## news/4.39/jdt.md

### Issues to Fix

#### 1. Image Format Issue

**File:** `LambdaHighlight.gif`

**Action Required:**
1. Convert GIF to PNG format (or extract representative frame)
2. Rename to: `lambda-highlight.png`
3. Update markdown reference

**Rationale:** Instructions specify PNG format only for consistency and better compression.

#### 2. Missing Contributors Section

**Section:** "JDT Developers" (line 64)

**Note:** This appears to be a commented-out section template, not an actual entry. Verify if this needs contributors or should be removed.

---

## Implementation Priority

### Phase 1: Quick Fixes (Minimal Risk)
1. ✅ **Remove trailing spaces** - Can be done with simple find/replace
2. ✅ **Fix title case** - 2 instances only
3. ✅ **Add missing backticks** - Improves readability

### Phase 2: Structural Changes (Medium Risk)
1. **Move GitHub links to comments** - Changes visibility but not functionality
2. **Add missing contributor sections** - Only if contributors are identified

### Phase 3: File Operations (Higher Risk)
1. **Rename image files** - Requires careful coordination
   - Must rename actual files AND update markdown references
   - Risk of broken links if not done atomically
   - Consider creating a migration script

2. **Convert GIF to PNG** - Requires image processing
   - Need graphics tool to convert
   - Verify quality after conversion

---

## Automation Opportunities

### 1. Pre-commit Hook
```bash
#!/bin/bash
# Check for trailing spaces in contributor names
if git diff --cached --name-only | grep -E "news/.*\.md$"; then
    python3 tools/validate_nn_entries.py --staged
fi
```

### 2. CI/CD Validation
Add GitHub Actions workflow to validate N&N entries on PRs.

### 3. Image Renaming Script
```python
# Script to rename images and update markdown references atomically
def rename_images_in_release(release_dir):
    # Scan markdown files for image references
    # Rename image files
    # Update markdown references
    # Commit atomically
    pass
```

---

## Conclusion

Most issues are cosmetic and can be fixed systematically. The highest impact improvements are:

1. **Trailing spaces** - Easy fix, improves git history
2. **Image naming** - Consistency, but requires careful migration
3. **Backticks** - Improves readability
4. **GitHub links** - Aligns with guidelines

Recommend implementing Phase 1 immediately, Phase 2 as time permits, and Phase 3 with proper testing and migration planning.
