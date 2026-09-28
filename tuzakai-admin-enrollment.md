---
name: TuzakAI administrator enrollment
description: Why site settings require explicit owner authorization rather than first-user bootstrap.
---

Do not grant administrator privileges to the first person who signs up or visits the site. The settings editor remains inaccessible until the real owner signs in and their account is explicitly authorized.

**Why:** A publicly reachable site could be visited by someone else first. Automatic first-user promotion would hand over contact and social-link controls to an attacker.

**How to apply:** When helping the owner activate site settings, request only their non-secret account identifier after sign-in and authorize it through the workspace secrets flow. Do not fabricate a contact address or open anonymous writes to bypass this step.