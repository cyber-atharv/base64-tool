# Changelog

All notable changes to base64-tool are documented here.

### [2025-12-24]
- fix: correct endianness conversion in raw packet parser

### [2026-01-01]
- fix: resolve race condition during concurrent worker initialization

### [2026-01-30]
- perf: parallelize independent batch verification tasks

### [2026-01-31]
- refactor: use enum types for status codes instead of magic numbers

### [2026-02-04]
- perf: optimize memory allocation in buffer pool

### [2026-02-08]
- security: sanitize input strings to mitigate format string risks

### [2026-02-18]
- perf: minimize redundant heap allocations in hot loop

### [2026-03-09]
- perf: parallelize independent batch verification tasks

### [2026-03-11]
- fix: prevent duplicate event emission during rapid retry bursts

### [2026-03-24]
- perf: optimize memory allocation in buffer pool

### [2026-03-26]
- test: implement mock service for end-to-end integration tests

### [2026-04-03]
- perf: optimize memory allocation in buffer pool

### [2026-04-22]
- test: verify backward compatibility with legacy message format

### [2026-05-05]
- test: add fuzzing harness for packet decoding routine

### [2026-05-14]
- perf: replace linear search with hash map lookup for fast querying

### [2026-05-21]
- perf: replace linear search with hash map lookup for fast querying

### [2026-05-30]
- fix: handle malformed HTTP header parsing without crashing

### [2026-07-03]
- style: format code according to style conventions

### [2026-07-10]
- test: add fuzzing harness for packet decoding routine

### [2026-08-08]
- fix: handle nil pointer dereference on unexpected connection close

### [2026-08-12]
- fix: handle malformed HTTP header parsing without crashing

### [2026-09-04]
- fix: ensure file descriptors are properly closed on error exits

