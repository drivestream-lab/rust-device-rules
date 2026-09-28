# Changelog

All notable changes to `rust-device-rules` are documented here.

---

## v0.1.0

### Summary

Initial constitution for long-running Rust device daemons — core vs platform
backends, process lifecycle, local IPC transport craft, footprint governance,
cloud adapter without domain logic, credential-store hygiene, and shared
practice names aligned with `python-services-rules` (DI/singleton, fail-fast,
SDD, testing tiers).

### Changes

- Initial module set (see `code-guidelines-index.mdc`)
- MIT license, versioned submodule adoption pattern

### Migration guide

- Greenfield: mount at `.cursor/rules` and pin `v0.1.0`
- No prior consumers
