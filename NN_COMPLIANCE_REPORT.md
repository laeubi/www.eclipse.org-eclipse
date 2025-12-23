# New & Noteworthy (N&N) Compliance Report

**Date:** 2025-12-23  
**Releases Checked:** 4.37, 4.38, 4.39  
**Total Issues Found:** 89 (0 errors, 71 warnings, 18 info)

## Executive Summary

This report analyzes all N&N entries in recent releases (4.37, 4.38, 4.39) for compliance with the guidelines specified in `news/instructions.md`. The validation found several common patterns of non-compliance that can be systematically addressed.

## Key Findings

### Issue Categories

1. **Image Naming Issues (56 instances)** - Most common issue
   - 41 cases: Filenames not all lowercase
   - 15 cases: Using underscores instead of hyphens

2. **Trailing Spaces in Contributor Names (16 instances)**
   - Extra spaces after contributor names in markdown links

3. **Missing UI Element Backticks (6 instances)**
   - UI elements, commands, and shortcuts not wrapped in backticks

4. **GitHub Issue Links Not in Comments (5 instances)**
   - Issue/PR links visible in text instead of HTML comments

5. **Missing Contributors Section (4 instances)**
   - Entries without contributor details sections

6. **Title Case Issues (2 instances)**
   - Titles not following Title Case convention

7. **Image Format Issues (1 instance)**
   - GIF file used instead of PNG

## Detailed Findings by Release

### 4.37 Release

#### news/4.37/jdt.md

**Image Naming Issues:**
- `overlappingStartEndCustomRegionMarkersPrefs.png` → should be `overlappingstartendcustomregionmarkersprefs.png`
- `overlappingStartEndCustomRegionMarkersExpanded.png` → should be `overlappingstartendcustomregionmarkersexpanded.png`
- `overlappingStartEndCustomRegionMarkersCollapsed.png` → should be `overlappingstartendcustomregionmarkerscollapsed.png`
- `deprecatedFieldCleanUp.png` → should be `deprecatedfieldcleanup.png`
- `deprecatedFieldExampleBefore.png` → should be `deprecatedfieldexamplebefore.png`
- `deprecatedFieldExampleAfter.png` → should be `deprecatedfieldexampleafter.png`
- `extractMethodAccessors.png` → should be `extractmethodaccessors.png`
- `rulerToggleMenuWithHitcountAndTriggerpoint.png` → should be `rulertogglemenuwithhitcountandtriggerpoint.png`

**Missing Contributors Section:**
- "JDT Developers" section (line 112)

#### news/4.37/pde.md

**Image Naming Issues:**
- `pde_junit_launch_config.png` → should use hyphens: `pde-junit-launch-config.png`
- `invalidCharactersCheck.png` → should be `invalidcharacterscheck.png`
- `spaceCheckBeforeColon.png` → should be `spacecheckbeforecolon.png`

**Trailing Spaces:**
- "Christoph Läubrich " (lines 7, 31)
- "Gireesh Punathil " (line 68)
- "Neha Burnwal " (line 68)

**Backticks Missing:**
- Multiple instances of "quick fix" and "Quick fix" should be wrapped in backticks (line 68)

#### news/4.37/platform.md

**Image Naming Issues:**
- `terminal_console.png` → should use hyphens: `terminal-console.png`
- `webkit_browser_search_dialog1.png` → should use hyphens: `webkit-browser-search-dialog1.png`
- `webkit_browser_search_dialog2.png` → should use hyphens: `webkit-browser-search-dialog2.png`
- `CompareClipBoard.png` → should be `compareclipboard.png`
- `CompareResult.png` → should be `compareresult.png`
- `ReplaceClipBoard.png` → should be `replaceclipboard.png`
- `menu_state_system.png` → should use hyphens: `menu-state-system.png`
- `menu_state_noimage.png` → should use hyphens: `menu-state-noimage.png`
- `menu_state_overlay.png` → should use hyphens: `menu-state-overlay.png`
- `QuickSearchAscendingSort.png` → should be `quicksearchascendingsort.png`
- `QuickSearchDescendingSort.png` → should be `quicksearchdescendingsort.png`
- `BreakpointGroupMenu.png` → should be `breakpointgroupmenu.png`
- `EnablementGrouping.png` → should be `enablementgrouping.png`

**Trailing Spaces:**
- "Christoph Läubrich " (line 33)
- "Simeon Andreev " (line 76)
- "Andrey Loskutov " (line 76)
- "Sougandh S " (lines 108, 154, 178)
- "Stephan Wahlbrink " (line 133)

#### news/4.37/platform_isv.md

**Missing Contributors Section:**
- "Terminal View and Connectors Support" (line 8)
- "Clarified ImageDataProvider Contract" (line 42)

### 4.38 Release

#### news/4.38/jdt.md

**Title Case Issue:**
- "Eclipse support for JUnit 6.0.1" → should be "Eclipse Support for JUnit 6.0.1"

**Backticks Missing:**
- "Ctrl+1" mentioned without backticks (line 14)

**Image Naming Issues:**
- `JUnit6NewTestCaseWizard.png` → should be `junit6newtestcasewizard.png`
- `JUnit6AddClasspathContainer.png` → should be `junit6addclasspathcontainer.png`
- `JUnit6QuickFixProposal.png` → should be `junit6quickfixproposal.png`
- `JUnit6BuildPropertiesContainer.png` → should be `junit6buildpropertiescontainer.png`
- `organize-imports-before.png` ✓ (correct)
- `organize-imports-after.png` ✓ (correct)
- `add-import-module-before.png` ✓ (correct)
- `add-import-module-after.png` ✓ (correct)
- `markdown-comments-templates.png` ✓ (correct)
- `multi-release-jar-config.png` ✓ (correct)
- `DeprecationWarnings.png` → should be `deprecationwarnings.png`
- `DeprecationQuickFixes.png` → should be `deprecationquickfixes.png`
- `VariableCompareWithClipboardOption.png` → should be `variablecomparewithclipboardoption.png`
- `VariableCompareWithClipboardResult.png` → should be `variablecomparewithclipboardresult.png`
- `VariableCompareWithCllipboardArrays.png` → should be `variablecomparewithcllipboardarrays.png` (note: typo "Cllipboard")
- `VariableCompareWithCllipboardPrimitives.png` → should be `variablecomparewithcllipboardprimitives.png` (note: typo "Cllipboard")
- `LambdaBreakpointDialog.png` → should be `lambdabreakpointdialog.png`
- `LambdaFilteringInDialog.png` → should be `lambdafilteringindialog.png`
- `LambdaInlineBreakpointsView.png` → should be `lambdainlinebreakpointsview.png`

**GitHub Issue Links:**
- Several links should be in comments (lines 165, 203, 245)

#### news/4.38/pde.md

**Image Naming Issues:**
- `osgiFrameworkSelector.png` → should be `osgiframeworkselector.png`

**Trailing Spaces:**
- "Christoph Laeubrich " (line 7)

#### news/4.38/platform.md

**Image Naming Issues:**
- `Autopin.png` → should be `autopin.png`
- `AutopinPreference.png` → should be `autopinpreference.png`
- `VersionControlPreference.png` → should be `versioncontrolpreference.png`
- `ConsoleElapsedPreference.png` → should be `consoleelapsedpreference.png`
- `ConsoleElapsedDropDown.png` → should be `consoleelapseddropdown.png`
- `ConsoleElapsedSelection.png` → should be `consoleelapsedselection.png`
- `ConsoleElapsedFormat.png` → should be `consoleelapsedformat.png`
- `MonitorSpecificScalingOff.png` → should be `monitorspecificscalingoff.png`
- `MonitorSpecificScalingOn.png` → should be `monitorspecificscalingon.png`
- `DebugPromptOnSkipBreakpoints.png` → should be `debugpromptonskipbreakpoints.png`

**Trailing Spaces:**
- "Sougandh S " (lines 68, 193)
- "Andrey Loskutov " (line 193)

**GitHub Issue Links:**
- Multiple links should be in comments (line 94: https://github.com/eclipse-platform/eclipse.platform.swt/issues/1961)
- Multiple links in "Merging the JVM and the Operating System Trust Stores" section (line 158)

#### news/4.38/platform_isv.md

**Trailing Spaces:**
- "Arun Jose " (line 13)
- "Heiko Klare " (line 13)
- "Michael Bangas " (line 13)

### 4.39 Release

#### news/4.39/jdt.md

**Image Format Issue:**
- `LambdaHighlight.gif` → should be converted to PNG format

**Image Naming Issues:**
- `LambdaHighlight.gif` → should be `lambdahighlight.png` (after conversion)

**Missing Contributors Section:**
- "JDT Developers" section (line 64)

## Recommended Actions

### Priority 1: Quick Fixes (Can be automated)

1. **Fix Trailing Spaces** (16 instances)
   - Remove trailing spaces from contributor names
   - Files affected: 4.37/pde.md, 4.37/platform.md, 4.38/pde.md, 4.38/platform.md, 4.38/platform_isv.md

2. **Add Missing Contributors Sections** (4 instances)
   - Add `<details><summary>Contributors</summary>` sections
   - Files: 4.37/jdt.md, 4.37/platform_isv.md, 4.39/jdt.md

### Priority 2: Image Renaming (Requires coordination)

**Note:** Image renaming requires:
1. Renaming actual image files in the `images/` directories
2. Updating references in markdown files
3. Ensuring no broken links

**Recommended approach:**
- Create a migration script to rename files and update references atomically
- Or document required changes for contributors to apply

### Priority 3: Style Improvements

1. **Add Backticks for UI Elements** (6 instances)
   - Wrap UI elements, commands, shortcuts in backticks
   - File: 4.37/pde.md

2. **Move GitHub Links to Comments** (5 instances)
   - Wrap issue/PR links in `<!-- -->` comments
   - Files: 4.38/jdt.md, 4.38/platform.md

3. **Fix Title Case** (2 instances)
   - Capitalize major words in titles
   - File: 4.38/jdt.md

4. **Convert Image Format** (1 instance)
   - Convert GIF to PNG
   - File: 4.39/jdt.md

## Validation Rules Reference

Based on `news/instructions.md`, the key rules are:

1. **Title Format**
   - Use Title Case
   - No trailing punctuation
   - Keep short and snappy

2. **Contributors**
   - Use `<details><summary>Contributors</summary>` format
   - Link to GitHub profiles: `[Name](https://github.com/username)`
   - Use real full names (or pseudonyms with consent)

3. **Content**
   - Use active voice ("you" not "the user")
   - Use backticks for UI elements: `Quick Fix`, `Ctrl+1`, `Preferences > General > Keys`
   - Complete sentences with punctuation
   - Start each sentence on new line

4. **Images**
   - Use PNG format only
   - Filename: lowercase with hyphens (e.g., `foo-view.png`)
   - Store in `images/` subdirectory
   - Include descriptive label

5. **Links**
   - GitHub issue/PR links as invisible comments: `<!-- link -->`
   - Don't link to issues in visible text
   - Don't promote third-party products

## Next Steps

1. **Immediate Actions (This PR):**
   - ✓ Create validation script
   - ✓ Generate this compliance report
   - Apply quick fixes (trailing spaces, missing sections)

2. **Future Improvements:**
   - Create image renaming migration script
   - Add pre-commit hook for validation
   - Document style guide more prominently
   - Consider adding linting to CI/CD

3. **Contributor Education:**
   - Share this report with contributors
   - Update contributing guidelines
   - Create examples of perfect entries

## Conclusion

The N&N entries are generally well-formatted, but there are consistent patterns of minor non-compliance that can be systematically addressed. Most issues are cosmetic (image naming, trailing spaces) rather than functional. Implementing automated validation in CI/CD would prevent future issues.

---

**Generated by:** N&N Validation Script  
**Script Location:** `/tmp/validate_nn_entries.py`  
**Command to reproduce:** `python3 /tmp/validate_nn_entries.py`
