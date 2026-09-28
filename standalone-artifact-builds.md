---
name: Standalone artifact builds
description: Distinguish managed workflow environment injection from one-off static builds.
---

Treat a standalone shell build and a managed artifact workflow as different environments. A healthy managed preview does not mean a bare build command receives the service's injected runtime variables.

**Why:** A standalone production build initially failed at config loading because runtime-only values were absent, even while the managed development service started successfully. That failure was about how the command was launched, not broken application routing.

**How to apply:** Verify both the managed workflow and the standalone build. Keep port and base-path checks strict when serving, but do not require a listening port for a static build; let deployment-supplied values take precedence when present.