# Phase 2 – Data Mapping (Leetcode ↔ Neetcode)

Goal: Achieve reliable **1-to-1 problem matching** between the two platforms.

## Checklist

- [ ] Collect 100-problem sample datasets from both sites.
- [ ] Identify potential unique keys:
  - Leetcode: `questionId`, slug, internal `_id`
  - Neetcode: problem slug, external link back to Leetcode (if present)
- [ ] Build a mapping table (`mapping.json`) with fields:
  ```json
  {
    "leetcodeQuestionId": "",
    "leetcodeSlug": "",
    "neetcodeSlug": "",
    "status": "matched | fuzzy | unknown"
  }
  ```
- [ ] Write script to auto-generate/refresh the mapping file.
- [ ] Implement fuzzy matcher (title similarity ≥ 90 %) as fallback when unique keys fail.
- [ ] Log ambiguous matches for manual review.
- [ ] Add unit tests for exact and fuzzy matching logic.
- [ ] Document mapping rules and edge cases.

> Do not proceed to Phase 3 until mapping accuracy ≥ 98 % on the sample set.
