# Minecraft Plugin API Contract Tests

Reusable test cases for validating plugin integrations against the API contracts they consume or provide. The goal is to catch behavioral incompatibilities before a plugin combination reaches a live server.

## Contract areas
- Provider discovery and enable/disable lifecycle.
- Missing-provider behavior and actionable diagnostics.
- Permission checks and UUID-based identity handling.
- Threading expectations for callbacks and server API access.
- Configuration migration and default behavior.
- Timeouts, partial failures, and clean resource shutdown.

Run contracts against the exact supported Paper or proxy version and the real provider implementation where practical. Keep test fixtures disposable and avoid production player data. A passing contract suite covers only the behaviors it asserts; publish the tested dependency versions and limitations.