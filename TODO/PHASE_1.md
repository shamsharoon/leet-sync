# Phase 1 – Data-Dump Testing

Goal: Validate that the extension can **collect** and **persist** raw problem-submission data from both Leetcode and Neetcode.

## Checklist

- [ ] Instrument content script to capture on-page submission events.
- [ ] Extract the following fields after every successful submission:
  - Problem ID / internal key
  - Title (slug & display title)
  - Tags / topic list
  - Difficulty
  - Source code (all languages, where available)
  - Runtime & memory stats
  - Timestamp of completion
- [ ] Save captured payload locally (IndexedDB) and log to the dev console for quick inspection.
- [ ] Verify that data persists after full page reload.
- [ ] Export sample JSON files for:
  - 3 solved Leetcode problems
  - 3 solved Neetcode problems
- [ ] Document any missing or inconsistent fields between the two sites.
- [ ] Add Jest tests for the parsing utilities (ensure correct field extraction).
- [ ] Create troubleshooting guide for common capture failures (e.g., DOM changes, login state).

> Thoroughly test every item before moving to Phase 2.
