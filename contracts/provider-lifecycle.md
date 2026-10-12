# Provider lifecycle contract

- Consumer startup with provider present succeeds and reports its version.
- Consumer startup with provider absent follows documented optional/required behavior.
- Provider disable closes owned resources and rejects new work.
- Consumer disable unregisters listeners and callbacks.
- Re-enable in a disposable test environment does not duplicate registrations.
- Failures include provider identity and actionable next steps without leaking secrets.
