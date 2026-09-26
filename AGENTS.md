# Repository instructions

This is a static browser prototype with `index.html` and `test.html`; application logic is inline. There is no package manifest or automated test/lint/typecheck/build suite. `test.html` is a live Anthropic request page, not a unit-test runner.

For UI development, serve the root with Python 3 using `python3 -m http.server 8000`, then inspect the changed page and browser errors. The simulator can issue repeated provider requests, and the pages use an API key from localStorage. Use dummy credentials and mocked requests for validation; do not read an existing browser profile's key, start a paid simulation, or expose keys in screenshots/logs without the corresponding task scope. A static render does not prove provider behavior.

For HTML/instruction-only changes, inspect syntax, referenced paths, and `git diff --check -- <changed-paths>`. For simulation changes, exercise the changed state transitions with controlled responses; inspect actual rendered states for visual changes and stop owned preview processes when done.

Complete the authorized change through relevant verification and repair of introduced failures. Resolve routine implementation choices directly; ask only for information or decisions that materially affect the result. If blocked, name the affected action and missing prerequisite, continue independent work, and close with changed paths, checks actually run, and unverified behavior.
