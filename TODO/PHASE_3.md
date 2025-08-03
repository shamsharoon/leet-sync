# Phase 3 – Cross-Platform Submission

Goal: Automatically **push solutions** between platforms once a problem is solved on either one.

## Checklist

### Leetcode → Neetcode

- [ ] After capturing a successful Leetcode submission, check mapping table for corresponding Neetcode slug.
- [ ] Use Neetcode API (or scripted form submission) to create/update the solution.
- [ ] Handle authentication (cookie/session or OAuth, depending on support).
- [ ] Respect Neetcode rate limits; implement exponential back-off.
- [ ] Provide user feedback in popup ("Synced ✅" or error message).

### Neetcode → Leetcode

- [ ] Mirror the above flow for Neetcode origin submissions.
- [ ] Ensure that language choice and runtime stats are preserved when pushing to Leetcode (if the API allows it).

### Common

- [ ] Expose toggle switches in the UI to enable/disable each direction synchronisation.
- [ ] Centralised error logging with retry queue.
- [ ] Unit tests mocking both platform APIs.
- [ ] Security review – avoid storing credentials in plain text.

> All critical errors must be resolved before moving on.
